# Harshvardhansinh Jadeja — Portfolio

A responsive static portfolio built with HTML, CSS, and vanilla JavaScript. It is designed to deploy on GitHub Pages and use `harshvardhansinh.xyz`.

## Before publishing

Review `index.html` and verify:
- Email address and social profile links.
- Project descriptions and technology lists.
- Repository links and any live demos.
- Your current education and availability details.

The project cards currently link to your GitHub profile because individual repository URLs and demos should be verified before adding them.

## Deploy to GitHub Pages

1. Create a **public** GitHub repository named `harshvardhansinh-jadeja-521.github.io` (or choose another name and adjust the Pages settings accordingly).
2. Upload all files and folders from this package to the repository's **root**. Keep `index.html`, `styles.css`, `script.js`, `CNAME`, `.nojekyll`, and `assets/` at the root level.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select branch `main`, folder `/ (root)`, and click **Save**.
6. Wait for the Pages deployment to complete.

## Connect the custom domain

The `CNAME` file is already set to `harshvardhansinh.xyz`. In **Settings → Pages → Custom domain**, enter `harshvardhansinh.xyz` if it is not already filled in, then save. GitHub will check DNS.

At the domain registrar (gen.xyz), use its DNS management page to create these records. **Do not change nameservers to random values.** Keep the registrar's default nameservers if using its DNS manager.

| Type | Host / Name | Value |
|---|---|---|
| A | `@` (or blank for root) | `185.199.108.153` |
| A | `@` (or blank for root) | `185.199.109.153` |
| A | `@` (or blank for root) | `185.199.110.153` |
| A | `@` (or blank for root) | `185.199.111.153` |
| CNAME | `www` | `Harshvardhansinh-jadeja-521.github.io` |

If you choose a differently named repository, use the GitHub Pages hostname shown in your repository's Pages settings for the `www` CNAME target.

Remove old conflicting A records for `@` or `www` records that point to Weebly, but do not remove unrelated records such as email MX/TXT records if you use them. Avoid using the registrar's one-click redirect feature.

## HTTPS

After DNS resolves to GitHub Pages and the domain is verified, go back to **Settings → Pages** and enable **Enforce HTTPS** when GitHub makes it available. DNS and certificate provisioning can take some time.

## Local preview

You can double-click `index.html` to preview most of the site. For a local server, run from this folder:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Notes

- This is a static website: it does not require a build step, Node.js, or a backend.
- The Google Fonts import requires internet access; system fallbacks are included.
- The contact link opens the visitor's email app; it does not submit to a backend.
