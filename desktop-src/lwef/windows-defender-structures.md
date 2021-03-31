---
title: Estructuras de Windows Defender
description: Estructuras usadas por las aplicaciones cuando se llama a exámenes de solicitud, actualizaciones de firmas o información de Windows Defender.
ms.assetid: EF4116D3-DA50-4078-A024-2D624945D8C1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d690de552137ce267b9d1d7a9cec711b161528
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774491"
---
# <a name="windows-defender-structures"></a>Estructuras de Windows Defender

Estructuras usadas por las aplicaciones cuando se llama a exámenes de solicitud, actualizaciones de firmas o información de Windows Defender.



| Estructura                                                      | Descripción                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**datos de MPCALLBACK \_**](mpcallback-data.md)                    | Datos pasados a la función de devolución de llamada.<br/>                                        |
| [**datos de MPCLEAN \_**](mpclean-data.md)                          | Datos de notificación pasados a la función de devolución de llamada Clean.<br/>                         |
| [**MPCLEAN \_ comprobar \_ datos**](mpclean-precheck-data.md)       | Datos de notificación pasados a la función de devolución de llamada de precomprobación limpia.<br/>                |
| [**Estado de MPCOMPONENT \_**](mpcomponent-status.md)              | Información de estado del componente.<br/>                                                |
| [**versión de MPCOMPONENT \_**](mpcomponent-version.md)            | Versión y tiempo de actualización de un componente individual.<br/>                         |
| [**datos de MPCONFIGURATION \_**](mpconfiguration-data.md)          | Contiene datos sobre los cambios de configuración, incluidos los valores antiguos y nuevos.<br/> |
| [**datos de MPENDOFLIFE \_**](mpendoflife-data.md)                  | Datos de notificación de "fin de la vida".<br/>                                             |
| [**datos de MPEXPIRATION \_**](mpexpiration-data.md)                | Notificación de estado de expiración del producto.<br/>                                      |
| [**datos de MPFASTPATH \_**](mpfastpath-data.md)                    | Notificación de actualización de FastPath.<br/>                                                |
| [**datos de MPHEALTH \_**](mphealth-data.md)                        | Datos de notificación de estado.<br/>                                                    |
| [**datos de MPMALWARETOAST \_**](mpmalwaretoast-data.md)            | Datos de notificación del sistema de malware.<br/>                                             |
| [**MPNIS \_ \_ datos privados**](mpnis-private-data.md)             | Notificaciones NIS privadas.<br/>                                                   |
| [**datos de MPRESERVED \_**](mpreserved-data.md)                    | Datos de notificación reservados.<br/>                                                  |
| [**información de MPRESOURCE \_**](mpresource-info.md)                    | Estructura de información de recursos.<br/>                                              |
| [**estadísticas de MPRESOURCE \_**](mpresource-stats.md)                  | Estadísticas relacionadas con recursos.<br/>                                                 |
| [**datos de MPSAMPLE \_**](mpsample-data.md)                        | Datos de notificación pasados a la función de devolución de llamada de envío de ejemplo.<br/>         |
| [**datos de MPSCAN \_**](mpscan-data.md)                            | Examinar los datos pasados a la devolución de llamada.<br/>                                            |
| [**recursos de MPSCAN \_**](mpscan-resources.md)                  | Información de recursos pasada durante una operación de examen.<br/>                         |
| [**resultado de MPSCAN \_**](mpscan-result.md)                        | Los resultados de un examen.<br/>                                                       |
| [**datos de MPSIGUPDATE \_**](mpsigupdate-data.md)                  | Datos de notificación pasados a la función de devolución de llamada de actualización de firma.<br/>          |
| [**datos de MPSTATUS \_**](mpstatus-data.md)                        | Contiene datos sobre el estado actual de un componente del producto.<br/>        |
| [**MPSTATUS \_ DATAEX \_ no usado**](mpstatus-dataex-unused.md)     | Estructura ficticia para no SRP.<br/>                                                 |
| [**información de MPSTATUS \_**](mpstatus-info.md)                        | Información de estado para el administrador de protección contra malware de.<br/>                       |
| [**datos de MPTHREAT \_**](mpthreat-data.md)                        | Datos de notificación pasados debido a la detección de amenazas o a la modificación.<br/>            |
| [**información de MPTHREAT \_**](mpthreat-info.md)                        | Contiene información sobre una amenaza.<br/>                                         |
| [**\_comportamiento de INFOEX de MPTHREAT \_**](mpthreat-infoex-behavior.md) | Contiene información específica de la modificación del comportamiento.<br/>                         |
| [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)           | Contiene información específica de NIS.<br/>                                           |
| [**MPTHREAT \_ INFOEX \_ no usado**](mpthreat-infoex-unused.md)     | Estructura ficticia para amenazas de tipo de modificación sin comportamiento.<br/>                  |
| [**\_información localizada de MPTHREAT \_**](mpthreat-localized-info.md)   | Información localizada para una amenaza.<br/>                                          |
| [**estadísticas de MPTHREAT \_**](mpthreat-stats.md)                      | Estadísticas relacionadas con amenazas.<br/>                                                   |
| [**datos de estadísticas de MPTHREAT \_ \_**](mpthreat-stats-data.md)           | Datos adicionales de estadísticas de amenazas.<br/>                                           |
| [**información de MPVERSION \_**](mpversion-info.md)                      | Información de versión de los componentes del administrador de protección contra malware de.<br/>         |



 

 

 





