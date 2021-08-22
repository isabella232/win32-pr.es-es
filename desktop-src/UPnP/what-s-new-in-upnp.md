---
title: Novedades de las API de UPnP
description: Las API de ™ UPnP tienen nuevas características y documentación actualizada para Windows XP SP2. En la tabla siguiente se identifica la nueva documentación.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68ab872eab498e80ec8d30f996f839c73432875d02ec8d32060595ce8d6482b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058005"
---
# <a name="whats-new-in-the-upnp-apis"></a>Novedades de las API de UPnP

Las API de ™ UPnP tienen nuevas características y documentación actualizada para Windows XP SP2. En la tabla siguiente se identifica la nueva documentación.



| Característica                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | Esta nueva interfaz permite que un dispositivo hospedado obtenga información sobre un solicitante (es decir, un punto de control) y la solicitud. Incluye tres métodos, cada uno de los cuales proporciona un tipo de información diferente.                                                                                                                                                              |
| [Implementar el comportamiento del dispositivo](implementing-device-behavior.md) | En este tema se incluye una nueva sección en la que se explica cómo obtener información del punto de conexión mediante la nueva [**interfaz IUPnPRemoteEndpointInfo.**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)                                                                                                                                                                                                     |
| [Configuración Configuración](configuration-settings.md)             | En este nuevo tema se proporciona información sobre la configuración del Registro que afecta al comportamiento de las API de UPnP.                                                                                                                                                                                                                                                                    |
| [Códigos de error de dispositivo](device-error-codes.md)                     | En este nuevo tema se explica cómo un código de error de un dispositivo se convierte en un valor HRESULT y viceversa. Es necesario comprender este proceso para evaluar un valor HRESULT devuelto por los métodos [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) e [**IUPnPService::QueryStateVariable.**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) |



 

 

 




