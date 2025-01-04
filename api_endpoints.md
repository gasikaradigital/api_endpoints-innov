# Liste des API pour le projet ERPINNOV

## **1. Authentification et gestion des utilisateurs**

- `POST /api/register` : Inscription d'un utilisateur.
- `POST /api/login` : Connexion utilisateur.
- `POST /api/logout` : Déconnexion utilisateur.
- `POST /api/forgot-password` : Réinitialisation du mot de passe.
- `POST /api/reset-password` : Réinitialisation du mot de passe via un token.
- `GET /api/user` : Récupérer les informations de l'utilisateur connecté.
- `PUT /api/user/update-profile` : Mise à jour du profil utilisateur.
- `POST /api/user/change-password` : Changer le mot de passe.

---

## **2. Gestion des rôles et permissions**

- `GET /api/roles` : Liste des rôles disponibles (SuperAdmin, Manager, Client).
- `POST /api/roles` : Créer un rôle.
- `GET /api/permissions` : Liste des permissions disponibles.
- `POST /api/roles/assign-permissions` : Assigner des permissions à un rôle.

---

## **3. Gestion des instances Dolibarr**

- `GET /api/instances` : Liste des instances de l'utilisateur.
- `POST /api/instances` : Création d'une nouvelle instance.
- `GET /api/instances/{id}` : Détails d'une instance spécifique.
- `PUT /api/instances/{id}` : Mise à jour des informations d'une instance.
- `DELETE /api/instances/{id}` : Suppression d'une instance.
- `POST /api/instances/{id}/start` : Démarrage d'une instance.
- `POST /api/instances/{id}/stop` : Arrêt d'une instance.
- `POST /api/instances/{id}/renew` : Renouvellement de la période d'essai ou abonnement.

---

## **4. Gestion des abonnements**

- `GET /api/subscriptions` : Liste des abonnements d'un utilisateur.
- `POST /api/subscriptions` : Souscription à un abonnement.
- `GET /api/subscriptions/{id}` : Détails d'un abonnement spécifique.
- `PUT /api/subscriptions/{id}/upgrade` : Mise à niveau de l'abonnement.
- `DELETE /api/subscriptions/{id}` : Annulation d'un abonnement.
- `GET /api/subscriptions/plans` : Liste des plans disponibles.

---

## **5. Gestion de la facturation et des paiements**

- `GET /api/billing/invoices` : Liste des factures de l'utilisateur.
- `GET /api/billing/invoices/{id}` : Télécharger une facture.
- `POST /api/billing/payment` : Effectuer un paiement.
- `POST /api/billing/refund` : Demande de remboursement.

---

## **6. Période d'essai**

- `GET /api/trial` : Vérifier la durée restante de la période d'essai.
- `POST /api/trial/extend` : Extension de la période d'essai (si applicable).

---

## **7. Gestion des notifications**

- `GET /api/notifications` : Liste des notifications pour l'utilisateur connecté.
- `POST /api/notifications/mark-as-read` : Marquer une notification comme lue.
- `DELETE /api/notifications/{id}` : Supprimer une notification.

---

## **8. Gestion des logs et suivi**

- `GET /api/logs/instances/{id}` : Récupérer les logs d'une instance Dolibarr.
- `GET /api/logs/user` : Logs des activités de l'utilisateur connecté.

---

## **9. Gestion des fichiers**

- `POST /api/files/upload` : Upload de fichiers (ex : configuration ou sauvegarde).
- `GET /api/files/download/{id}` : Télécharger un fichier.
- `DELETE /api/files/{id}` : Supprimer un fichier.

---

## **10. Intégration avec Dolibarr**

- `GET /api/dolibarr/{instance_id}/users` : Récupérer la liste des utilisateurs Dolibarr.
- `POST /api/dolibarr/{instance_id}/users` : Ajouter un utilisateur Dolibarr.
- `GET /api/dolibarr/{instance_id}/modules` : Liste des modules activés pour une instance.
- `POST /api/dolibarr/{instance_id}/modules` : Activer/désactiver un module.

---

## **11. Gestion des sous-domaines**

- `GET /api/subdomains` : Liste des sous-domaines utilisés.
- `POST /api/subdomains/validate` : Valider la disponibilité d'un sous-domaine.
- `POST /api/subdomains/update` : Mise à jour du sous-domaine d'une instance.

---

## **12. Tableau de bord (statistiques)**

- `GET /api/dashboard` : Statistiques globales de l'utilisateur.
- `GET /api/dashboard/admin` : Statistiques globales pour SuperAdmin.

---

## **13. API publique (webhooks, intégrations externes)**

- `POST /api/webhooks/dolibarr-events` : Gestion des événements Dolibarr (webhooks).
- `GET /api/webhooks` : Liste des webhooks configurés.
- `POST /api/webhooks` : Ajouter un webhook.
- `DELETE /api/webhooks/{id}` : Supprimer un webhook.

---

## **14. Gestion des essais multiples**

- `GET /api/trial/check` : Vérifier si l'utilisateur est éligible pour une nouvelle période d'essai.
- `POST /api/trial/reset` : Réinitialisation manuelle d'une période d'essai (SuperAdmin uniquement).

---

## **15. Sauvegarde et restauration**

- `POST /api/instances/{id}/backup` : Sauvegarde manuelle d'une instance.
- `POST /api/instances/{id}/restore` : Restauration d'une instance à partir d'une sauvegarde.

---

## **Options spécifiques à l'administration (SuperAdmin)**

- `GET /api/admin/users` : Liste des utilisateurs inscrits.
- `GET /api/admin/instances` : Liste de toutes les instances.
- `GET /api/admin/logs` : Logs système globaux.
- `POST /api/admin/settings` : Mise à jour des paramètres globaux du système.
