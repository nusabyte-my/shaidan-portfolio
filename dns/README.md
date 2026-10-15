# Custom domain: shaidan.nusabyte.my

Add these A records at the DNS provider for nusabyte.my, then re-add the `CNAME`
file at the repo root and push:

    185.199.108.153
    185.199.109.153
    185.199.110.153
    185.199.111.153

Then GitHub repo → Settings → Pages → Custom domain → `shaidan.nusabyte.my` →
Enforce HTTPS once the certificate is issued (usually under 10 minutes).

Until then the site serves from https://nusabyte-my.github.io/shaidan-portfolio/
