# South American mCDR Research Map

## Files
- `index.html`: interactive Leaflet map connected to the published `Map_Public` CSV.

## Publish with GitHub Pages
1. Create a GitHub repository, for example `south-american-mcdr-map`.
2. Upload `index.html` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose branch `main` and folder `/ (root)`, then Save.
6. Wait for GitHub Pages to publish the site. Its URL will appear in the Pages settings.

## Data connection
The map fetches the published `Map_Public` CSV on page load and every 5 minutes.
Keep only public-safe fields in `Map_Public`. The map assumes these column headers:
`record_id, project_id, project_name, country, region, location_name, latitude, longitude, location_precision, research_category, mcdr_approach, research_contribution, ecosystem, short_description, contact_person, contact_role, lead_institution, collaborating_institutions, project_status, project_url, publication_doi, last_verified`

The Google Sheet must remain published as CSV. The map cannot display records without valid latitude and longitude. It does not publish or read the internal `Research_Inventory` tab.
