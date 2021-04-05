---
description: Los contextos de secuencia controlan los protocolos orientados a secuencias seguros, como SSL o PCT.
ms.assetid: 05a6b036-1f7f-473f-9813-a1e1534e0f0d
title: Contextos de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53103dc1269c05e5a2c162133d21e167d8035c2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001562"
---
# <a name="stream-contexts"></a>Contextos de secuencia

Los contextos de secuencia controlan los protocolos orientados a secuencias seguros, como SSL o PCT. En interés de compartir la misma interfaz y la administración similar de credenciales, SSPI proporciona compatibilidad con los contextos de secuencia. El [*Protocolo de seguridad*](../secgloss/s-gly.md) incorpora el esquema de autenticación de secuencias y los formatos de registro.

Para proporcionar protocolos orientados a secuencias, los [*paquetes de seguridad*](../secgloss/s-gly.md) que admiten contextos de secuencia tienen las siguientes características de proceso:

-   El paquete establece la marca de flujo de la \_ marca SECPKG \_ para indicar que admite la semántica de secuencias.
-   Las aplicaciones de transporte solicitan la semántica de los flujos estableciendo la secuencia de REQ de ISC \_ \_ y las \_ \_ marcas de flujo de REQ de ASC en las llamadas a las funciones [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) y [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
-   La aplicación llama a la función [**QueryContextAttributes (general)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) con una estructura [**SecPkgContext \_ StreamSizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_streamsizes) para consultar el [*contexto de seguridad*](../secgloss/s-gly.md) para el número de búferes que se van a proporcionar y los tamaños que se reservan para los encabezados o finalizadores.
-   La aplicación proporciona descriptores de búfer para la reserva durante el procesamiento real de los datos. Al especificar la semántica de los flujos, el autor de la llamada indica la disposición de realizar un procesamiento adicional para que el [*paquete de seguridad*](../secgloss/s-gly.md) pueda controlar el bloqueo de los mensajes. En esencia, para las funciones [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) , el autor de la llamada pasa una lista de búferes. Cuando se recibe un mensaje de un canal orientado a secuencias (por ejemplo, un puerto TCP), el autor de la llamada pasa una lista de búferes como se indica a continuación.

    | Buffer | Length         | Tipo de búfer      |
    |--------|----------------|------------------|
    | 1      | Longitud del mensaje | datos de SECBUFFER \_  |
    | 2      | 0              | SECBUFFER \_ vacío |
    | 3      | 0              | SECBUFFER \_ vacío |
    | 4      | 0              | SECBUFFER \_ vacío |
    | 5      | 0              | SECBUFFER \_ vacío |

    

     

    Después, el paquete de seguridad funciona en el [*BLOB*](../secgloss/b-gly.md). Si la función se devuelve correctamente, la lista de búferes tiene un aspecto similar al siguiente.

    

    | Buffer | Length         | Tipo de búfer                |
    |--------|----------------|----------------------------|
    | 1      | Longitud del encabezado  | SECBUFFER \_ encabezado de secuencia \_  |
    | 2      | Longitud de los datos    | datos de SECBUFFER \_            |
    | 3      | Longitud del finalizador | \_finalizador de flujo SECBUFFER \_ |
    | 4      | 0              | SECBUFFER \_ vacío           |
    | 5      | 0              | SECBUFFER \_ vacío           |

    

     

    El paquete también podría haber devuelto el búfer \# 4 con la longitud x y el tipo de búfer SECBUFFER \_ extra, lo que indica que los datos de este búfer forman parte del Registro siguiente y aún no se han procesado. Por el contrario, si la función de mensaje devuelve el \_ código de error de mensaje s E \_ incompleto \_ , la lista de búferes devuelta sería similar a la siguiente.

    

    | Buffer | Length | Tipo de búfer        |
    |--------|--------|--------------------|
    | 1      | x      | \_falta SECBUFFER |

    

     

    Esto indica que se necesitan más datos para procesar el registro. A diferencia de la mayoría de los errores devueltos por una función de mensaje, este tipo de búfer no indica que el contexto se ha puesto en peligro. En su lugar, indica que se necesitan más datos. los [*paquetes de seguridad*](../secgloss/s-gly.md) no deben actualizar su [*Estado*](../secgloss/s-gly.md) en esta condición.

    Del mismo modo, en el lado del remitente de la comunicación, el autor de la llamada puede llamar a la función [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) . Es posible que el paquete de seguridad tenga que reasignar el búfer o copiar los elementos. El autor de la llamada puede ser más eficaz al proporcionar una lista de búferes como se indica a continuación.

    

    | Buffer | Length         | Tipo                       |
    |--------|----------------|----------------------------|
    | 1      | Longitud del encabezado  | SECBUFFER \_ encabezado de secuencia \_  |
    | 2      | Longitud de los datos    | datos de SECBUFFER \_            |
    | 3      | Longitud del finalizador | \_finalizador de flujo SECBUFFER \_ |

    

     

    Esto permite que el llamador utilice los búferes de manera más eficaz. Al llamar a la función [**QueryContextAttributes**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) para determinar la cantidad de espacio que se va a reservar antes de llamar a [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), la operación es más eficaz para la aplicación y el paquete de seguridad.

 

 
