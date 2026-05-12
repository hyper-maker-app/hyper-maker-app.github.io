# HyperIsle Privacy Policy Site

This directory is a ready-to-publish payload for the public GitHub Pages site that hosts the HyperIsle landing page, privacy policy, Terms, and AdMob `app-ads.txt`.

## Recommended GitHub setup

Use a separate public GitHub Pages repository dedicated to the custom domain.
Copy the contents of this directory to that repository root, commit, and push to `main`.

Then open the new repository on GitHub and configure:

```text
Settings -> Pages -> Build and deployment -> Source: Deploy from a branch
Branch: main
Folder: / (root)
```

The public URLs will be:

```text
https://hyperisle.app/
https://hyperisle.app/tr/
https://hyperisle.app/app-ads.txt
```

Use `https://hyperisle.app/` in Google Play Console's Privacy policy field and Developer website field.

The included `CNAME` file sets the GitHub Pages custom domain to:

```text
hyperisle.app
```

Squarespace should remain the domain/DNS provider. Point the apex domain to GitHub Pages with these A records:

```text
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Point `www` to the GitHub Pages default hostname shown in that repository's
Pages settings. Do not use wildcard DNS records.

## app-ads.txt

This payload includes `app-ads.txt` for AdMob Authorized Digital Sellers for Apps:

```text
google.com, pub-3024447897187619, DIRECT, f08c47fec0942fa0
```

AdMob crawls `app-ads.txt` from the hostname root of the developer website listed
in the app store. Because this payload now publishes from the root
custom-domain Pages repo, the required URL is
`https://hyperisle.app/app-ads.txt`.

After the AdMob account/app is approved, compare this line with the personalized
snippet shown in AdMob > Apps > app-ads.txt. If AdMob shows a different
publisher snippet, replace the line here before publishing.
