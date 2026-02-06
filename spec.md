# Specification

## Summary
**Goal:** Fix the production deployment failure, identify the root cause, and successfully retry a fresh production deployment without changing existing app behavior.

**Planned changes:**
- Investigate the prior production deploy failure (build/bundle, canister configuration, frontend asset build, or backend canister build) and document the root cause.
- Apply minimal code/configuration adjustments required to make the production build and deploy succeed.
- Re-run production deployment and verify post-deploy behavior remains unchanged across existing routes and the Home page simulator flow.

**User-visible outcome:** The app deploys to production successfully, loads in the browser, all existing routes render (Home, How It Works, Disclaimer, About Us, Contact, Privacy Policy), and the Home simulator still shows the 60-second loading state followed by exactly one random result message with no new external API calls.
