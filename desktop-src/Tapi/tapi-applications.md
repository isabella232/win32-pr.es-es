---
description: En el siguiente material se proporcionan instrucciones sobre el uso de TAPI para escribir aplicaciones de comunicaciones de servidor o usuario final. Esta información también es muy relevante para los programadores del proveedor de servicios.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: Aplicaciones TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7133e65576a1c89a30211d9b7af34e3cde130190291aa1547877094566f597d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034295"
---
# <a name="tapi-applications"></a>Aplicaciones TAPI

En el siguiente material se proporcionan instrucciones sobre el uso de TAPI para escribir aplicaciones de comunicaciones de servidor o usuario final. Esta información también es muy relevante para los programadores del proveedor de servicios.

La primera decisión que debe tomar un programador en el uso de TAPI es el nivel de servicio necesario. Por ejemplo, si una aplicación requiere una selección de menú que puede marcar un número de teléfono, probablemente no se requiera una aplicación TAPI completa. La telefonía asistida puede habilitar esta opción de forma rápida y sencilla. Consulte Niveles [de servicio de TAPI](tapi-levels-of-service.md) para obtener más información sobre la distinción entre las aplicaciones TAPI completa y la telefonía asistida.

La segunda decisión importante es si se debe usar TAPI 2.x, la API basada en C o TAPI 3.x, que se basa en COM. Consulte [TAPI 3.x frente a TAPI 2.x](tapi-3-x-versus-tapi-2-x.md) para obtener una explicación de consideraciones importantes a la hora de decidir cuál usar.

En el diagrama siguiente se muestran los bloques de creación básicos de una aplicación TAPI completa. TAPI 2.x y TAPI 3.x se abordan en estas secciones. El material muy específico de uno se trata en las secciones de información general de TAPI 2.x o TAPI 3.x.

![bloques de creación de una aplicación tapi](images/tapior3.png)

Los vínculos siguientes proporcionan contenido que corresponde a las figuras de la imagen anterior:

| Figura | Documentación                                                                    |
|--------|----------------------------------------------------------------------------------|
| 1      | [Inicialización de TAPI](tapi-initialization.md)                                   |
| 2      | [Control de sesión](session-control.md)                                           |
| 3      | [Control de dispositivos](device-control.md)                                             |
| 4      | [Control multimedia](media-control.md)                                               |
| 5      | [Acerca de los controles del centro de llamadas](about-call-center-controls.md)                     |
| 6      | [Conferencia de telefonía IP de encuentro](rendezvous-ip-telephony-conferencing.md) |
| 7      | [Apagado de TAPI](tapi-shutdown.md)                                               |



 

 

 



