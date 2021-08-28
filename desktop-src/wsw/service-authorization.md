---
title: Autorización de servicio
description: Una aplicación puede implementar la autorización personalizada para los mensajes entrantes en un host de servicio.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Servicios web de autorización de servicio para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b84b9947d088d5f594ac11f0ee83cc03925f8a3bbc9aeceae0bc7d5cb120477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109845"
---
# <a name="service-authorization"></a>Autorización de servicio

Una aplicación puede implementar la autorización personalizada para los mensajes entrantes en un host de servicio.


Un host de servicio recibe una devolución de llamada de seguridad [**WS \_ SERVICE SECURITY \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) como parte del punto de conexión de servicio de [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) que se pasa a la función [**WsCreateServiceHost.**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) Esta devolución de llamada se invoca cuando [se recibe WS \_ MESSAGE.](ws-message.md)

La aplicación puede confiar en esta devolución de llamada para implementar la autorización personalizada para los mensajes entrantes en el host de servicio. Si se produce un error en la autorización, la función de devolución de llamada de seguridad devuelve un rr. H. de error y el host de servicio anula el canal.

Vea el nombre de usuario sobre el ejemplo de [SSL, HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), para obtener una implementación de ejemplo.

 

 




