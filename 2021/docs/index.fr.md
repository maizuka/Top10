# Introduction

## Bienvenue à l'OWASP Top 10 - 2021

![OWASP Top 10 Logo](./assets/TOP_10_logo_Final_Logo_Colour.png){:class="img-responsive"}

Bienvenue pour cette nouvelle édition de l'OWASP Top 10 ! L'OWASP Top 10 2021 apporte de nombreux changements, avec notamment une nouvelle interface et une nouvelle infographie, disponible sur un format d'une page qu'il est possible de se procurer depuis notre page d'accueil.

Un très grand merci à l'ensemble des personnes qui ont contribué de leur temps et leurs données pour cette itération. Sans vous, cette mouture n'aurait pas vu le jour. **MERCI**.

## Les changements du Top 10 pour 2021

Il y a trois nouvelles catégories, quatre catégories avec un changement de nom et de périmètre, ainsi que des consolidations dans ce Top 10 2021. Nous avons changé les noms si nécessaire pour se concentrer sur la cause plutôt que le symptôme.

![Relations entre le Top 10 2017 et le Top 10 2021](assets/mapping.png)

- **[A01:2021-Contrôles d'accès défaillants](A01_2021-Broken_Access_Control.md)** passe de la cinquième position à celle de catégorie présentant le risque de sécurité le plus sérieux pour une application web ; les données partagées indiquent, qu'en moyenne, 3,81% des applications testées avaient une ou plusieurs *Common Weakness Enumeration* (CWEs) avec plus de 318k occurrences de CWEs de cette catégorie. Les 34 CWEs associées ont eu plus d'occurrences dans les applications auditées que n'importe quelle autre catégorie.
- **[A02:2021-Défaillances cryptographiques](A02_2021-Cryptographic_Failures.md)** gagne une position et prend la deuxième place, précédemment connue sous le nom de **A3:2017-Exposition de données sensibles**, qui était un symptôme large plutôt qu'une cause principale. L'accent est mis sur des défaillances liées à la cryptographie, ce qui était le cas implicitement auparavant. Cette catégorie entraîne souvent une exposition de données sensibles ou une compromission de système.
- **[A03:2021-Injection](A03_2021-Injection.md)** glisse à la troisième position. 94% des applications ont été testées sur des vulnérabilités de ce type, avec une incidence maximale de 19% et une incidence moyenne de 3,37%. Les 33 CWEs associées à cette catégorie ont eu le deuxième plus grand nombre d'occurrences. *Cross-Site Scripting* fait désormais partie de cette catégorie dans cette édition.
- **[A04:2021-Conception non sécurisée](A04_2021-Insecure_Design.md)** est une nouvelle catégorie, avec un accent sur les défauts de conception. Si nous voulons ajouter des contrôles en amont, nous avons besoin de modèles de menaces, de modèles et principes de conception sécurisés, et d'architectures de référence. Une conception non sécurisée ne peut pas être corrigé par une implémentation parfaite car, par définition, les contrôles de sécurité nécessaires pour se défendre contre certaines attaques n'ont jamais été créés.
- **[A05:2021-Mauvaise configuration de sécurité](A05_2021-Security_Misconfiguration.md)** gagne une place ; 90% des applications ont été testées sur des vulnérabilités de ce type, avec une incidence moyenne de 4,5% et plus de 208k occurrences des CWEs associées. Avec des logiciels de plus en plus paramétrables, il n'est pas surprenant de voir cette catégorie prendre de l'ampleur. L'ancienne catégorie **A4:2017-XML Entités externes (XXE)** est incluse dans celle-ci.
- **[A06:2021-Composants vulnérables et obsolètes](A06_2021-Vulnerable_and_Outdated_Components.md)** était précédemment nommée *Utilisation de Composants avec des Vulnérabilités Connues*. Elle se place deuxième de l'enquête auprès de la communauté du Top 10, mais pouvait également entrer dans le Top 10 via l'analyse de données. Cette catégorie progresse depuis sa neuvième place en 2017, elle est un problème connu dont nous avons du mal à tester et à mesurer les risques. Il s'agit de la seule catégorie à n'avoir aucunes *Common Vulnerability and Exposures* (CVEs) associées aux CWEs concernées, en conséquence les coefficients d'impact et de poids ont été renseignés à 5.0 par défaut.
- **[A07:2021-Identification et authentification de mauvaise qualité](A07_2021-Identification_and_Authentication_Failures.md)** était précédemment *Authentification de mauvaise qualité*, elle perd la deuxième place. Elle inclut désormais des CWEs également liées aux échecs d'identification. Cette catégorie est toujours présente dans le Top 10, mais la mise à disposition croissante de frameworks standardisés semble aider.
- **[A08:2021-Manque d'intégrité des données et du logiciel](A08_2021-Software_and_Data_Integrity_Failures.md)** est une nouvelle catégorie, se concentrant sur la formulation d'hypothèses sur les mises à jour logicielles, les données critiques et les pipelines CI/CD sans vérifier leur intégrité. L'un des impacts les plus élevés à partir des données de *Common Vulnerability and Exposures/Common Vulnerability Scoring System* (CVE/CVSS) associées aux 10 CWEs de cette catégorie. **A8:2017-Désérialisation non sécurisée**, listée en 2017, est désormais partie intégrante de cette catégorie.
- **[A09:2021-Carence des systèmes de contrôle et de journalisation](A09_2021-Security_Logging_and_Monitoring_Failures.md)**, précédemment **A10:2017-Supervision et Journalisation Insuffisantes**, est ajoutée de l'enquête auprès de l'industrie (3ème), précédemment à la dixième place. Cette catégorie a été étendue pour inclure plus de types de défaillances, est difficile à tester et est dès lors mal représentée dans les données CVE/CVSS. Toutefois, des incidents dans cette catégorie peuvent impacter directement la visibilité, la levée d'alertes et l'analyse forensique.
- **[A10:2021-Falsification de requête côté serveur](A10_2021-Server-Side_Request_Forgery_(SSRF).md)** provient de l'enquête auprès de la communauté Top 10 (1ère). Les données montrent une incidence faible, avec un taux de couverture des tests supérieur à la moyenne, accompagné de notes de potentiel d'exploitabilité et d'impact supérieur à la moyenne. Cette catégorie est un exemple où les membres de la communauté sécurité nous indiquent que cette catégorie est importante, même si cela ne transparaît pas encore dans les données.

## Méthodologie

Cette version du Top 10 est bien plus basée sur des données que les précédentes, mais elle n'est pas pour autant aveuglée par celles-ci. Parmi les dix catégories, huit proviennent des données fournies et les deux dernières proviennent d'une enquête à haut niveau auprès de la communauté. Nous faisons ceci pour une raison fondamentale, observer les données consiste à observer le passé. Les chercheurs en sécurité s'investissent pour trouver de nouvelles vulnérabilités et de nouveaux moyens pour les détecter. Un temps certain est nécessaire pour intégrer ces tests au sein des outils et des processus. Au moment où nous pouvons tester ces vulnérabilités à l'échelle, des années se sont bien souvent écoulées. Pour équilibrer cette approche, nous avons utilisé une enquête communautaire pour demander aux experts en sécurité applicative et en développement, en première ligne, ce qu'ils constatent comme failles essentielles, que les données pourraient ne pas encore montrer.

Nous avons adopté quelques changements importants pour continuer à faire mûrir le Top 10.

## Comment les catégories sont structurées

Quelques catégories ont changé depuis la précédente édition de l'OWASP Top Ten. Voici ici un bref résumé des changements.

Les précédentes collectes de données étaient concentrés sur un sous ensemble d'approximativement 30 CWEs accompagnées d'un champ demandant des découvertes complémentaires. Nous avons appris que les organisations se concentraient sur les seules 30 CWEs et n'ajoutaient que rarement d'autres CWEs qu'elles rencontraient. Dans cette édition, nous nous sommes contentés de demander des données, sans aucune restriction sur les CWEs. Nous avons demandé le nombre d'applications testées pour une année donnée (à partir de 2017), et le nombre d'applications avec au moins une instance d'une CWE trouvée lors des tests. Ce format nous permet de déterminer la prévalence de chaque CWE au sein des applications. Nous ignorons la fréquence pour nos besoins ; bien que cela pourrait être nécessaire dans d'autres situations, cela cache la prévalence au sein du panel. Qu'une application ait quatre instances d'une CWE ou 4 000 ne fait pas partie du calcul du Top 10. Nous sommes passés d'approximativement 30 CWEs à près de 400 CWEs à analyser dans le jeu de données. Nous prévoyons d'ajouter des analyses complémentaires dans le futur. Cette augmentation significative dans le nombre de CWEs nécessite des changements dans la façon dont les catégories sont structurées.

Nous avons passé plusieurs mois à regrouper et catégoriser les CWEs. Nous aurions pu continuer encore pendant des mois. Nous avons dû nous arrêter à un moment donné. Il existe à la fois des CWEs de type *cause racine* et *symptôme*, où les types *cause racine* sont de la forme "Défaillances cryptographiques" et "Mauvaise configuration", en contraste avec les types *symptôme* tels que "Exposition de données sensibles" et "Déni de service". Nous avons décidé de nous concentrer sur les types *cause racine* autant que possible car ils sont plus logiques pour fournir des conseils d'identification et de remédiation. Se concentrer sur la *cause racine* plutôt que le *symptôme* n'est pas un concept nouveau ; le Top 10 a été un mélange de *symptômes* et de *causes racines*. Les CWEs le sont également ; nous faisons ce choix délibérément et lançons un appel à ce sujet. Il y a une moyenne de 19,6 CWEs par catégorie dans cette édition, avec un minimum d'1 CWE pour **A10:2021-Falsification de requête côté serveur** et un maximum de 40 CWEs pour **A04:2021-Conception non sécurisée**. Cette nouvelle organisation de catégories apporte des avantages pour les formations, les sociétés peuvent se concentrer sur les CWEs les plus pertinentes pour un langage ou un framework.

## Comment les données ont été utilisées pour sélectionner les catégories

En 2017, nous avons sélectionné les catégories à partir du taux d'incidence pour déterminer la probabilité, puis les avons classées via des discussions en équipe basées sur des décennies d'expérience sur des critères d'*Exploitabilité*, *Détectabilité* (également *probabilité*) et *Impact technique*. Pour 2021, nous souhaitons, si possible, utiliser des données pour *Exploitabilité* et *Impact (technique)*.

Nous avons téléchargé OWASP Dependency Check et extrait les scores CVSS d'exploitabilité et d'impact agrégés par CWE connexes. Cela a nécessité un temps de recherche significatif, car toutes les CVEs ont un score CVSSv2, mais celui-ci possède des défauts que CVSSv3 devrait corriger. Après un certain temps, toutes les CVEs reçoivent également un score CVSSv3. De plus, les plages de notation et les formules ont été mises-à-jour entre CVSSv2 et CVSSv3.

En CVSSv2, *Exploitabilité* et *Impact (technique)* peuvent atteindre 10, mais la formule les ramène à 60&nbsp;% pour *Exploitabilité* et 40&nbsp;% pour *Impact*. En CVSSv3, le maximum théorique est limité à 6,0 pour *Exploitabilité* et 4,0 pour *Impact*. Avec la pondération prise en compte, le score d'impact a augmenté, de près d'un point et demi en moyenne dans CVSSv3, et l'exploitabilité a baissé de près d'un demi-point en moyenne.

Il y a 125&nbsp;000 enregistrements d'une CVE associée à une CWE dans les données de la National Vunerability Database (NVD) extraites d'OWASP Dependency Check, et il y a 241 CWE uniques associées à une CVE. 62&nbsp;000 enregistrements ont un score CVSSv3, ce qui représente environ la moitié des données.

Pour le Top Ten 2021, nous avons calculé les scores moyens d'*exploitabilité* et d'*impact* de la manière suivante. Nous avons regroupé toutes les CVEs avec des scores CVSS par CWE et pondéré à la fois *exploitabilité* et *impact* notés par le pourcentage de la population qui disposait d'un score CVSSv3, plus la population restante de scores CVSSv2 pour obtenir une moyenne globale. Nous avons associé ces moyennes aux CWEs de l'ensemble de données à utiliser comme notes d'*Exploitabilité* et d'*Impact (technique)* pour l'autre moitié de l'équation de risque.

## Pourquoi ne pas se reposer uniquement sur des données statistiques ?

Les résultats obtenus à partir des données sont principalement limités à ce que nous pouvons tester de manière automatisée. Parlez à un professionnel chevronné de la sécurité, il vous parlera de ce qu'il trouve et des tendances qu'il observe qui ne sont pas encore dans les données. Il faut du temps aux gens pour développer des méthodologies de test pour certains types de vulnérabilités, puis plus de temps pour que ces tests soient automatisés et exécutés sur un grand nombre d'applications. Tout ce que nous trouvons sont des vestiges du passé qui pourraient manquer les tendances de l'année écoulée, qui ne sont pas présentes dans les données.

Par conséquent, nous ne sélectionnons que huit catégories sur dix à partir des données, car elles sont incomplètes. Les deux autres catégories proviennent de l'enquête communautaire Top 10. Cela permet aux praticiens en première ligne de voter pour ce qu'ils considèrent comme les risques les plus élevés qui pourraient ne pas être représentés par les données (et qui pourraient ne jamais être exprimés par les données).

## Pourquoi le taux d'incidence au lieu de la fréquence ?

Il y a trois sources principales de données. Nous les identifions comme étant l'outillage assisté par l'homme (OaH), l'homme assisté par l'outil (HaO) et l'outillage brut.

L'outillage et l'OaH sont des générateurs de recherche à haute fréquence. Les outils cherchent des vulnérabilités spécifiques, tentent inlassablement de trouver chaque instance de cette vulnérabilité et génèrent un nombre élevé de découvertes pour certains types de vulnérabilité. Prenez *Cross-Site Scripting*, qui est généralement l'une de ces deux variantes : il s'agit soit d'une erreur mineure et isolée, soit d'un problème systémique. Lorsqu'il s'agit d'un problème systémique, le nombre de constations peut se chiffrer par milliers pour une seule application. Cette fréquence élevée noie la plupart des autres vulnérabilités trouvées dans les rapports ou les données.

L'HaO, d'autre part, trouvera une gamme plus large de types de vulnérabilités mais à une fréquence beaucoup plus faible en raison de contraintes de temps. Lorsque les humains testent une application et détectent une vulnérabilité comme *Cross-Site Scripting*, ils trouveront généralement trois ou quatre instances et s'arrêteront. Ils peuvent déterminer une découverte systémique et la rédiger avec une recommandation à corriger à l'échelle de l'application. Il n'y a pas de besoin (ou de temps) de trouver chaque instance.

Supposons que nous prenions ces deux ensembles de données distincts et essayions de les fusionner en se basant sur la fréquence. Dans ce cas, les données d'outillage et d'OaH noieront les données HaO plus précises (mais plus larges) et expliquent en grande partie pourquoi une catégorie comme *Cross-Site Scripting* a été si bien classée dans de nombreuses listes alors que l'impact est généralement faible à modéré. C'est à cause du volume considérable de résultats. Le *Cross-Site Scripting* est également assez facile à tester, il y a donc beaucoup plus de tests pour cela.

En 2017, nous avons introduit le taux d'incidence pour jeter un nouveau regard sur les données et fusionner proprement les données d'outillage et d'OaH avec les données d'HaO. Le taux d'incidence demande quel pourcentage de la population d'applications avait au moins une instance d'un type de vulnérabilité. Peu nous importe si c'était ponctuel ou systémique. Ce n'est pas pertinent pour nos fins ; nous avons seulement besoin de savoir combien d'applications ont eu au moins une instance, ce qui permet de fournir une vue plus claire des résultats des tests sur plusieurs types de tests sans noyer les données dans des résultats à haute fréquence. Cela correspond à une vue liée au risque, car un attaquant n'a besoin que d'une seule instance pour attaquer une application avec succès via la catégorie.

## What is your data collection and analysis process?

We formalized the OWASP Top 10 data collection process at the Open Security Summit in 2017. OWASP Top 10 leaders and the community spent two days working out formalizing a transparent data collection process. The 2021 edition is the second time we have used this methodology.

We publish a call for data through social media channels available to us, both project and OWASP. On the OWASP Project page, we list the data elements and structure we are looking for and how to submit them. In the GitHub project, we have example files that serve as templates. We work with organizations as needed to help figure out the structure and mapping to CWEs.

We get data from organizations that are testing vendors by trade, bug bounty vendors, and organizations that contribute internal testing data. Once we have the data, we load it together and run a fundamental analysis of what CWEs map to risk categories. There is overlap between some CWEs, and others are very closely related (ex. Cryptographic vulnerabilities). Any decisions related to the raw data submitted are documented and published to be open and transparent with how we normalized the data.

We look at the eight categories with the highest incidence rates for inclusion in the Top 10. We also look at the Top 10 community survey results to see which ones may already be present in the data. The top two votes that aren't already present in the data will be selected for the other two places in the Top 10. Once all ten were selected, we applied generalized factors for exploitability and impact; to help rank the Top 10 2021 in a risk based order.

## Data Factors

There are data factors that are listed for each of the Top 10 Categories, here is what they mean:

- CWEs Mapped: The number of CWEs mapped to a category by the Top 10 team.
- Incidence Rate: Incidence rate is the percentage of applications vulnerable to that CWE from the population tested by that org for that year.
- (Testing) Coverage: The percentage of applications tested by all organizations for a given CWE.
- Weighted Exploit: The Exploit sub-score from CVSSv2 and CVSSv3 scores assigned to CVEs mapped to CWEs, normalized, and placed on a 10pt scale.
- Weighted Impact: The Impact sub-score from CVSSv2 and CVSSv3 scores assigned to CVEs mapped to CWEs, normalized, and placed on a 10pt scale.
- Total Occurrences: Total number of applications found to have the CWEs mapped to a category.
- Total CVEs: Total number of CVEs in the NVD DB that were mapped to the CWEs mapped to a category.

## Thank you to our data contributors

The following organizations (along with some anonymous donors) kindly donated data for over 500,000 applications to make this the largest and most comprehensive application security data set. Without you, this would not be possible.

- AppSec Labs
- Cobalt.io
- Contrast Security
- GitLab
- HackerOne
- HCL Technologies
- Micro Focus
- PenTest-Tools
- Probely
- Sqreen
- Veracode
- WhiteHat (NTT)

## Thank you to our sponsor

The OWASP Top 10 2021 team gratefully acknowledge the financial support of Secure Code Warrior and Just Eat.

[![Secure Code Warrior](assets/securecodewarrior.png){ width="256" }](https://securecodewarrior.com)    

[![Just Eats](assets/JustEat.png){ width="256" }](https://www.just-eat.co.uk/)
