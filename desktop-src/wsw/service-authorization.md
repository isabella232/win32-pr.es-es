---
title: Autorización de servicio
description: Una aplicación puede implementar la autorización personalizada para los mensajes entrantes en un host de servicio.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Servicios Web de autorización de servicios para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c296dc6b4900bd20df7d1e70631e758599a0028d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149732"
---
# <a name="service-authorization"></a>Autorización de servicio

Una aplicación puede implementar la autorización personalizada para los mensajes entrantes en un host de servicio.


Un host de servicio recibe una [**devolución de \_ \_ \_ llamada de seguridad del servicio WS del servicio**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) de devolución de llamada de seguridad como parte del punto de [**\_ \_ conexión de servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) que se pasa a la función [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) . Esta devolución de llamada se invoca cuando se recibe el [ \_ mensaje de WS](ws-message.md) .

La aplicación puede basarse en esta devolución de llamada para implementar la autorización personalizada para los mensajes entrantes en el host del servicio. Si se produce un error en la autorización, la función de devolución de llamada de seguridad devuelve un error HR y el host del servicio anula el canal.

Vea el ejemplo de nombre de usuario sobre SSL, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), para obtener una implementación de ejemplo.

 

 




