---
title: Protocolo de Upload BITS
description: En esta sección se describe el protocolo de red para los tipos de trabajo de carga y carga y respuesta de BITS.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01fea1ff4703dba9a0429c0b37e9c34ebe0d0099016af788c972dd8ee9fddef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021243"
---
# <a name="bits-upload-protocol"></a>Protocolo de Upload BITS

En esta sección se describe el protocolo de red para los tipos de trabajo de carga y carga y respuesta de BITS. El protocolo de carga de BITS se encuentra sobre HTTP 1.1 y usa muchos de los encabezados HTTP existentes y define nuevos encabezados. El protocolo de carga de BITS admite un único archivo de carga por sesión.

BITS usa paquetes para describir las solicitudes de cliente y las respuestas del servidor. El encabezado BITS-Packet-Type especifica el tipo de paquete que se envía. Cada paquete contiene encabezados específicos. BITS usa el verbo POST de BITS \_ para identificar los paquetes de carga de BITS. Los paquetes de respuesta siempre usan el tipo de paquete Ack, que significa confirmación. El paquete de Ack se envía en el contexto de la solicitud anterior; solo puede haber una solicitud pendiente a la vez.

Para los trabajos de carga y respuesta, BITS usa este protocolo para cargar el archivo, pero no usa este protocolo para enviar la respuesta al cliente. En su lugar, el servidor BITS envía la ubicación del archivo de respuesta al cliente y el cliente crea un trabajo de descarga de BITS para descargar el archivo de respuesta.

Use el protocolo de carga para reemplazar el software cliente o servidor bits por su propia implementación. Para obtener una lista de los paquetes de solicitud enviados por el cliente bits, vea [Paquetes de solicitud de BITS](bits-request-packets.md). Para obtener una lista de los paquetes de respuesta enviados por el servidor BITS, vea [Paquetes de respuesta de BITS](bits-response-packets.md).

El cliente determina cómo responde a errores o paquetes inesperados del servidor BITS. Si el servidor recibe un paquete que no espera, el servidor debe enviar un paquete Deck con un código de retorno 400 (solicitud no esperada).

 

 




