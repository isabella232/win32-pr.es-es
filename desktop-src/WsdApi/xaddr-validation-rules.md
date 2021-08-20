---
description: Las direcciones de transporte (XAddrs) incluidas en los mensajes ProbeMatches y ResolveMatches están sujetas a validación básica antes de que WSDAPI envíe un mensaje HTTP, como una solicitud de metadatos.
ms.assetid: 6b5139b5-aa31-42bc-a281-8784006edfbe
title: Reglas de validación de XAddr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3b167101b6012bcf20779381993cfff4ea7ea22d35eef5397ac1349baa2cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049513"
---
# <a name="xaddr-validation-rules"></a>Reglas de validación de XAddr

Las direcciones de transporte (XAddrs) incluidas en los mensajes [ProbeMatches](probematches-message.md) y [ResolveMatches](resolvematches-message.md) están sujetas a validación básica antes de que WSDAPI envíe un mensaje HTTP, como una solicitud de metadatos.

Esto es para asegurarse de que los XAddrs están en la misma subred que el cliente.

El siguiente XML muestra un elemento XAddrs de ejemplo. El prefijo wsd hace referencia al espacio de nombres `https://schemas.xmlsoap.org/ws/2005/04/discovery` .

``` syntax
<wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs>
```

Se deben cumplir todas las condiciones siguientes antes de que el mensaje HTTP salga a través de la conexión.

-   XAddrs debe ser direcciones HTTP o HTTPS. Se omiten los XAddrs de otros esquemas.
-   Si hay algún XAddr HTTPS presente, todos los XAddrs deben ser HTTPS. Las secciones de XAddr que incluyen direcciones HTTP y HTTPS se omiten completamente. Además, la dirección del punto de conexión del dispositivo debe coincidir exactamente con los XAddrs HTTPS.
-   XAddrs debe ser direcciones IP o nombres de host que se puedan resolver a través de DNS. Normalmente, se usan direcciones IP.
-   Al menos una dirección IP incluida en XAddrs (o una dirección IP resuelta a partir de un nombre de host incluido en los XAddrs) debe estar en la misma subred que el adaptador sobre el que se recibió el mensaje [ProbeMatches](probematches-message.md) o [ResolveMatches.](resolvematches-message.md)
-   La dirección y el puerto especificados en el primer XAddr deben ser accesibles. WSDAPI intenta conectarse a esta dirección al establecer una conexión HTTP.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[ProbeMatches](probematches-message.md)
</dt> <dt>

[ResolveMatches](resolvematches-message.md)
</dt> <dt>

[Patrones de mensajes de Exchange de detección y metadatos](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



