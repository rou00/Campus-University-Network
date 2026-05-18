# Campus-University-Network
Campus University Network – Multi-Site VLAN And Routing Lab

Ce projet simule l’infrastructure réseau complète d’un **campus universitaire** avec deux sites :
- **Campus principal** (Main Campus)
- **Campus annexe / distant** (Branch Campus)

L’objectif est de démontrer des compétences en **conception réseau**, **segmentation VLAN**, **routage inter-VLAN**, **routage dynamique RIP v2**, **DHCP**, et **interconnexion de sites**.

## Équipements utilisés

| Équipement | Rôle |
|------------|------|
| router-main-campus | Routeur principal (Router-on-a-stick, DHCP, RIP) |
| router-branch-campus | Routeur distant (sous-interfaces, DHCP, RIP) |
| router-cloud | Simulateur d’opérateur (liaison série) |
| switch-l3-main-compus | Switch d’accès principal (VLANs, trunk) |
| switch-l3-branch-compus | Switch d’accès distant |

## VLANs configurés

### Main campus
| VLAN | Nom |
|------|-----|
| 10 | Admin |
| 20 | RH |
| 30 | Finance |
| 40 | Business |
| 50 | EIC |
| 60 | AID |
| 70 | StudentLab |
| 80 | IT |

### Branch campus
| VLAN | Nom |
|------|-----|
| 90 | Staff |
| 100 | StudentLab |

## Technologies mises en œuvre

-  **802.1Q Trunking** entre switchs et routeurs
-  **Router-on-a-stick** (sous-interfaces GigabitEthernet)
-  **RIP version 2** dynamique entre 3 routeurs
-  **DHCP pools** intégrés aux routeurs par VLAN
-  **Liaisons série point-à-point** (/30)
-  **Spanning Tree PVST+** (par VLAN)
-  **Segmentation réseau** et isolation logique
