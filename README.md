XML Schema

Enoncé

Réalisez une grammaire XML Schema pour le document http-ns.xml en vous basant sur la structure du document. 
Aussi, on voudrait : 
utiliser une énumération pour les valeurs de l’attribut « status » de la balise « hd :header »
que l’attribut « name » de la balise « hd:header » ainsi que la balise « hd:RFC » peuvent avoir plusieurs valeurs séparées par des espaces
que l'élément « request-headers » peut être substitué avec « http-request-headers » et l'élément « response-headers » peut être substitué avec « http-response-headers »

Étapes

 Pour réaliser la grammaire de document XML, on va créer deux documents XML Schema :
Un document qui déclare les types des éléments appartenant au namespace hd (http://www.ietf.org/headers/). Ce document ne déclarera que des types (complexes et simples)
La grammaire globale qui va créer la structure de tout le document, et importera la grammaire précédente pour utiliser ses types.
⚠️ Faites attention aux IRIs des namespaces
⚠️ Notez que tout namespace utilisé au sein d'un document devra être déclaré dans la racine avec l'attribut xmlns
ℹ️ L'attribut xml:lang est un attribut spécial qui est standardisé dans l'espace de noms XML (http://www.w3.org/XML/1998/namespace). 
Nul besoin de le recréer, il suffit de le référencer dans la définition de la grammaire avec l'attribut ref. Aussi, il faut déclarer le namespace associé 
au préfixe xml dans la racine et l'importer avec la balise <xs:import>
