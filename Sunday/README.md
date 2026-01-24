# Sunday

**OAuth Authentication Platform for SSI Ecosystem**

Sunday is the central authentication and identity platform for all Stealth Services Inc. applications. It provides secure OAuth-based authentication with support for passkeys and biometric login.

## Features

- 🔐 **OAuth 2.0** - Industry-standard authentication
- 🔑 **Passkey Support** - WebAuthn/FIDO2 passwordless login
- 👤 **Face ID / Touch ID** - Biometric authentication
- 🎫 **JWT Tokens** - Secure session management
- 🔗 **SSO** - Single sign-on across all SSI apps
- 📱 **Mobile Ready** - Responsive authentication UI

## How It Works

1. User visits an SSI app (MACRA, iAXIS, COVRD, etc.)
2. App redirects to Sunday for authentication
3. User logs in with passkey/biometrics
4. Sunday issues JWT token
5. User is redirected back to app with valid session

## Integration

Apps integrate with Sunday using the Sunday Auth SDK:

```javascript
// Include the SDK
<script src="/js/sunday-auth.js"></script>

// Initialize
SundayAuth.init({
    appId: 'your-app-id',
    redirectUri: window.location.origin
});

// Check authentication
if (!SundayAuth.isAuthenticated()) {
    SundayAuth.login();
}
```

## API Endpoints

- `GET /authorize` - Start OAuth flow
- `POST /token` - Exchange code for token
- `GET /userinfo` - Get user profile
- `POST /logout` - End session

## Deployment

Deployed via Cloudflare Pages as part of the SSI ecosystem.

**Live URL**: https://www.umbrassi.com/Sunday/

## Part of SSI Ecosystem

Sunday is the authentication backbone for **Stealth Services Inc.** operated by Main Street Group LLC.

---

Built with 💪 by **Main Street Group LLC**
