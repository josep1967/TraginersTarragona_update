📘 Traginers de Tarragona (Android)

📝 Descripció del projecte
Aquesta aplicació Android permet gestionar períodes de treball, activitats diàries i descansos segons la normativa de transport professional. 
Inclou càlcul automàtic de:
- Descansos entre activitats
- Descansos setmanals
- Reduccions aplicades
- Compensacions pendents
- Disponibilitat futura
- Tancament i obertura de períodes

L’objectiu és oferir una eina fiable, clara i normativa per al conductor.

Tambè pot programar Recordatoris amb Notificacions persistents.

Gestió de Localitzacions desades.

Grabació de Recorreguts.

🧱 Arquitectura general
El projecte està desenvolupat en Java amb Android Studio, utilitzant:
- SQLite com a base de dades local
- DBHelper com a capa d’accés a dades
- MainActivity com a pantalla principal
- ActividadActivity per gestionar activitats i períodes
- SharedPreferences per sincronitzar l’estat de la UI entre pantalles
  
🔄 Flux de funcionament
1. Obertura d’un període
- Es crea un nou registre a periodo
- Es guarda la data d’inici
- La UI mostra disponibilitat immediata
2. Creació d’activitats
Cada activitat té:
- Hora d’inici i fi
- Tipus d’activitat
- Reducció aplicada (si escau)
Quan es tanca una activitat:
- Es calcula el descans amb l’anterior
- Es classifica (normal, reduït, insuficient)
- Es marca reduccionAplicada si toca
- S’actualitza reducciones i compensacionPendiente del període
3. Tancament d’un període
Quan es tanca:
- Es valida que no hi hagi activitat oberta
- Es calcula duració total, km i reduccions
- Es mostra un resum
- Es calcula la nova disponibilitat: fi del període + 45 hores
- Aquesta disponibilitat es desa a SharedPreferences
4. MainActivity
Quan l’usuari torna a la pantalla principal:
- Llegeix l’estat guardat a SharedPreferences
- Mostra disponibilitat, avisos i estat general

🧮 Lògica normativa implementada
✔ Descansos
- Càlcul automàtic entre activitats
- Classificació segons normativa
✔ Reduccions
- Es marquen a l’activitat on s’apliquen
- Es comptabilitzen al període
- Es mostren com X / 3
✔ Compensacions
- S’acumulen al període
- Es mostren al resum de tancament
✔ Disponibilitat
- Durant període → segons activitat
- Després de tancar període → fi + 45h

💾 Persistència
SQLite

👤 Autor
Projecte desenvolupat per P&C enginyeria, Android developer i creative technologist.
