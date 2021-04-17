---
description: En el material siguiente se proporcionan instrucciones sobre el uso de TAPI para escribir aplicaciones de comunicaciones de usuario final o de servidor. Esta información también es muy relevante para los programadores de proveedores de servicios.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: Aplicaciones TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678357"
---
# <a name="tapi-applications"></a>Aplicaciones TAPI

En el material siguiente se proporcionan instrucciones sobre el uso de TAPI para escribir aplicaciones de comunicaciones de usuario final o de servidor. Esta información también es muy relevante para los programadores de proveedores de servicios.

La primera decisión que debe realizar un programador al usar TAPI es el nivel de servicio requerido. Por ejemplo, si una aplicación requiere una selección de menú que puede marcar un número de teléfono, es probable que no se requiera una aplicación TAPI completa. La telefonía asistida puede habilitar esta opción de forma rápida y sencilla. Consulte [niveles de servicio de TAPI](tapi-levels-of-service.md) para obtener más información acerca de la diferencia entre las aplicaciones TAPI completas y la telefonía asistida.

La segunda decisión importante es si se usa TAPI 2. x, la API basada en C o TAPI 3. x, que se basa en COM. Consulte [TAPI 3. x frente a TAPI 2. x](tapi-3-x-versus-tapi-2-x.md) para obtener una explicación de las consideraciones importantes a la hora de decidir cuál usar.

En el diagrama siguiente se ilustran los bloques de creación básicos de una aplicación TAPI completa. TAPI 2. x y TAPI 3. x se tratan en estas secciones. En las secciones de información general de TAPI 2. x o TAPI 3. x se trata el material muy específico de uno.

![bloques de creación de una aplicación TAPI](images/tapior3.png)

Los vínculos siguientes proporcionan contenido que corresponde a las cifras de la imagen anterior:

| Figura | Documentación                                                                    |
|--------|----------------------------------------------------------------------------------|
| 1      | [Inicialización de TAPI](tapi-initialization.md)                                   |
| 2      | [Control de sesión](session-control.md)                                           |
| 3      | [Control de dispositivo](device-control.md)                                             |
| 4      | [Control multimedia](media-control.md)                                               |
| 5      | [Acerca de los controles de centro de llamadas](about-call-center-controls.md)                     |
| 6      | [Conferencias de telefonía IP de encuentro](rendezvous-ip-telephony-conferencing.md) |
| 7      | [Apagado de TAPI](tapi-shutdown.md)                                               |



 

 

 



