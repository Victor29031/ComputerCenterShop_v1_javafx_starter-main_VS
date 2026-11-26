# ComputerCenterShop — pràctica integradora RA2

> **Plantilla de l'equip.** Copieu aquest fitxer al vostre repositori de treball i completeu-lo a mesura que avanceu. No inclou solucions de codi: les decisions, proves i explicacions han de ser vostres.

## Fitxa de l'equip

- Integrants: **Sebastian Alarcon** i **Victor Sol**
- Repositori compartit: **https://github.com/Victor29031/ComputerCenterShop_v1_javafx_starter-main_VS**
- Branca de treball habitual: **main_sebas**
- Data d'inici: **11/19/2026**
- Última actualització: **[AAAA-MM-DD]**

## Propòsit del projecte

En aquesta pràctica desenvolupem una aplicació Java que accedeix a una base de dades relacional amb JDBC. Treballem sobre el projecte *starter* indicat pel professorat i fem servir el backlog RA2 per organitzar les tasques, els commits, les proves i les decisions tècniques.

El repositori ha de mostrar el procés de treball real de l'equip. No es tracta només d'arribar a una aplicació que s'executi: també cal poder explicar què s'ha canviat, com s'ha comprovat i per què la decisió correspon a cada *issue*.

## Punt de partida

- Repositori *starter* utilitzat: **[URL o nom del repositori]**
- Gestor de base de dades relacional utilitzat: **[indiqueu-lo]**
- Connector utilitzat: **[indiqueu-lo]**
- Entorn de desenvolupament: **[indiqueu-lo]**
- Comandament o acció que fem servir per comprovar l'execució: **[completeu-lo]**

> No incorporeu ORM, Hibernate, ObjectDB, MongoDB, serveis externs ni persistència principal en fitxers. Aquests elements no formen part de RA2.

## Com treballem cada *issue*

1. Llegim l'objectiu i els criteris d'acceptació de l'*issue*.
2. Acordem què ha de canviar i qui inicia la feina.
3. Fem canvis petits i comprensibles, amb *commits* que expliquin la decisió.
4. Provem el comportament esperat i en guardem una evidència.
5. Actualitzem aquest README amb el resultat, la prova i l'enllaç al *commit* o a la *pull request*.
6. Tanquem l'*issue* només quan l'equip pot explicar individualment la solució aplicada.

## Progrés del backlog

Marqueu una tasca quan la prova i el rastre al repositori estiguin recollits. Els enllaços apunten a l'enunciat, no a una solució.

### M1 · Base JDBC operativa

- [ ] [RA2-ISSUE-01 · Preparar el projecte JDBC](issues/RA2-ISSUE-01-preparar-projecte-jdbc.md)
- [ ] [RA2-ISSUE-02 · Connector, URL i connexió](issues/RA2-ISSUE-02-revisar-connector-url-connexio.md)
- [ ] [RA2-ISSUE-03 · Estructura relacional](issues/RA2-ISSUE-03-crear-estructura-relacional.md)

### M2 · Operacions relacionals principals

