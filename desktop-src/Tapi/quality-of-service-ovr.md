---
description: Las redes del modo de transferencia asincrónica (ATM) están emergiendo en la parte estándar de la informática y se ha agregado compatibilidad con ATM a muchas partes del sistema operativo.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Calidad de servicio (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 131f54d69cd44799f9ea694fe83d50f28fded0ac7c8c15dabfd7a2db499b2293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761236"
---
# <a name="quality-of-service-telephony-api"></a>Calidad de servicio (API de telefonía)

Las redes del modo de transferencia asincrónica (ATM) están emergiendo en la parte estándar de la informática y se ha agregado compatibilidad con ATM a muchas partes del sistema operativo. TAPI también admite atributos clave para establecer llamadas en instalaciones de cajeros automáticos. La más importante de ellas desde la perspectiva de la aplicación es la capacidad de solicitar, negociar, renegociar y recibir indicaciones de parámetros de calidad de servicio (QOS) en las llamadas entrantes y salientes.

La información de QOS en TAPI se intercambia entre aplicaciones y proveedores de servicios en estructuras [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) que se definen en Windows Sockets 2.0.

Las aplicaciones solicitan QOS en las llamadas salientes estableciendo valores de información de sesión antes de iniciar una sesión de comunicaciones. El proveedor de servicios intentará proporcionar la QOS especificada y producirá un error en la llamada si no es posible. A continuación, la aplicación puede ajustar sus parámetros e intentar la llamada de nuevo. Una vez establecida una llamada, una aplicación puede solicitar un cambio en la QOS.

TAPI proporciona notificaciones de eventos al propietario o a las aplicaciones de supervisión si se produce algún cambio en los niveles de QOS.

La compatibilidad con QOS no está restringida a los transportes de cajeros automáticos. cualquier proveedor de servicios puede implementar características de QOS.

No todos los proveedores de servicios admiten el uso de esta información.

**TAPI 2.x: **[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **dwSendingFlowspecOffset,** **dwReceivingFlowspecSize** y **dwReceivingFlowspecOffset** miembros de [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)

**TAPI 3.x: **[**ITBasicCallControl::SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)

 

 
