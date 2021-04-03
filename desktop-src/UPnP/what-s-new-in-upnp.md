---
title: Novedades de las API de UPnP
description: Las API de™ UPnP tienen nuevas características y documentación actualizada para Windows XP SP2. En la tabla siguiente se identifica la nueva documentación.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779885"
---
# <a name="whats-new-in-the-upnp-apis"></a>Novedades de las API de UPnP

Las API de™ UPnP tienen nuevas características y documentación actualizada para Windows XP SP2. En la tabla siguiente se identifica la nueva documentación.



| Característica                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | Esta nueva interfaz permite a un dispositivo hospedado obtener información sobre un solicitante (es decir, un punto de control) y la solicitud. Incluye tres métodos, cada uno de los cuales proporciona un tipo de información diferente.                                                                                                                                                              |
| [Implementar el comportamiento del dispositivo](implementing-device-behavior.md) | En este tema se incluye una nueva sección que explica cómo obtener información del punto de conexión mediante la nueva interfaz [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) .                                                                                                                                                                                                     |
| [Opciones de configuración](configuration-settings.md)             | Este nuevo tema proporciona información sobre la configuración del registro que afecta al comportamiento de las API de UPnP.                                                                                                                                                                                                                                                                    |
| [Códigos de error de dispositivo](device-error-codes.md)                     | Este nuevo tema explica cómo se convierte un código de error de un dispositivo en un valor HRESULT y viceversa. Es necesario entender este proceso para evaluar un valor HRESULT que devuelven los métodos [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) y [**IUPnPService:: QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) . |



 

 

 




