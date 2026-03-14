# 📑 Especificación de Requisitos (IEEE 830)

## 1. Introducción

Este documento define los requisitos para el **Sistema de Gestión de Semáforos Inteligentes (SGSI-RUU)**, enfocado en la optimización del flujo vehicular y la seguridad vial en la localidad de Rafael Uribe Uribe, Bogotá. El sistema se alinea con el Plan de Movilidad Distrital y los protocolos del Centro de Gestión de Tránsito (CGT).

## 2. Requisitos Funcionales (RF)
| ID | Descripción | Fuente | Prioridad |
| :--- | :--- | :--- | :--- |
| **RF-01** | **Control de Ciclos Dinámicos:** Ajuste automático de tiempos (verde/rojo) basado en el conteo de vehículos de los sensores. | Ingeniería de Tránsito | **Alta** |
| **RF-02** | **Prioridad a Emergencias (Preemption):** Cambio forzado a verde al detectar señales GPS de ambulancias o bomberos. | Protocolo de Emergencias | **Alta** |
| **RF-03** | **Sincronización de Corredores (Ola Verde):** Coordinación de fases entre semáforos sucesivos en la Av. Caracas y Calle 40 Sur. | Plan de Movilidad | **Alta** |
| **RF-04** | **Monitoreo de Hardware:** Reporte en tiempo real sobre el estado de las luminarias LED y controladores locales. | Mantenimiento Preventivo | **Media** |
| **RF-05** | **Interfaz de Operador Remoto:** Panel de control para intervención manual desde el CGT en caso de protestas o bloqueos. | Operaciones CGT | **Media** |

## 3. Requisitos No Funcionales (RNF)
* **Disponibilidad (Alta Disponibilidad):** El software debe garantizar un tiempo de actividad del **99.99%**, ya que un fallo puede comprometer la vida de los ciudadanos.
* **Tiempo de Respuesta (Real-Time):** El procesamiento de los inputs de los sensores y la ejecución del cambio de luces debe ocurrir en un tiempo de latencia menor a **100ms**.
* **Seguridad (Fail-Safe):** En caso de pérdida de conexión con el servidor central o fallo de lógica, el controlador físico debe activar automáticamente el modo de **Amarillo Intermitente** en todas las direcciones.
* **Ciberseguridad:** Toda comunicación entre los controladores de calle y la central debe estar protegida mediante túneles **VPN y encriptación robusta** para evitar ataques de denegación de servicio o manipulación externa.
* **Escalabilidad:** El sistema debe permitir la integración de hasta **200 nuevas intersecciones** en la localidad sin degradar el rendimiento del servidor.

---
*Documento generado para la Facultad de Ingeniería de Sistemas - Universidad Antonio Nariño.*
