# OpenSaaS

A Next.js interface starter with Clerk sign-in/sign-up screens, an animated landing page, feature cards and a contact-form prototype.

This repository is a fork of [gdgdtu/OpenSaaS](https://github.com/gdgdtu/OpenSaaS). Upstream authorship and the fork relationship are preserved.

## Implemented scope

- Next.js App Router and React components.
- Clerk provider, account controls and sign-in/sign-up pages.
- Tailwind styling, Framer Motion animations and Vercel Analytics integration.
- Client-side contact-form validation and a local submission confirmation.

Payment, organisation-management and role-management cards describe the intended product direction; they are not complete backend features. The contact form does not send email or persist submissions.

## Development

Use Node.js 20+ and npm:

```sh
git clone https://github.com/Lakshaypal/OpenSaaS.git
cd OpenSaaS
npm ci
```

Create `.env.local` using your own Clerk development application's configuration:

```dotenv
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_publishable_key
CLERK_SECRET_KEY=your_secret_key
```

Keep the secret key out of Git and browser code.

```sh
npm run dev
```

Open `http://localhost:3000`.

```sh
npm run build
npm start
```

## Structure

- `src/app/`: application layout, landing page and authentication routes.
- `src/components/ui/`: navbar, feature cards, form and shared controls.
- `src/components/variants/`: animation settings.
- `src/lib/utils.ts`: class-name utilities.

Authentication UI is present, but a production application still needs its own server-side access controls and feature backend.
