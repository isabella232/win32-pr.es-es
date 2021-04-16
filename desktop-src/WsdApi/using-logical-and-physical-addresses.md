---
description: 'WS-Discovery define el direccionamiento lógico mediante URI basados en el formato urn: UUID:.'
ms.assetid: ed152f53-2996-4b90-8c4a-d187af0a598b
title: Usar direcciones lógicas y físicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ddf1dc6fe34325a90f52e43346e507d837ab3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705585"
---
# <a name="using-logical-and-physical-addresses"></a>Usar direcciones lógicas y físicas

[WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) define el direccionamiento lógico mediante URI basados en el `urn:uuid:` formato. El propósito de este esquema de direccionamiento es diferenciar la identidad del dispositivo de su dirección IP actual. En esencia, este esquema proporciona la funcionalidad de los nombres DNS sin necesidad de un servidor de nombres. El [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) recomienda que los dispositivos usen este esquema de direccionamiento.

DPWS también recomienda que los servicios usen direcciones físicas (también denominadas transporte). Esto permite a los clientes que no admiten de forma nativa mecanismos de direccionamiento WS-Discovery para comunicarse con DPWS Services. Además, cada servicio puede definir sus direcciones, lo que permite el direccionamiento de nivel de transporte para implementaciones de dispositivos que administran el envío de servicios en una capa inferior. Por último, el uso de direcciones físicas maximiza la interoperabilidad.

La desventaja del direccionamiento físico es que agrega complejidad a las implementaciones de dispositivo, ya que se debe realizar un seguimiento de la dirección IP o de transporte actual y se deben modificar los metadatos del dispositivo en consecuencia. Por esta razón, DPWS no requiere que los servicios usen direcciones de transporte.

Si se usan direcciones lógicas, hay algunos escenarios en los que el comportamiento de implementación es indefinido. La especificación WS-Discovery no describe lo que significa que un servicio resida en una dirección lógica. El R1001 de la especificación WS-Discovery recomienda no usar WS-Discovery en servicios hospedados debido a la red chatter asociada.

No se recomienda que los servicios residan en direcciones lógicas, ya que esto reduce la interoperabilidad. Si una implementación debe residir en una dirección lógica, el servicio debe usar la misma dirección lógica que el dispositivo. Si esto agrega demasiada complejidad al modelo de distribución en el dispositivo, la solución recomendada es usar parámetros de referencia para diferenciar los servicios. WSDAPI enviará mensajes correctamente a los servicios si usan la misma dirección de punto de conexión que el dispositivo.

 

 



