# Changelog

## v0.2.3

* Updates
  * Allow `muontrap` v0.6.0 to be used since the breaking change doesn't affect
    `vintage_net_mobile`
  * Force `vintage_net` v0.7.9 or later to pull in PPP IP address fix

## v0.2.2

* New features
  * Added a "monitor" for reporting a SIM card's ICCID and IMSI. These are
    useful for debugging issues with service providers. Currently this is
    only available on the BG96, but can easily be added to other modems as
    testing permits.

## v0.2.1

This release has improvements and bug fixes throughout, but primarily for the
Quectel EC25 (LTE Cat 4 modem) and Quectel BG96 (LTE Cat M1/NB1 modem)

* New features
  * Network connection stats for the EC25 and BG96 modems. This lets you see how
    the modem connected (GSM, UMTS, LTE, etc) and to which cell tower (cell id,
    lac, mcc, mnc). This is useful for debug and geolocation.
  * Improved signal strength reporting. The reports are now in ASU (arbitrary
    strength units), dBm, and bars. Bars ranges from 0 bars (no connection) to 4
    bars (strong signal) similar to a cell phone

## v0.2.0

This release has significant changes to the configuration API and
`VintageNetMobile.Modem` behaviour. No migration from the old version is
supported. We don't expect to majorly change the API in future releases. Updates
will be more incremental. The plan is to add configuration migrations so that
devices in the field can continue to work between `vintage_net_mobile` updates.

To upgrade, find the module documentation for your modem. There will be a
configuration example that should look familiar.

## v0.1.2

* Bug fix
  * Prevent `VintageNet` from trying to run `ppp` before a modem is ready.

## v0.1.1

* Bug fixes
  * Fix a timing issue when `VintageNet` would try to call a `VintageNetMobile`
    process before it was started

## v0.1.0

Initial `vintage_net_mobile` release.