- [ ] [RA2-ISSUE-04 · Inserció de dades](issues/RA2-ISSUE-04-inserir-producte-preparedstatement.md)
- [ ] [RA2-ISSUE-05 · Actualització d'estoc](issues/RA2-ISSUE-05-actualitzar-estoc.md)
- [ ] [RA2-ISSUE-06 · Eliminació controlada](issues/RA2-ISSUE-06-eliminar-producte-controlat.md)
- [ ] [RA2-ISSUE-07 · Consultes i resultats](issues/RA2-ISSUE-07-consultar-inventari-resultset.md)

### M3 · Robustesa JDBC

- [ ] [RA2-ISSUE-08 · Tancament de recursos](issues/RA2-ISSUE-08-tancar-recursos.md)
- [ ] [RA2-ISSUE-09 · Transaccions](issues/RA2-ISSUE-09-transaccio-commit-rollback.md)
- [ ] [RA2-ISSUE-10 · Procediment amb paràmetres](issues/RA2-ISSUE-10-procediment-parametres.md)
- [ ] [RA2-ISSUE-11 · Errors de connexió i operacions](issues/RA2-ISSUE-11-errors-connexio-recursos.md)

### M4 · Documentació i tancament

- [ ] [RA2-ISSUE-12 · Documentar l'execució i la configuració](issues/RA2-ISSUE-12-documentar-execucio-configuracio.md)
- [ ] [RA2-ISSUE-13 · Preparar el lliurament de la pràctica](issues/RA2-ISSUE-13-lliurament-practica-integradora.md)

## Registre de treball

Dupliqueu aquest bloc per a cada *issue* que completeu. Escriviu amb les vostres paraules i enllaceu només proves i *commits* del vostre repositori.

### RA2-ISSUE-01 · Preparacio del projecte

- Estat: comprovat
- Persona que l'ha iniciat: Sebastian Alarcon.
- Problema inicial: Calia preparar el projecte inicial per poder començar a treballar amb Java, Maven i JavaFX.
- Decisió aplicada: He treballat amb el projecte inicial proporcionat pel professor i treballar-hi amb Eclipse i Maven.
- Canvis fets: Preparació i revisió de l'estructura del projecte i de la configuració necessària per executar-lo.
- Prova realitzada: Compilació i execució del projecte per comprovar que s'inicia correctament.
- Evidència: https://github.com/Victor29031/ComputerCenterShop_v1_javafx_starter-main_VS/issues/2#issuecomment-7014656985
- Commit o pull request: 
- Explicació individual: L'objectiu era preparar el projecte per poder desenvolupar les següents tasques.
- Ús d'IA: Hem utilitzat ChatGPT com a suport per entendre el projecte i revisar els passos de preparació.

### RA2-ISSUE-02 · Connectar, URL i connexio

- Estat: comprovat 
- Persona que l'ha iniciat: Sebastian Alarcon.
- Problema inicial: Faltava implementar la connexió amb la base de dades mitjançant JDBC.
- Decisió aplicada: Utilitzar `DriverManager.getConnection()` per connectar amb la base de dades H2, fent servir la URL, l'usuari i la contrasenya configurats.
- Canvis fets: Modificació del mètode `connect()` de `ProductDaoImplJDBC.java`.
- Prova realitzada: Execució de l'aplicació des d'Eclipse i comprovació de la connexió amb la base de dades H2.
- Evidència: https://github.com/Victor29031/ComputerCenterShop_v1_javafx_starter-main_VS/issues/1#issuecomment-7015071484
- Commit o pull request: 
- Explicació individual: El mètode `connect()` utilitza `DriverManager.getConnection()` i guarda la connexió a la variable `conn`.
- Ús d'IA: Hem utilitzat ChatGPT com a suport per entendre la connexió JDBC i revisar el codi.

### RA2-ISSUE-03 · Estructura relacional

- Estat: comprovat 
- Persona que l'ha iniciat: Sebastian Alarcon.
- Problema inicial: Faltava crear l'estructura de la base de dades i afegir les dades inicials.
- Decisió aplicada: Crear les taules mitjançant instruccions SQL i utilitzar `Statement` amb `try-with-resources`.
- Canvis fets: Implementació del mètode `initSchema()` a `ProductDaoImplJDBC.java`. També s'han fet ajustos a `ShopView.fxml` i `ShopController`.
- Prova realitzada: Execució de l'aplicació i comprovació de la inicialització de la base de dades H2.
- Evidència: https://github.com/Victor29031/ComputerCenterShop_v1_javafx_starter-main_VS/issues/3#issuecomment-7016990912
- Commit o pull request:
- Explicació individual: El mètode crea les taules `products` i `inventory_history`, estableix la clau forana, crea l'àlies `STOCK_ALERT_LIMIT` i insereix productes inicials si la taula està buida.
- Ús d'IA: Hem utilitzat ChatGPT com a suport per entendre les instruccions SQL i revisar la implementació. 

### RA2-ISSUE-04 · Implementar insercio amb PreparedStatement

- Estat: comprovat.
- Persona que l'ha iniciat: Sebastian Alarcon.
- Problema inicial: Faltava implementar la inserció de productes a la base de dades mitjançant JDBC.
- Decisió aplicada: Utilitzar `PreparedStatement` amb una sentència SQL parametritzada per inserir els productes.
- Canvis fets: Implementació del mètode `insertProduct(Product product)` a `ProductDaoImplJDBC.java`.
- Prova realitzada: S'ha provat la inserció d'un producte i s'ha comprovat que apareix correctament en una consulta posterior.
- Evidència: https://github.com/Victor29031/ComputerCenterShop_v1_javafx_starter-main_VS/issues/5#issuecomment-7196966008
- Commit o pull request: 
- Explicació individual: El mètode utilitza `PreparedStatement` per assignar el nom, el preu majorista, la disponibilitat i l'estoc. Després executa la inserció i retorna el nombre de files afectades.
- Ús d'IA: Hem utilitzat ChatGPT com a suport per entendre el funcionament de `PreparedStatement` i revisar la implementació. 

### RA2-ISSUE-05 · Implementar actualitzacio d'estoc

- Estat: comprovat.
- Persona que l'ha iniciat: Sebastian Alarcon.
- Problema inicial: Faltava implementar l'actualització de l'estoc dels productes a la base de dades.
- Decisió aplicada: Utilitzar `PreparedStatement` amb una sentència SQL `UPDATE` per modificar l'estoc i la disponibilitat.
- Canvis fets: Implementació del mètode `updateStock(String name, int newStock)` a `ProductDaoImplJDBC.java`.
- Prova realitzada: Hem modificat l'estoc del producte Mouse de 25 a 0 i s'ha comprovat que la disponibilitat ha canviat de `true` a `false`.
- Evidència: https://github.com/Victor29031/ComputerCenterShop_v1_javafx_starter-main_VS/issues/6#issuecomment-7199441276
- Commit o pull request: 
- Explicació individual: El mètode utilitza `PreparedStatement` per actualitzar el stock, canviar la disponibilitat segons les unitats disponibles i retornar les files afectades.
- Ús d'IA: Hem utilitzat ChatGPT com a suport per entendre el funcionament de `PreparedStatement` i les sentències SQL `UPDATE`.

## Proves que hem de poder repetir

| Cas que comprovem | Dades o condicions inicials | Resultat observat | Evidència |
| --- | --- | --- | --- |
| Arrencada del projecte | **[completeu]** | **[completeu]** | **[enllaç]** |
| Operació de modificació | **[completeu]** | **[completeu]** | **[enllaç]** |
| Consulta de dades | **[completeu]** | **[completeu]** | **[enllaç]** |
| Cas d'error controlat | **[completeu]** | **[completeu]** | **[enllaç]** |
| Operació agrupada o transacció | **[completeu]** | **[completeu]** | **[enllaç]** |

## Decisions i dubtes de l'equip

| Data | *Issue* | Decisió o dubte | Com s'ha resolt | Referència |
| --- | --- | --- | --- | --- |
| **[AAAA-MM-DD]** | **[RA2-ISSUE-XX]** | **[completeu]** | **[completeu]** | **[enllaç]** |

## Ús responsable d'IA

El nivell previst és **IA-1**: podeu usar eines d'IA com a suport per entendre conceptes, formular hipòtesis o revisar una explicació. No substitueixen les proves del projecte ni l'explicació individual.

Si n'heu fet ús, anoteu a l'*issue* corresponent què heu preguntat, què heu contrastat amb el projecte i quina decisió final heu pres. No enganxeu una resposta d'IA com si fos una prova de funcionament.

## Abans de donar la pràctica per preparada

- [ ] Els *issues* P0 tenen un resultat comprovat o una incidència explicada.
- [ ] El repositori conté *commits* que permeten seguir el treball de l'equip.
- [ ] Les proves de funcionament tenen evidències enllaçades.
- [ ] Les decisions sobre connector, consultes, recursos, transaccions i procediments estan explicades amb paraules pròpies.
- [ ] Tots dos integrants poden defensar individualment les decisions tècniques del repositori.
- [ ] El README no inclou solucions copiades ni contingut fora de l'abast de RA2.

---

*Aquesta plantilla és un suport per documentar el treball. El que acredita el procés és el repositori de l'equip, amb els seus canvis, proves, decisions i explicacions.*# ComputerCenterShop — pràctica integradora RA2

> **Plantilla de l'equip.** Copieu aquest fitxer al vostre repositori de treball i completeu-lo a mesura que avanceu. No inclou solucions de codi: les decisions, proves i explicacions han de ser vostres.

## Fitxa de l'equip

- Integrants: **[nom i cognoms]** i **[nom i cognoms]**
- Repositori compartit: **[URL del repositori]**
- Branca de treball habitual: **[nom de la branca]**
- Data d'inici: **[AAAA-MM-DD]**
- Última actualització: **[AAAA-MM-DD]**

## Propòsit del projecte

En aquesta pràctica desenvolupem una aplicació Java que accedeix a una base de dades relacional amb JDBC. Treballem sobre el projecte *starter* indicat pel professorat i fem servir el backlog RA2 per organitzar les tasques, els commits, les proves i les decisions tècniques.

El repositori ha de mostrar el procés de treball real de l'equip. No es tracta només d'arribar a una aplicació que s'executi: també cal poder explicar què s'ha canviat, com s'ha comprovat i per què la decisió correspon a cada *issue*.

## Punt de partida

- Repositori *starter* utilitzat: **[URL o nom del repositori]**
- Gestor de base de dades relacional utilitzat: **[indiqueu-lo]**
- Connector utilitzat: **[indiqueu-lo]**
- Entorn de desenvolupament: **[indiqueu-lo]**
- Comandament o acció que fem servir per comprovar l'execució: **[completeu-lo]**

> No incorporeu ORM, Hibernate, ObjectDB, MongoDB, serveis externs ni persistència principal en fitxers. Aquests elements no formen part de RA2.

## Com treballem cada *issue*

1. Llegim l'objectiu i els criteris d'acceptació de l'*issue*.
2. Acordem què ha de canviar i qui inicia la feina.
3. Fem canvis petits i comprensibles, amb *commits* que expliquin la decisió.
4. Provem el comportament esperat i en guardem una evidència.
5. Actualitzem aquest README amb el resultat, la prova i l'enllaç al *commit* o a la *pull request*.
6. Tanquem l'*issue* només quan l'equip pot explicar individualment la solució aplicada.

## Progrés del backlog

Marqueu una tasca quan la prova i el rastre al repositori estiguin recollits. Els enllaços apunten a l'enunciat, no a una solució.

### M1 · Base JDBC operativa

- [ ] [RA2-ISSUE-01 · Preparar el projecte JDBC](issues/RA2-ISSUE-01-preparar-projecte-jdbc.md)
- [ ] [RA2-ISSUE-02 · Connector, URL i connexió](issues/RA2-ISSUE-02-revisar-connector-url-connexio.md)
- [ ] [RA2-ISSUE-03 · Estructura relacional](issues/RA2-ISSUE-03-crear-estructura-relacional.md)

### M2 · Operacions relacionals principals

- [ ] [RA2-ISSUE-04 · Inserció de dades](issues/RA2-ISSUE-04-inserir-producte-preparedstatement.md)
- [ ] [RA2-ISSUE-05 · Actualització d'estoc](issues/RA2-ISSUE-05-actualitzar-estoc.md)
- [ ] [RA2-ISSUE-06 · Eliminació controlada](issues/RA2-ISSUE-06-eliminar-producte-controlat.md)
- [ ] [RA2-ISSUE-07 · Consultes i resultats](issues/RA2-ISSUE-07-consultar-inventari-resultset.md)

### M3 · Robustesa JDBC

- [ ] [RA2-ISSUE-08 · Tancament de recursos](issues/RA2-ISSUE-08-tancar-recursos.md)
- [ ] [RA2-ISSUE-09 · Transaccions](issues/RA2-ISSUE-09-transaccio-commit-rollback.md)
- [ ] [RA2-ISSUE-10 · Procediment amb paràmetres](issues/RA2-ISSUE-10-procediment-parametres.md)
- [ ] [RA2-ISSUE-11 · Errors de connexió i operacions](issues/RA2-ISSUE-11-errors-connexio-recursos.md)

### M4 · Documentació i tancament

- [ ] [RA2-ISSUE-12 · Documentar l'execució i la configuració](issues/RA2-ISSUE-12-documentar-execucio-configuracio.md)
- [ ] [RA2-ISSUE-13 · Preparar el lliurament de la pràctica](issues/RA2-ISSUE-13-lliurament-practica-integradora.md)

## Registre de treball

Dupliqueu aquest bloc per a cada *issue* que completeu. Escriviu amb les vostres paraules i enllaceu només proves i *commits* del vostre repositori.

### RA2-ISSUE-XX · [títol de l'*issue*]

- Estat: **pendent | en curs | comprovat**
- Persona que l'ha iniciat: **[nom]**
- Problema inicial: **[què no funcionava o què faltava]**
- Decisió aplicada: **[què heu decidit fer i per què]**
- Canvis fets: **[fitxers o parts del projecte modificades]**
- Prova realitzada: **[cas que heu provat i resultat observat]**
- Evidència: **[enllaç a captura, registre, vídeo breu o apartat del repositori]**
- *Commit* o *pull request*: **[enllaç o identificador]**
- Explicació individual: **[què pot explicar cada integrant sobre aquesta tasca]**
- Ús d'IA, si n'hi ha hagut: **[consulta feta, ajuda rebuda i comprovació pròpia]**

## Proves que hem de poder repetir

| Cas que comprovem | Dades o condicions inicials | Resultat observat | Evidència |
| --- | --- | --- | --- |
| Arrencada del projecte | **[completeu]** | **[completeu]** | **[enllaç]** |
| Operació de modificació | **[completeu]** | **[completeu]** | **[enllaç]** |
| Consulta de dades | **[completeu]** | **[completeu]** | **[enllaç]** |
| Cas d'error controlat | **[completeu]** | **[completeu]** | **[enllaç]** |
| Operació agrupada o transacció | **[completeu]** | **[completeu]** | **[enllaç]** |

## Decisions i dubtes de l'equip

| Data | *Issue* | Decisió o dubte | Com s'ha resolt | Referència |
| --- | --- | --- | --- | --- |
| **[AAAA-MM-DD]** | **[RA2-ISSUE-XX]** | **[completeu]** | **[completeu]** | **[enllaç]** |

## Ús responsable d'IA

El nivell previst és **IA-1**: podeu usar eines d'IA com a suport per entendre conceptes, formular hipòtesis o revisar una explicació. No substitueixen les proves del projecte ni l'explicació individual.

Si n'heu fet ús, anoteu a l'*issue* corresponent què heu preguntat, què heu contrastat amb el projecte i quina decisió final heu pres. No enganxeu una resposta d'IA com si fos una prova de funcionament.

## Abans de donar la pràctica per preparada

- [ ] Els *issues* P0 tenen un resultat comprovat o una incidència explicada.
- [ ] El repositori conté *commits* que permeten seguir el treball de l'equip.
- [ ] Les proves de funcionament tenen evidències enllaçades.
- [ ] Les decisions sobre connector, consultes, recursos, transaccions i procediments estan explicades amb paraules pròpies.
- [ ] Tots dos integrants poden defensar individualment les decisions tècniques del repositori.
- [ ] El README no inclou solucions copiades ni contingut fora de l'abast de RA2.

---

*Aquesta plantilla és un suport per documentar el treball. El que acredita el procés és el repositori de l'equip, amb els seus canvis, proves, decisions i explicacions.*# ComputerCenterShop v1 JavaFX starter

Projecte inicial d'alumnat per al backlog RA2 del modul MP0486 - Acces a dades.

## Finalitat

Aquesta variant deriva de `ComputerCenterShop_v1_javafx`, pero no esta resolta. Compila parcialment sense JavaFX i conserva la interfície JavaFX/FXML, el model i el servei, pero deixa la capa `ProductDaoImplJDBC` amb buits controlats perquè el backlog impliqui crear o corregir codi JDBC real.



## Que ha de resoldre l'alumnat

| Issue | Codi pendent |
| --- | --- |
| RA2-ISSUE-02 | Implementar `connect()` amb URL, usuari i propietats de sistema. |
| RA2-ISSUE-03 | Implementar `initSchema()` amb DDL i seed inicial. |
| RA2-ISSUE-04 | Implementar `insertProduct()` amb `PreparedStatement`. |
| RA2-ISSUE-05 | Implementar `updateStock()` i disponibilitat segons estoc. |
| RA2-ISSUE-06 | Implementar `deleteProduct()` de forma controlada. |
| RA2-ISSUE-07 | Implementar consultes, `ResultSet` i `mapProduct()`. |
| RA2-ISSUE-08 | Revisar tancament de recursos amb `try-with-resources` i `disconnect()`. |
| RA2-ISSUE-09 | Implementar transaccio `commit` / `rollback`. |
| RA2-ISSUE-10 | Implementar crida amb `CallableStatement`. |
| RA2-ISSUE-11 | Millorar gestio d'errors de connexio i operacions. |

## Execucio prevista

Requisits:

- JDK 25 LTS.
- Maven.

Compilar:

```bash
mvn compile
```

Executar JavaFX:

```bash
mvn javafx:run
```

En l'estat inicial, l'aplicacio pot mostrar errors `RA2-ISSUE-xx pendent`. Aquests errors son intencionats i indiquen quin issue s'ha de resoldre.

## Limits RA2

No s'ha d'introduir ORM, Hibernate, ObjectDB, MongoDB, serveis externs, persistencia principal en fitxers ni components reutilitzables de RA6.
