---
title: Protocolo de carga de BITS
description: En esta sección se describe el protocolo de red para los tipos de trabajo carga de BITS y carga-respuesta.
ms.assetid: d0706ab1-1bf4-4b17-9321-ec3e00dd25e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642426decd0bc37390fa9fdd9b1ad2be11a0aa84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773680"
---
# <a name="bits-upload-protocol"></a>Protocolo de carga de BITS

En esta sección se describe el protocolo de red para los tipos de trabajo carga de BITS y carga-respuesta. El protocolo de carga de BITS está superpuesto a HTTP 1,1 y utiliza muchos de los encabezados HTTP existentes y define nuevos encabezados. El protocolo de carga de BITS admite un solo archivo de carga por sesión.

BITS usa paquetes para describir las solicitudes de cliente y las respuestas del servidor. El encabezado BITS-paquete-tipo especifica el tipo de paquete que se envía. Cada paquete contiene encabezados concretos. BITS utiliza el \_ verbo post de bits para identificar los paquetes de carga de bits. Los paquetes de respuesta siempre usan el tipo de paquete ACK que representa la confirmación. El paquete de confirmación se envía en el contexto de la solicitud anterior; solo puede haber una solicitud pendiente al mismo tiempo.

En el caso de los trabajos de carga y respuesta, BITS usa este protocolo para cargar el archivo, pero no usa este protocolo para enviar la respuesta al cliente. En su lugar, el servidor BITS envía la ubicación del archivo de respuesta al cliente y el cliente crea un trabajo de descarga de BITS para descargar el archivo de respuesta.

Use el protocolo de carga para reemplazar el software de cliente o servidor de BITS por su propia implementación. Para obtener una lista de los paquetes de solicitud enviados por el cliente BITS, consulte [paquetes de solicitud de bits](bits-request-packets.md). Para obtener una lista de los paquetes de respuesta enviados por el servidor BITS, consulte [paquetes de respuesta de bits](bits-response-packets.md).

El cliente determina el modo en que responde a errores o paquetes inesperados del servidor BITS. Si el servidor recibe un paquete que no espera, el servidor debe enviar un paquete de confirmación con un código de retorno 400 (solicitud incorrecta).

 

 




