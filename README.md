# Bring Frida Back

Static one-page site for the effort to restore the Frida Kahlo mural at Cavalcade and Irvington (Houston). No build step. Everything is in `index.html`; photos are in `images/`.

## Things still to do before launch
- Replace `images/frida-now.jpg` with an original photo of the cabinet as it is today. The current file looks like a Google Street View screenshot and should not stay on a public site.
- Confirm Anat Ronen is fine with her work being shown. Confirm UP Art Studio and the Mayor's Office of the Arts are comfortable being named under "Who is at the table".
- Done: `og:image` points to `https://bringfridaback.com/images/frida-city.jpg`.

## Edit points (script at the bottom of `index.html`)
- `EMAIL`: public contact address.
- `ABC13_URL`: news link under "Then and now".
- `SPONSOR`: leave `null` until a sponsor commits in writing. Then set `{name, logo, url}`. The sponsor card turns grey, shows the sponsor, and the letter template hides.
- `SUPPORTERS`: organizations that sent a letter of support and agreed to be listed. Each entry `{name, logo, url}`; logos go in `images/logos/`.

## Deploy on GitHub Pages with a custom domain
1. Push this folder to the root of a GitHub repo, `main` branch.
2. Repo Settings > Pages > Deploy from a branch > `main` / root. Enter the custom domain; GitHub adds a `CNAME` file.
3. DNS at the registrar:
   - Subdomain (for example `www.example.org`): CNAME to `<github-username>.github.io`.
   - Apex domain: A records to 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153.
4. After DNS resolves, enable "Enforce HTTPS" in Pages settings.
