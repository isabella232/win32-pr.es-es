---
description: Las direcciones de transporte (XAddrs) incluidas en los mensajes ProbeMatches y ResolveMatches están sujetas a la validación básica antes de que WSDAPI envíe un mensaje HTTP, como una solicitud de metadatos.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Reglas de validación de XAddr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc91ce8a0e1bba267ea92fa79a6680b481297f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276109"
---
# <a name="xaddr-validation-rules"></a>Reglas de validación de XAddr

Las direcciones de transporte (XAddrs) incluidas en los mensajes [ProbeMatches](probematches-message.md) y [ResolveMatches](resolvematches-message.md) están sujetas a la validación básica antes de que WSDAPI envíe un mensaje http, como una solicitud de metadatos.

Para asegurarse de que los XAddrs están en la misma subred que el cliente.

En el código XML siguiente se muestra un elemento XAddrs de ejemplo. El prefijo WSD hace referencia al espacio de nombres `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

Se deben cumplir todas las condiciones siguientes antes de que el mensaje HTTP salga de la conexión.

-   XAddrs debe ser una dirección HTTP o HTTPS. XAddrs de otros esquemas se omiten.
-   Si hay algún XAddrs HTTPS presente, todos los XAddrs deben ser HTTPS. Las secciones XAddr que incluyen direcciones HTTP y HTTPS se omiten por completo. Además, la dirección del punto de conexión del dispositivo debe coincidir exactamente con el XAddrs HTTPS.
-   XAddrs debe ser direcciones IP o nombres de host que puedan resolverse a través de DNS. Normalmente, se usan direcciones IP.
-   Al menos una dirección IP incluida en la XAddrs (o la dirección IP resuelta desde un nombre de host incluido en XAddrs) debe estar en la misma subred que el adaptador en el que se recibió el mensaje [ProbeMatches](probematches-message.md) o [ResolveMatches](resolvematches-message.md) .
-   La dirección y el puerto especificados en el primer XAddr deben ser accesibles. WSDAPI intenta conectarse a esta dirección al establecer una conexión HTTP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ProbeMatches](probematches-message.md)
</dt> <dt>

[ResolveMatches](resolvematches-message.md)
</dt> <dt>

[Patrones de mensajes de intercambio de metadatos y detección](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



