# liste-prenoms-nouveaux-nes
Spécification de la liste annuelle des prénoms des nouveaux-nés en France.

La liste annuelle des prénoms des nouveaux-nés est un jeu de données simple et très apprécié du public. Il consiste en une liste de prénoms avec l'occurrence de chacun pour une année donnée. Les prénoms listés correspondent au premier prénom donné dans chaque acte de naissance de l'état-civil.

Ce schéma décrit le détail de chaque champ. Pour chacun, nous fournissons également l'expression rationnelle informatique (ou "regexp") qui permet de contrôler le contenu du champ.

## Origine du standard
Ce standard a tout d'abord été élaboré à partir du recueil et de l'observation des fichiers produits en open data par plusieurs communes françaises, publiés dès 2012. Il s'est nourri de l'observation des usages et a puisé également dans les textes de lois ou textes de référence qui standardisent la forme des prénoms en français.

### Textes de loi et de référence
* Le code civil : https://www.legifrance.gouv.fr/affichCode.do?cidTexte=LEGITEXT000006070721&dateTexte=20170327
* L'encyclopédie Wikipedia synthétise les instructions générales relatives à l'état-civil : https://fr.wikipedia.org/wiki/Instruction_g%C3%A9n%C3%A9rale_relative_%C3%A0_l%27%C3%A9tat_civil ; notamment les deux textes suivants, qui précisent ce qui possible ou non en matière de prénom :
  * Circulaire du 28 octobre 2011 relative aux règles particulières à divers actes de l'état civil relatifs à la naissance et à la filiation — NOR : JUSC1119808C : http://www.textes.justice.gouv.fr/art_pix/JUSC1119808C.pdf
  * Circulaire du 23 juillet 2014 relative à l’état civil — NOR : JUSC1412888C : http://circulaire.legifrance.gouv.fr/pdf/2014/07/cir_38565.pdf
* Normes techniques de l'INSEE : http://xml.insee.fr/schema/etat-civil/ ; ce texte spécifie notamment très clairement : "*Les caractères acceptés pour l’écriture du ou des prénom(s) sont : Pour la 1ère lettre : - les 26 lettres de l’alphabet utilisées dans la langue française en majuscules, - 15 lettres avec signes diacritiques en majuscules (À Â Ä Ç É È Ê Ë Î Ï Ô Ö Ù Û Ü), - 2 ligatures en majuscules (Æ Œ). Pour les suivantes : - les 26 lettres de l’alphabet utilisées dans la langue française en minuscules, - 15 lettres avec signes diacritiques en minuscules (à â ä ç é è ê ë î ï ô ö ù û ü), - 2 ligatures en minuscules (æ, œ) - l’apostrophe, le tiret sans espace avant et après (obligatoire pour les prénoms composés)*"

## Schéma au format Table Schema
Table Schema est une sorte de "dictionnaire de données" qui permet de valider automatiquement un fichier CSV. Il offre donc une spécification précise du fichier. Il permet également de documenter le format d'un fichier. Il s'agit d'un fichier au format JSON. La spécification de la liste annuelle des prénoms des nouveaux-nés est établie sous cette forme :
https://github.com/CharlesNepote/liste-prenoms-nouveaux-nes/blob/v0.7beta/prenom-schema.json

## Exemple de fichiers CSV
* Exemple compatible avec la version v0.7beta : https://gist.githubusercontent.com/CharlesNepote/94983541b2ca3e84f29b616d1ffa29fa/raw/674351f4b41ed0b581099378d38071c7a8dd711d/prenom.csv

## Historique
* 2018-01-19 : rétro-publication des versions 0.5beta et 0.7beta sur Github, afin de garder un historique des modifications et une URL plus pérenne
* 2017-11-29 : publication par la Ville de Digne-les-Bains d'une première version compatible avec la version 1.0 (beta) du Socle commun des données locales , source : https://twitter.com/mairiedigne/status/935878333174370305
* 2017-06-13 : publication d'une version "1.0 (beta)" sur le Socle commun des données locales d'Opendata Locale, sous le titre "Liste annuelle des prénoms des nouveaux-nés déclarés à l’état-civil"
  * version remaniée de la 0.5beta : outre quelques changements cosmétiques, les noms des colonnes ont complètement changé : http://opendatalocale.net/presentation-de-chaque-jeu-et-de-sa-normalisation-precise/
  * le document est un Google doc à cette adresse : https://www.google.com/url?q=https://docs.google.com/document/d/1Vk0kpBw3MIocai9JqovLK2HxcUA_3QHnZicqxuOpcQ8/edit&sa=D&ust=1516378130800000&usg=AFQjCNGOhVG26wYL6cx5ApGeJWqed4YzQA
* 2017-04-26 : v0.7beta ([diff](https://github.com/CharlesNepote/liste-prenoms-nouveaux-nes/commit/9a9a4963513e888bc7e7b86e54f4f3c830fda025#diff-ef3b39c9e34d1e422e98be05e0d9f2a3))
* 2017-03-26 : v0.5beta
* 2017-03 : premières versions non publiées.
