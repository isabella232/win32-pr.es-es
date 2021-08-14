---
description: Los contextos de flujo controlan los protocolos seguros orientados a flujos, como SSL o PCT.
ms.assetid: 05a6b036-1f7f-473f-9813-a1e1534e0f0d
title: Contextos de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c843889df6aec3f82e8cb8516a7c23ccbf7a6de9957f9a0c572f6e6ca63ac75d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916684"
---
# <a name="stream-contexts"></a>Contextos de secuencia

Los contextos de flujo controlan los protocolos seguros orientados a flujos, como SSL o PCT. Con el interés de compartir la misma interfaz y una administración de credenciales similar, SSPI proporciona compatibilidad con contextos de flujo. El [*protocolo de seguridad*](../secgloss/s-gly.md) incorpora el esquema de autenticación de flujo y los formatos de registro.

Para proporcionar protocolos orientados [](../secgloss/s-gly.md) a secuencias, los paquetes de seguridad que admiten contextos de flujo tienen las siguientes características de proceso:

-   El paquete establece la marca SECPKG \_ FLAG STREAM para indicar que admite la semántica de \_ secuencias.
-   Las aplicaciones de transporte solicitan semántica de flujo estableciendo las marcas STREAM de ISC REQ STREAM y ASC REQ STREAM en las llamadas a las funciones \_ \_ \_ \_ [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) y [**AcceptSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
-   La aplicación llama a la función [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) con una [](../secgloss/s-gly.md) estructura [**SecPkgContext \_ StreamSizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes) para consultar el contexto de seguridad del número de búferes que se deben proporcionar y los tamaños que se reservan para encabezados o finalizadores.
-   La aplicación proporciona descriptores de búfer que se pueden ahorrar durante el procesamiento real de los datos. Al especificar la semántica de flujo, el autor de [](../secgloss/s-gly.md) la llamada indica la disposición a realizar un procesamiento adicional para que el paquete de seguridad pueda controlar el bloqueo de los mensajes. Básicamente, para las [**funciones MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature,**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) el autor de la llamada pasa una lista de búferes. Cuando se recibe un mensaje de un canal orientado a secuencias (por ejemplo, un puerto TCP), el autor de la llamada pasa una lista de búferes como se indica a continuación.

    | Buffer | Length         | Tipo de búfer      |
    |--------|----------------|------------------|
    | 1      | Longitud del mensaje | DATOS \_ SECBUFFER  |
    | 2      | 0              | SECBUFFER \_ EMPTY |
    | 3      | 0              | SECBUFFER \_ EMPTY |
    | 4      | 0              | SECBUFFER \_ EMPTY |
    | 5      | 0              | SECBUFFER \_ EMPTY |

    

     

    A continuación, el paquete de seguridad funciona en [*el blob*](../secgloss/b-gly.md). Si la función se devuelve correctamente, la lista de búferes tiene un aspecto similar al siguiente.

    

    | Buffer | Length         | Tipo de búfer                |
    |--------|----------------|----------------------------|
    | 1      | Longitud del encabezado  | SECBUFFER \_ STREAM \_ HEADER  |
    | 2      | Longitud de los datos    | DATOS \_ SECBUFFER            |
    | 3      | Longitud del finalizador | FINALIZADOR DE \_ SECUENCIAS DE \_ SECBUFFER |
    | 4      | 0              | SECBUFFER \_ EMPTY           |
    | 5      | 0              | SECBUFFER \_ EMPTY           |

    

     

    El paquete también podría haber devuelto el búfer 4 con la longitud x y el tipo de búfer SECBUFFER EXTRA, lo que indica que los datos de este búfer forman parte del registro siguiente y aún no se han \# \_ procesado. Por el contrario, si la función de mensaje devuelve el código de error SEC E INCOMPLETE MESSAGE, la lista de búferes devuelta \_ tendría un aspecto parecido al \_ \_ siguiente.

    

    | Buffer | Length | Tipo de búfer        |
    |--------|--------|--------------------|
    | 1      | x      | FALTA \_ SECBUFFER |

    

     

    Esto indica que se necesitaron más datos para procesar el registro. A diferencia de la mayoría de los errores devueltos por una función de mensaje, este tipo de búfer no indica que el contexto se haya puesto en peligro. En su lugar, indica que se necesitan más datos. [*los paquetes*](../secgloss/s-gly.md) de seguridad no deben actualizar [*su estado*](../secgloss/s-gly.md) en esta condición.

    De forma similar, en el lado remitente de la comunicación, el autor de la llamada puede llamar a la [**función MakeSignature.**](/windows/desktop/api/Sspi/nf-sspi-makesignature) Es posible que el paquete de seguridad tenga que volver alocar el búfer o copiar cosas. El autor de la llamada puede ser más eficaz proporcionando una lista de búferes como se muestra a continuación.

    

    | Buffer | Length         | Tipo                       |
    |--------|----------------|----------------------------|
    | 1      | Longitud del encabezado  | SECBUFFER \_ STREAM \_ HEADER  |
    | 2      | Longitud de los datos    | DATOS \_ SECBUFFER            |
    | 3      | Longitud del finalizador | FINALIZADOR DE \_ SECUENCIAS DE \_ SECBUFFER |

    

     

    Esto permite al autor de la llamada usar los búferes de forma más eficaz. Al llamar a [**la función QueryContextAttributes**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) para determinar la cantidad de espacio que se reserva antes de llamar a [**MakeSignature,**](/windows/desktop/api/Sspi/nf-sspi-makesignature)la operación es más eficaz para la aplicación y el paquete de seguridad.

 

 
