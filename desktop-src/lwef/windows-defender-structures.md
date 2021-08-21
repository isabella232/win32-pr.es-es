---
title: Windows Defender Estructuras
description: Estructuras usadas por las aplicaciones al llamar a para solicitar exámenes, actualizaciones de firmas o información de Windows Defender.
ms.assetid: EF4116D3-DA50-4078-A024-2D624945D8C1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa735805fd5f9b7f85e61bff748ee2714d915ab1ddf7f94eabb9fff316aba710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975385"
---
# <a name="windows-defender-structures"></a>Windows Defender Estructuras

Estructuras usadas por las aplicaciones al llamar a para solicitar exámenes, actualizaciones de firmas o información de Windows Defender.



| Estructura                                                      | Descripción                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DATOS DE DEVOLUCIÓN DE \_ LLAMADA DE MP**](mpcallback-data.md)                    | Datos pasados a la función de devolución de llamada.<br/>                                        |
| [**MPCLEAN \_ DATA**](mpclean-data.md)                          | Datos de notificación pasados a la función de devolución de llamada limpia.<br/>                         |
| [**MPCLEAN \_ PRECHECK \_ DATA**](mpclean-precheck-data.md)       | Datos de notificación pasados para limpiar la función de devolución de llamada de comprobación previa.<br/>                |
| [**ESTADO DE \_ MPCOMPONENT**](mpcomponent-status.md)              | Información de estado del componente.<br/>                                                |
| [**VERSIÓN DE \_ MPCOMPONENT**](mpcomponent-version.md)            | Versión y hora de actualización de un componente individual.<br/>                         |
| [**DATOS DE \_ MPCONFIGURATION**](mpconfiguration-data.md)          | Contiene datos sobre los cambios de configuración, incluidos los valores antiguos y nuevos.<br/> |
| [**DATOS DE \_ MPENDOFLIFE**](mpendoflife-data.md)                  | Datos de notificación de "Fin del ciclo de vida".<br/>                                             |
| [**DATOS DE \_ MPEXPIRATION**](mpexpiration-data.md)                | Notificación de estado de expiración del producto.<br/>                                      |
| [**DATOS \_ MPFASTPATH**](mpfastpath-data.md)                    | Notificación de actualización de FastPath.<br/>                                                |
| [**DATOS DE \_ MPHEALTH**](mphealth-data.md)                        | Datos de notificación de estado.<br/>                                                    |
| [**DATOS MPMALWARETOAST \_**](mpmalwaretoast-data.md)            | Datos de notificación del sistema de malware.<br/>                                             |
| [**DATOS PRIVADOS DE MPNI \_ \_**](mpnis-private-data.md)             | Notificaciones privadas de NIS.<br/>                                                   |
| [**DATOS \_ MPRESERVED**](mpreserved-data.md)                    | Datos de notificación reservados.<br/>                                                  |
| [**MPRESOURCE \_ INFO**](mpresource-info.md)                    | Estructura de información de recursos.<br/>                                              |
| [**MPRESOURCE \_ STATS**](mpresource-stats.md)                  | Estadísticas relacionadas con recursos.<br/>                                                 |
| [**DATOS \_ MPSAMPLE**](mpsample-data.md)                        | Datos de notificación pasados a la función de devolución de llamada de envío de ejemplo.<br/>         |
| [**DATOS DE \_ MPSCAN**](mpscan-data.md)                            | Examinar los datos pasados a la devolución de llamada.<br/>                                            |
| [**RECURSOS DE \_ MPSCAN**](mpscan-resources.md)                  | Información de recursos pasada durante una operación de examen.<br/>                         |
| [**MPSCAN \_ RESULT**](mpscan-result.md)                        | Resultados de un examen.<br/>                                                       |
| [**MPSIGUPDATE \_ DATA**](mpsigupdate-data.md)                  | Datos de notificación pasados a la función de devolución de llamada de actualización de firma.<br/>          |
| [**DATOS DE \_ MPSTATUS**](mpstatus-data.md)                        | Contiene datos sobre el estado actual de un componente del producto.<br/>        |
| [**MPSTATUS \_ DATAEX \_ UNUSED**](mpstatus-dataex-unused.md)     | Estructura ficticia para no SRP.<br/>                                                 |
| [**INFORMACIÓN \_ DE MPSTATUS**](mpstatus-info.md)                        | Información de estado del administrador de protección contra malware.<br/>                       |
| [**DATOS DE \_ MPTHREAT**](mpthreat-data.md)                        | Datos de notificación pasados debido a la detección o modificación de amenazas.<br/>            |
| [**INFORMACIÓN DE \_ MPTHREAT**](mpthreat-info.md)                        | Contiene información sobre una amenaza.<br/>                                         |
| [**COMPORTAMIENTO DE \_ INFOEX DE MPTHREAT \_**](mpthreat-infoex-behavior.md) | Contiene información específica de modificación del comportamiento.<br/>                         |
| [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)           | Contiene información específica de NIS.<br/>                                           |
| [**MPTHREAT \_ INFOEX \_ SIN USAR**](mpthreat-infoex-unused.md)     | Estructura ficticia para amenazas de tipos de modificación que no son de comportamiento.<br/>                  |
| [**INFORMACIÓN LOCALIZADA DE MPTHREAT \_ \_**](mpthreat-localized-info.md)   | Información localizada de una amenaza.<br/>                                          |
| [**ESTADÍSTICAS DE MPTHREAT \_**](mpthreat-stats.md)                      | Estadísticas relacionadas con amenazas.<br/>                                                   |
| [**DATOS DE ESTADÍSTICAS \_ DE MPTHREAT \_**](mpthreat-stats-data.md)           | Datos de estadísticas de amenazas adicionales.<br/>                                           |
| [**INFORMACIÓN \_ DE MPVERSION**](mpversion-info.md)                      | Información de versión de los componentes del administrador de protección contra malware.<br/>         |



 

 

 





