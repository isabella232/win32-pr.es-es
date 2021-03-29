---
description: La red del modo de transferencia asincrónico (ATM) está en funcionamiento en el estándar de la informática y se ha agregado compatibilidad con ATM a muchas partes del sistema operativo.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Calidad de servicio (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6525ced0b29d35482244c3c37f8382edbfcb9fd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911986"
---
# <a name="quality-of-service-telephony-api"></a>Calidad de servicio (API de telefonía)

La red del modo de transferencia asincrónico (ATM) está en funcionamiento en el estándar de la informática y se ha agregado compatibilidad con ATM a muchas partes del sistema operativo. TAPI también admite atributos clave para establecer llamadas en las instalaciones de ATM. Lo más importante de la perspectiva de la aplicación es la posibilidad de solicitar, negociar, renegociar y recibir indicaciones de los parámetros de calidad de servicio (QOS) en las llamadas entrantes y salientes.

La información de QOS en TAPI se intercambia entre aplicaciones y proveedores de servicios en estructuras [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) definidas en Windows sockets 2,0.

Las aplicaciones solicitan QOS en las llamadas salientes estableciendo los valores de información de sesión antes de iniciar una sesión de comunicaciones. El proveedor de servicios intentará proporcionar la QOS especificada y se producirá un error en la llamada si no es posible. A continuación, la aplicación puede ajustar sus parámetros y volver a intentar la llamada. Una vez establecida una llamada, una aplicación puede solicitar un cambio en la QOS.

TAPI proporciona notificaciones de eventos para el propietario o la supervisión de aplicaciones si se produce algún cambio en los niveles de QOS.

La compatibilidad con QOS no está restringida a los transportes ATM; cualquier proveedor de servicios puede implementar características de QOS.

No todos los proveedores de servicios admiten el uso de esta información.

* * TAPI 2. x: * *[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **DwSendingFlowspecOffset**, **dwReceivingFlowspecSize** y **dwReceivingFlowspecOffset** miembros de [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)

* * TAPI 3. x: * *[**ITBasicCallControl:: SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)

 

 
