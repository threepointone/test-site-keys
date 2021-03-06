## Steps

1. Let's use a globally installed version of wrangler here. Run `npm install -g wrangler`. (Alternately, use `npx wrangler@latest` instead of `wrangler` for all commands.)
2. We're using a standard Sites project generated by wrangler v1 here. The only change was to rename `wrangler.toml` to `my.wrangler.toml` so that wrangler doesn't automatically pick it up when we run commands.
3. `cd workers-site && npm install && cd ..`
4. `wrangler dev --config my.wrangler.toml`, open `localhost:8787`, see the site as expected.
5. `wrangler dev workers-site/index.js --site public`, open `localhost:8787`, see the site as expected.
6. `wrangler publish --config my.wrangler.toml`, open `test-site-keys.<subdomain>.workers.dev`, see the site as expected.
7. `wrangler publish workers-site/index.js --site public --compatibility-date 2022-06-12 --name test-site-keys`, open `test-site-keys.<subdomain>.workers.dev`, see the site as expected.
