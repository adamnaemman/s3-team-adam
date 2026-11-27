# s3-team-adam · Section 3 · Group 02
###### Project Planning : https://canva.link/hatv2g8o8bihmr2
###### Live:

| Matric | Role       | Shop                | Feature                 | Branch                          | Folder                               |
|------- |------------|---------------------|-------------------------|---------------------------------|--------------------------------------|
|2418711 | Setup Lead | Kek Tapak Kuda      | Favourites              | feature-favourites              | src/features/favourites              | 
|2411639 | Member     | Nasi Beriyani Power | Opening Hours           | feature-opening-hours           | src/features/opening-hours           | 
|2412941 | Member     | Kerabu Shack        | Promotions              | feature-promotions              | src/features/promotions              | 
|2416409 | Member     | Warung Selera Kita  | Ratings and Reviews     | feature-ratings-and-reviews      | src/features/rating-and-reviews      | 
|2419467 | Member     | Nasi Kukus          | Allergen and halal info | feature-allergen-and-halal-info | src/features/allergen-and-halal-info | 

## Features
| Feature                   | Problem it solves (who it helps)        | Screen / route    | Firestore data | Offline strategy       |
|---------------------------|-----------------------------------------|-------------------|----------------|------------------------|
| Favourites                | Regular students can bookmark go-to stalls and find them quickly without scanning the full list item                                  | /favourites (and save toogle on /shop/:id)      | users(saved shop IDs) & shops                                     | Cache First            |
| Opening Hours             | Student grabbing meals between classes or later in the evening avoid to a stall that is closed                                        | /shops (stall list) & /shop/:id (stall details) | shops (operating hours/open-closed fields)                  | Stale-While-Revalidate |
| Promotions                | Budget-conscious students can spot active discounts, combos, or deals before deciding what to order                                   | /shops (promo cards/banners) & /shop/:id        | promotions / shops                                                 | Stale-While-Revalidate |
| Ratings and Reviews       | First-time students can gauge food quality and service from peers' feedback before placing an order                                   | /shop/:id (rating & reviews section)            | reviews (and aggregate rating summary on shops if used)            | Stale-While-Revalidate |
| Allergen and halal info   | Students with dietary restrictions, food allergies, or halal requirements can verify item suitability with confidence before ordering | /shop/:id (stall info & menu item details)      | shops / menu items (menuItems or subcollection under shops)        | Stale-While-Revalidate |

## Run it
1. git clone https://github.com/adamnaemman/s3-team-adam && cd s3-team-adam
2. npm install
3. Create .env.local with the VITE_FIREBASE_* keys (from the group chat, never on GitHub)
4. npm run dev

## Test accounts (for the demo; passwords shared privately)
| Role    | Email                   |
|---------|-------------------------|
| Admin   | admin@test.com          | admin1234
| Vendor  | vendor-2418711@test.com |
| Vendor  | vendor-2411639@test.com |
| Vendor  | vendor-2412941@test.com |
| Vendor  | vendor-2416409@test.com |
| Vendor  | vendor-2419467@test.com |
| Student | student@test.com        |

## Tech
React 19 + Vite · React Router · Context API · Firebase Auth, Firestore, Hosting · vite-plugin-pwa (Workbox)

## Releases
- v1.0 (13 Dec): every shop + every feature (screen, data, rule)
- v1.1 (27 Dec): installable, every feature works offline

## AI use
See AI_USAGE.md (each member logs their own entries under their matric).


