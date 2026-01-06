# 🚚 App de Gestión de Actividades y Normativa para Conductores Profesionales

Una aplicación móvil pensada **para el conductor**, no para la oficina.  
Combina normativa, GPS y una línea de tiempo visual para ayudar a cumplir el Reglamento 561/2006 de forma clara e intuitiva.

---

## 🧩 Módulos principales

### 🟦 1. Recordatorios
Sistema de avisos útiles para el conductor:
- recordatorios persistentes,
- alertas contextuales,
- avisos normativos.

### 🟦 2. Gestor de Localizaciones
Motor de geolocalización con:
- detección peatón/vehículo,
- filtros de precisión y velocidad,
- gestión de puntos GPS,
- sincronización con actividades.

### 🟦 3. Registro de Recorridos
Sistema de rutas con:
- polilíneas limpias,
- bounding box automático,
- marcadores de inicio y fin,
- integración con la línea de tiempo.

---

## 🎯 Funcionalidades destacadas

- Registro de actividades (conducción, trabajo, descanso, disponibilidad).  
- Línea de tiempo visual de toda la jornada.  
- Detección automática de descansos largos.  
- Clasificación normativa (diario, reducido, semanal, normal).  
- Reinicio automático del período de 144 horas.  
- Cálculo y gestión de compensaciones pendientes.  
- Avisos persistentes y puntuales para evitar sanciones.  

---

## 🧠 ¿Por qué es diferente?

Los softwares del sector (TachoScan, Optac, Continental…) están pensados para inspectores y gestores.  
Esta app está pensada **para el conductor**:

- asistencia en tiempo real,  
- normativa explicada de forma humana,  
- prevención de infracciones,  
- integración GPS + actividades + normativa,  
- todo en un solo dispositivo.

---

## 🗺 Diagrama conceptual del proyecto

```text
                ┌──────────────────────────┐
                │        Pantalla          │
                │        Principal         │
                │  - Estado actual         │
                │  - Avisos persistentes   │
                │  - Timeline + Mapa       │
                └────────────┬─────────────┘
                             │
                             ▼
        ┌──────────────────────────────────────────┐
        │              Motor Normativo             │
        │  - Clasificación de descansos            │
        │  - Períodos de 144h                      │
        │  - Compensaciones pendientes             │
        │  - Aplicación automática                 │
        └──────────────────┬───────────────────────┘
                           │
                           ▼
        ┌──────────────────────────────────────────┐
        │            Gestor de Actividades         │
        │  - Conducción / Trabajo / Descanso       │
        │  - Inicio y fin de actividad             │
        │  - Sincronización con timeline           │
        └──────────────────┬───────────────────────┘
                           │
                           ▼
        ┌──────────────────────────────────────────┐
        │         Gestor de Localizaciones         │
        │  - GPS filtrado                          │
        │  - Modo peatón/vehículo                  │
        │  - Registro de puntos                    │
        └──────────────────┬───────────────────────┘
                           │
                           ▼
        ┌──────────────────────────────────────────┐
        │       Registro de Recorridos             │
        │  - Polilíneas limpias                    │
        │  - Marcadores de inicio y fin            │
        │  - Bounding box automático               │
        └──────────────────────────────────────────┘


👤 Autor
Projecte desenvolupat per P&C enginyeria, Android developer i creative technologist.
