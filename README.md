from pathlib import Path
from html import escape

root = Path(__file__).parent
languages = [
    ('C', 'C', 'Systems', '#9fb8d7'),
    ('C++', 'C++', 'Concurrency', '#72b7ff'),
    ('Rs', 'Rust', 'Memory safety', '#eab18f'),
    ('Go', 'Go', 'Network services', '#5cd6e8'),
    ('Py', 'Python', 'Automation', '#e7cb79'),
    ('>_', 'Bash', 'Shell scripting', '#97d6ad'),
    ('SQL', 'SQL', 'Data & queries', '#b7a7ef'),
    ('Lua', 'Lua', 'Embedded scripting', '#a2afff'),
]

for theme in ('dark', 'light'):
    if theme == 'dark':
        bg, bar, tile, line = '#0d1117', '#161b22', '#131a23', '#293341'
        fg, muted, accent = '#eff4fa', '#98a7ba', '#8cdacb'
    else:
        bg, bar, tile, line = '#f8fafc', '#eef2f6', '#ffffff', '#d9e1ea'
        fg, muted, accent = '#172333', '#56677b', '#167a69'

    parts = [f'''<svg xmlns="http://www.w3.org/2000/svg" width="900" height="418" viewBox="0 0 900 418" role="img" aria-labelledby="title desc">
<title id="title">ThreadCrash — languages and systems</title>
<desc id="desc">SecOps, NetOps and SRE. C, C++, Rust, Go, Python, Bash, SQL and Lua.</desc>
<defs><clipPath id="window"><rect x="1" y="1" width="898" height="416" rx="16"/></clipPath></defs>
<g clip-path="url(#window)" font-family="Segoe UI, Arial, sans-serif">
<rect width="900" height="418" fill="{bg}"/>
<path d="M0 0H900V49H0Z" fill="{bar}"/>
<path d="M0 49H900" stroke="{line}"/>
<circle cx="25" cy="25" r="5" fill="#ff6259"/>
<circle cx="44" cy="25" r="5" fill="#ffbd2e"/>
<circle cx="63" cy="25" r="5" fill="#28c840"/>
<text x="91" y="30" fill="{muted}" font-size="12" font-family="Consolas, monospace">threadcrash / profile</text>
<text x="869" y="30" text-anchor="end" fill="{muted}" font-size="11" letter-spacing="1.8">README.md</text>
<text x="35" y="114" fill="{fg}" font-size="43" font-weight="700" letter-spacing="-1.7">ThreadCrash</text>
<text x="36" y="143" fill="{muted}" font-size="15">Systems software · Concurrency · Infrastructure</text>
<text x="863" y="111" text-anchor="end" fill="{accent}" font-family="Consolas, monospace" font-size="13">SecOps · NetOps · SRE</text>
<text x="36" y="187" fill="{muted}" font-size="10" font-weight="600" letter-spacing="2.4">LANGUAGES</text>
<path d="M144 183H864" stroke="{line}"/>''']

    for i, (symbol, name, detail, color) in enumerate(languages):
        x, y = 36 + (i % 4) * 211, 204 + (i // 4) * 94
        ink = color if theme == 'dark' else '#314f70'
        parts.append(f'''<g transform="translate({x} {y})">
<rect width="195" height="80" rx="10" fill="{tile}" stroke="{line}"/>
<text x="16" y="34" fill="{ink}" font-family="Consolas, monospace" font-size="21" font-weight="700">{escape(symbol)}</text>
<text x="78" y="32" fill="{fg}" font-size="15" font-weight="600">{escape(name)}</text>
<text x="16" y="61" fill="{muted}" font-size="11">{escape(detail)}</text>
</g>''')

    parts.append(f'</g><rect x="1" y="1" width="898" height="416" rx="16" fill="none" stroke="{line}"/></svg>')
    (root / 'assets' / f'banner-{theme}.svg').write_text('\n'.join(parts), encoding='utf-8')

alt = 'ThreadCrash | SecOps, NetOps, SRE | C, C++, Rust, Go, Python, Bash, SQL, Lua'
for path, prefix in [(root / 'README.md', 'assets'), (root.parent / 'Readmd.md', 'MyCurrentReadme.md/assets')]:
    path.write_text(f'''<p align="center">
  <picture>
    <source media="(prefers-color-scheme: light)" srcset="{prefix}/banner-light.svg">
    <img src="{prefix}/banner-dark.svg" alt="{alt}" width="900">
  </picture>
</p>
''', encoding='utf-8')
