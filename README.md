# test_plugin_selectbyrelationship
test sul plugin sperimentale selectbyrelationship

il database è cosi organizzato:

## tre vettori e una tabella:
+ _plg_aree_quadri_ -- vettore POLYGON che delimita i lampioni alimentati da una fornitura ENEL
+ _pti_pill_ -- vettore POINT che rappresenta la posizione dei lampioni
+ _pti_quadri_ -- vettore POINT che rappresenta la posizione della fornitura ENEL
+ _tabella_arm_ -- semplice tabella ALFANUMERICA che contiene i dati sulle armature

<img src = "https://github.com/pigreco/test_plugin_selectbyrelationship/blob/master/database.jpg" width =300>

## RELAZIONI:
+ PADRE: `pti_pill` FIGLIO: `tabella_arm` : ogni lampione puo' avere più lampade cioè più armature;
+ PADRE: `pti_quadri` FIGLIO: `pti_pill` : ogni quadro alimenta più lampioni;
+ PADRE: `plg_aree_quadri` FIGLIO: `pti_pill` : ogni area delimita i lampioni che sono alimentati dal quadro;

<img src = "https://github.com/pigreco/test_plugin_selectbyrelationship/blob/master/N4.jpg" width =700>

## progetti QGIS:
+ tre progetti con 1,2 e 3 relazioni presenti nel progetto;
+ configurazione standard del plugin: SOLO selezione feature PADRE da selezione record FIGLIO.

## in lavorazione
+ altri progetti con varie configurazioni del plugin
