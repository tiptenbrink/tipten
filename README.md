# tipten
Future home of all tipten.nl pages

# Tech stack
* All the front end pages will run as mostly static sites from Deno servers using Oak
  * These pages are built using Vite + React TypeScript
* They will use auth.tipten.nl, which will run on tiauth2, a Rust authentication server built with Axum
  * tiauth2 uses OPAQUE as its authentication protocol, with OAuth 2.1 Authorization Code + PKCE as the authorization flow
  * The authpage front end is also Vite + React Typescript, using WebAssembly to run the OPAQUE Rust code
  * tiauth2 uses Redis + PostgreSQL
