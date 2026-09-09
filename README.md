# Meteo România — date publice

Artefactele publice ale sistemului de prognoză cu corecție locală
pentru România (repo-ul de antrenare este privat):

- **`blend_v1.json`** — tabelul de corecție: bias per stație
  (lună × bloc de 3h, UTC) pentru ICON-EU / ECMWF IFS / GFS plus
  ponderile optimizate ale blend-ului. Republicat săptămânal de CI
  după re-antrenare. Aplicația Android îl descarcă automat.
- **`validation.csv`** — validarea la zi pe perioada de test (≥2025,
  date nevăzute la antrenare): RMSE per model brut vs. blend corectat,
  global și per stație.

Măsurat, nu estimat: câmpul `test_rmse` din JSON este RMSE-ul
blend-ului pe datele de test.

Surse: prognoze arhivate [Open-Meteo](https://open-meteo.com/)
(CC BY 4.0), observații [Meteostat](https://meteostat.net/).
