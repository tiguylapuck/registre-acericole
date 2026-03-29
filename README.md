# 🍁 Registre Acéricole — Osmose

Application web open source pour le suivi de la performance des membranes d'osmose inverse en acériculture.

**Application en ligne :** https://tiguylapuck.github.io/registre-acericole/

---

## Fonctionnalités

- **Variables initiales** — Configuration de début de saison : PEP initial à 150 et 175 psi, membranes individuelles, volumes de rinçage
- **Saisie journalière** — Mesures globales et par membrane, calcul automatique PEP et efficacité (%), données de lavage
- **Registre** — Historique complet de la saison avec export Excel et CSV
- **Bilan** — Statistiques de saison et performance par membrane
- **Multi-saisons** — Sélecteur de saison intégré
- **Cloud** — Données synchronisées en temps réel via Supabase (multi-appareils)

## Calculs

- **Facteur de correction (Fc)** — Grille de correction 0–25°C (norme industrie)
- **PEP actuelle** = Débit filtrat ÷ Fc
- **Efficacité (%)** = PEP actuelle ÷ PEP initial × 100
  - 🟢 ≥ 95% — Excellente
  - 🟡 80–95% — Acceptable
  - 🔴 < 80% — Lavage recommandé

## Technologies

- HTML / CSS / JavaScript (vanilla)
- [Supabase](https://supabase.com) — Base de données PostgreSQL cloud
- [SheetJS](https://sheetjs.com) — Export Excel
- Hébergé sur [GitHub Pages](https://pages.github.com)

## Installation locale

```bash
git clone https://github.com/tiguylapuck/registre-acericole.git
cd registre-acericole
# Ouvrir index.html dans un navigateur
```

## Configuration Supabase

1. Créer un projet sur [supabase.com](https://supabase.com)
2. Exécuter le script `supabase_tables.sql` dans l'éditeur SQL
3. Remplacer `SUPABASE_URL` et `SUPABASE_KEY` dans `index.html`

## Déploiement GitHub Pages

```bash
git add .
git commit -m "Mise à jour"
git push origin main
```

L'application est automatiquement déployée sur GitHub Pages.

## Licence

MIT — Libre d'utilisation et de modification.

---

*Développé pour les acériculteurs du Québec 🍁*
