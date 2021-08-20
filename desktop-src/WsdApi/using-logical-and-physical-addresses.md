---
description: WS-Discovery define el direccionamiento lógico mediante URI basados en el formato urn:uuid:.
ms.assetid: ed152f53-2996-4b90-8c4a-d187af0a598b
title: Uso de direcciones lógicas y físicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dae686a273935528a2d9ab5fcd6c5a99a90e57d2b6106ffcdd1f2a9d8deeb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920137"
---
# <a name="using-logical-and-physical-addresses"></a>Uso de direcciones lógicas y físicas

[WS-Discovery define](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) el direccionamiento lógico mediante URI basados en el `urn:uuid:` formato. El propósito de este esquema de direccionamiento es diferenciar la identidad del dispositivo de su dirección IP actual. Básicamente, este esquema proporciona la funcionalidad de los nombres DNS sin necesidad de un servidor de nombres. [El perfil de dispositivos para](https://specs.xmlsoap.org/ws/2006/02/devprof/) servicios web (DPWS) recomienda que los dispositivos usen este esquema de direccionamiento.

DPWS también recomienda que los servicios usen direcciones físicas (también denominadas transporte). Esto permite a los clientes que no admiten de forma WS-Discovery mecanismos de direccionamiento para comunicarse con los servicios DPWS. Además, cada servicio puede definir sus direcciones, lo que permite el direccionamiento de nivel de transporte para las implementaciones de dispositivos que administran el envío del servicio en una capa inferior. Por último, el uso de direcciones físicas maximiza la interoperabilidad.

La desventaja del direccionamiento físico es que agrega complejidad a las implementaciones de dispositivos, ya que se debe realizar el seguimiento de la dirección IP o de transporte actual y se deben modificar los metadatos del dispositivo en consecuencia. Por este motivo, DPWS no requiere que los servicios usen direcciones de transporte.

Si se usan direcciones lógicas, hay algunos escenarios en los que el comportamiento de implementación no está definido. La WS-Discovery especificación no describe lo que significa que un servicio resida en una dirección lógica. R1001 de la especificación WS-Discovery recomienda no usar WS-Discovery en los servicios hospedados debido a la charla de red asociada.

No se recomienda que los servicios residan en direcciones lógicas, ya que esto reduce la interoperabilidad. Si una implementación debe residir absolutamente en una dirección lógica, el servicio debe usar la misma dirección lógica que el dispositivo. Si esto agrega demasiada complejidad al modelo de distribución en el dispositivo, la solución recomendada es usar parámetros de referencia para diferenciar los servicios. WSDAPI enviará correctamente mensajes a los servicios si usan la misma dirección de punto de conexión que el dispositivo.

 

 



