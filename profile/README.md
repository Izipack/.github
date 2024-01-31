# Welcome to the Izipack Github Organization 👋
![Izipack Logo](https://raw.githubusercontent.com/Izipack/.github/main/assets/largeizipack.svg)
## Documentation pages 📄
- [Global Documentation page](https://izipack.github.io/documentation/)
- [Shipping API Swagger page](https://shipping-api.izipack.nl/index.html)

- ## Architecture overview
There are currently two environments active, acc and prod. The azure resources mentioned belowed are all named to their environment like `-acc or -prod`.

### API
There is the shipping-api which is responsible for accepting new creation of shipments, webhook updates from smartroute

### Polling Best Estimated Delivery Time
This is done by an azure function called func-shipment-processor. This calls all the scheduled orders from the active depots to check their ETA.

To configure the active depots there is an configuration setting called SmartRoute:ActiveDepots which is a comma separated string.
