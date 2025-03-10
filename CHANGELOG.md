# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [0.6.9] - 2023-01-06

-   Added missing types definitions - `"BSV"` in `CurrencyCode`.
-   Exported hidden types: `PaymentRequestItem`, `Attachment`, `TransactionParticipant`.

## [0.6.8] - 2022-12-05

-   Downgraded `nanoid` to have CommonJS support
-   Fixed query parameters formatting int the get public profiles by aliases endpoint

## [0.6.3] - 2022-11-29

-   Add `oauth-nonce` to the headers to avoid errors when creating multiple requests with the same `oauth-timestamp` in headers.

## [0.6.2] - 2022-11-15

-   Fully rewritten in TS.
-   Packaging/building process with Vite.
-   Fast tests using Vitest.
-   Smaller package size.
-   ESM & CJS support.
-   Documentation (Jsdoc) for all core functions and classes of the SDK.

> 🙏🏻 Credits to [trgsv](https://github.com/trgsv)

## [0.5.0] - 2022-09-29

-   Improve typescript definitions
-   Add [new feature](https://docs.handcash.io/docs/create-accounts) to create new accounts directly from apps
-   Fix bug when requesting multiple profiles [#31](https://github.com/HandCash/handcash-connect-sdk-js/pull/31)

> 🙏🏻 Credits to [krisarsov](https://github.com/krisarsov)

## [0.4.3] - 2022-06-21

-   Fix typescript definition for `PaymentParameters`

## [0.4.2] - 2022-05-18

-   Add typescript definitions `index.d.ts`!
-   Add tags to the payment items: `wallet.pay({ payments: [{ destination: 'satoshi', tags: ['tag1', 'tag2'], currencyCode: 'USD', sendAmount: 0.05}] });`

> 🙏🏻 Credits to [Alvin](https://github.com/irkaal)

## [0.4.1] - 2022-03-25

-   Use production environment by default in the SDK initialization.
-   Extend `HandCashOwner` (RUN extension) to return the NFT locations.

## [0.4.0] - 2022-03-17

-   Change SDK initialization to define `appSecret`.
-   Revert `clientUrl` so it redirects to app.handcash.io instead of handcash.io.

## [0.3.1] - 2022-02-06

-   Extend `Wallet` to expose the user total balance via `account.wallet.getTotalBalance()`.

## [0.3.0] - 2022-01-07

-   Update `clientUrl` so it redirects to handcash.io instead of app.handcash.io
-   Fix issues with some endpoints using HTTP GET with a body as it's not supported by some browsers.

## [0.2.9-beta] - 2021-09-01

-   Extend `HandCashOwner.nextOwner()` with an optional alias `HandCashOwner.nextOwner(alias)`.

## [0.2.8-beta] - 2021-08-23

-   Include app-secret in the headers for the run extension endpoints.

## [0.2.7-beta] - 2021-07-23

-   Improve JSDoc for better auto-completion
-   Improve error feedback when using wrong auth tokens: "Missing authToken" and "Invalid authToken".
-   Method to get the change spend limits URL via `handCashConnect.getChangeSpendLimitsUrl()`
-   Beta features: `HandCashPurse` and `HandCashOwner` to integrate HandCash Connect with RUN.

## [0.2.6] - 2021-04-9

-   Add feature in wallet to retrieve an exchange rate for a given fiat currency code.

## [0.2.5] - 2021-04-9

-   Add extra query parameters to the redirection URL so when the user is redirected back to the app these parameters are included.
-   Expose `bitcoinUnit` as part of users' public profile.

## [0.2.7-beta] - 2021-07-23

-   Improve JSDoc for better auto-completion
-   Improve error feedback when using wrong auth tokens: "Missing authToken" and "Invalid authToken".
-   Method to get the change spend limits URL via `handCashConnect.getChangeSpendLimitsUrl()`
-   Beta features: `HandCashPurse` and `HandCashOwner` to integrate HandCash Connect with RUN.

## [0.2.6] - 2021-04-9

-   Add feature in wallet to retrieve an exchange rate for a given fiat currency code.

## [0.2.5] - 2021-04-9

-   Add extra query parameters to the redirection URL so when the user is redirected back to the app these parameters are included.
-   Expose `bitcoinUnit` as part of users' public profile.

## [0.2.4] - 2021-03-17

-   Improve error propagation so `HandCashApiError` does not wrap generic errors as they lose the stack trace and other important details.
-   Replace deprecated `@std/esm` by `esm`.

## [0.2.3] - 2020-12-17

-   Fixed wrong signature issue affecting browser integration.

## [0.2.2] - 2020-12-14

-   Initial release
