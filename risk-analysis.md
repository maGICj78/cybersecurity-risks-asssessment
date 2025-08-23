# Analyse des Risques (Risk Assessment)

> **Objectif** : Comprendre *où* on peut avoir des problèmes et *dans quel ordre* les traiter.

## 1) Périmètre (ce que l'on protège)
- Données clients (contacts, devis, factures)
- Comptes e‑mail et cloud
- Postes Windows des employés
- Wi‑Fi de l'entreprise
- Téléphones (BYOD : personnels utilisés au travail)

## 2) Actifs, Menaces, Vulnérabilités
**Actif** = ce qui a de la valeur. **Menace** = ce qui peut faire du mal. **Vulnérabilité** = faiblesse.

| Actif                    | Menace                | Vulnérabilité typique                  |
|--------------------------|-----------------------|----------------------------------------|
| Comptes e‑mail           | Phishing              | 2FA désactivée, manque de formation    |
| Fichiers clients (cloud) | Ransomware            | Pas de sauvegarde hors ligne           |
| Postes Windows           | Malware               | Antivirus pas à jour                   |
| Wi‑Fi                    | Intrusion voisins     | Mot de passe faible, vieux chiffrement |
| Comptes employés         | Vol de mot de passe   | Réutilisation de mots de passe         |
| Données sensibles        | Perte/USB             | Ports USB non contrôlés                |
| Téléphones personnels    | Fuite de données      | Pas de verrouillage/MDM                |
| Boîte mail du gérant     | Usurpation/Business Email Compromise | Pas de vérification fournisseur |

## 3) Méthode d'évaluation (très simple)
- **Probabilité** : 1 (très rare) → 5 (très fréquent)
- **Impact** : 1 (faible) → 5 (très fort)
- **Score Risque** = Probabilité × Impact (max 25)
  - 20–25 : **Critique**
  - 12–19 : **Élevé**
  - 6–11  : **Moyen**
  - 1–5   : **Faible**

## 4) Registre des risques (à personnaliser)
| # | Risque (court)                     | Prob. | Impact | Score | Niveau     | Mesure rapide (résumé)                  |
|---|------------------------------------|:-----:|:------:|:-----:|------------|-----------------------------------------|
| 1 | Phishing sur e‑mail                |  5    |   4    |  20   | Critique   | Former + 2FA + filtre anti‑spam         |
| 2 | Ransomware (cloud synchronisé)     |  4    |   5    |  20   | Critique   | Sauvegardes 3‑2‑1 + droits minimaux     |
| 3 | Mots de passe faibles/réutilisés   |  4    |   4    |  16   | Élevé      | Gestionnaire + règles + 2FA             |
| 4 | Wi‑Fi peu sécurisé                 |  3    |   4    |  12   | Élevé      | WPA2/3, mot de passe fort, SSID invité  |
| 5 | Malware (antivirus obsolète)       |  3    |   3    |   9   | Moyen      | Antivirus auto + mises à jour           |
| 6 | Fuite via clé USB                  |  3    |   3    |   9   | Moyen      | Bloquer USB / Politique d'usage         |
| 7 | Téléphones non verrouillés (BYOD)  |  2    |   3    |   6   | Moyen      | Verrouillage + chiffrement              |
| 8 | Usurpation du gérant (BEC)         |  2    |   5    |  10   | Moyen      | Procédure de validation des paiements   |

> Astuce : Modifie les colonnes **Prob.** et **Impact** selon ton contexte, le **Score** se recalcule facilement.

## 5) Priorités (Top 5)
1. Activer **2FA** partout (e‑mail, cloud, banque)
2. Mettre en place des **sauvegardes 3‑2‑1**
3. **Mises à jour auto** (OS, antivirus, navigateurs)
4. **Wi‑Fi** : mot de passe fort, WPA2/3, réseau invité
5. **Formation anti‑phishing** (10 minutes / mois)

## 6) Matrice visuelle
Voir `assets/risk-matrix.png` (Probabilité en Y, Impact en X).

## 7) Annexe – Exemples d'indicateurs (simples)
- % comptes avec 2FA activée
- Âge moyen des mises à jour (jours)
- Nombre de sauvegardes testées avec succès par mois
- % employés passant le quiz phishing
