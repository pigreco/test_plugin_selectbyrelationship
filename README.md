# test_plugin_selectbyrelationship
test sul plugin sperimentale selectbyrelationship

il database è cosi organizzato:

tre vettori e una tabella:
+ plg_aree_qUadri -- vettore POLYGON che delimita i lampioni alimentati da una fornitura ENEL
+ pti_pill -- vettore POINT che rappresenta la posizione dei lampioni
+ pti_quadri -- vettore POINT che rappresenta la posizione della fornitura ENEL
+ tabella_arm -- semplice tabella ALFANUMERICA che contiene i dati sulle armature

<img src = "https://github.com/pigreco/test_plugin_selectbyrelationship/blob/master/database.jpg" width =300>

RELAZIONI:
+ PADRE: pti_pill FIGLIO: tabella_arm : ogni lampione puo' avere più lampade cioè più armature;
+ PADRE: pti_quadri FIGLIO: pti_pill : ogni quadro alimenta più lampioni;
+ PADRE: plg_aree_quadri FIGLIO: pti_pill : ogni area delimita i lampioni che sono alimentati dal quadro;

<img src = "https://github.com/pigreco/test_plugin_selectbyrelationship/blob/master/N4.jpg" width =300>
