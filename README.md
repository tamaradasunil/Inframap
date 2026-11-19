# InfraMap Expo preview

This is the Expo Go development preview for InfraMap. Explore shows local sample property data on a full-screen map; property search filters bundled listings only. There is no Places autocomplete or external place-search integration.

Phase 4 includes property browsing and filters, listing details and favorites, property posting with optional photos and documents, listing edit/pause/resume/delete, GPS or manual location capture, reverse-geocoded address where available, approximate or private pin visibility, boundary drawing, survey and plot fields, evidence timestamps and accuracy, and simulated location review stages. Review stages are demo states; GPS, imagery, boundaries and uploaded evidence do not establish ownership or legal title.

Phase 5 adds a local Services directory for repair services, professionals and contractors. Browse by provider type or an allowed category, search by provider or locality, compare up to three listings, view provider details, and request a quote, booking or consultation. The Explore map has a **Post service** shortcut. Providers select from the fixed category list, enter a shop locality, optionally capture a GPS shop pin, and verify a phone with a simulated OTP (`123456`). No SMS or Aadhaar verification is connected. Provider listings, verification labels and requests are local demo data, not vetted commercial listings.

Phase 6 adds a building-materials marketplace, including tiles and sanitaryware. Compare suppliers for the same product specification, filter by category and shop locality, view shop pins on a map, calculate quantity-based bulk prices with illustrative GST and delivery, and save quote requests. The Supplier mode lets a shop list products with its required address and map coordinates; a shop photo is optional. Sample shops include locations. Product details, prices, stock, taxes and requests are demo data; orders and payments are not processed.

Phase 7 adds a Construction Tools tab with an illustrative built-up-area and quality-based cost calculator, a sample materials BOQ, and shareable PDF and Excel workbook exports. Quantity factors and rates are estimates only; they are not engineering-certified quantities, supplier quotes or a construction contract.

Listings, service providers, material offers and quote requests, favorites, demo role, enquiries, and notifications are stored locally with AsyncStorage. There is no account or backend synchronization. Expo Go on Android uses its bundled Google Maps key for map display; custom native builds may need `GOOGLE_MAPS_API_KEY` for map tiles.


This is a clean, separate Expo project copy. Start it with `npm install` followed by `npx expo start --tunnel --clear --go`.

APK releases use the user-facing app version in `app.json` (`expo.version`, currently `1.0.0`) and an Android `versionCode` starting at `1`. EAS automatically increments `versionCode` for each `preview` APK build. Increase `expo.version` manually for a user-facing release change (for example, `1.0.0` to `1.1.0`); each build retains its own incremented Android code.

Navigation uses five bottom buttons: Explore, Favorites, Post, Enquiries, and Services. Services opens a simple landing page with three choices: Services, Materials, and Build. Each choice opens its detailed section with a back button. Profile remains available from the top.
