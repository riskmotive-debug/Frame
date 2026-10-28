# FRAME prototype — Supabase login

Run `python3 -m http.server 8000 --bind 0.0.0.0` in this folder. The site uses the Supabase JS SDK from a CDN and needs an internet connection.

## Connect authentication
1. Create a Supabase project. In Project Settings > API (or Connect), find the Project URL and publishable/anon key. Do NOT use a service_role or secret key in client-side code.
2. Enter those public values in `config.js`.
3. In Authentication > Providers, enable Email and Google. Configure Google OAuth credentials there, and register Supabase's Google callback URL in Google Cloud.
4. In Authentication > URL Configuration, set the deployed site URL and add allowed redirect URLs. Use a supported local URL for testing. Confirm email sign-up links as required by your Supabase settings.
5. Deploy the files to a static hosting service. Google OAuth generally needs an authorized domain and a valid redirect configuration.

Sign-in is real only when configured. There is no service account or backend authorization; video access cannot be securely protected using a static frontend alone. Watchlists and progress are local to the browser, not shared across devices. The sample film is Big Buck Bunny, © Blender Foundation, CC BY 3.0; https://peach.blender.org/. Other titles are fictional placeholders. No BDIX integration, live licensed catalog, mobile apps, or production-ready parental controls are included. External sources require permission and compatibility checks.
