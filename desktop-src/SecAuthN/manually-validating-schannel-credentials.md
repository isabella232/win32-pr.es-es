---
description: Explica cómo validar las credenciales de Schannel manualmente.
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: Validar manualmente las credenciales de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ec87b662cf9d3711c1ae729d2dd3b14ac5f79e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652910"
---
# <a name="manually-validating-schannel-credentials"></a>Validar manualmente las credenciales de Schannel

De forma predeterminada, Schannel valida el [*certificado de servidor*](../secgloss/s-gly.md) mediante una llamada a la función [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) ; sin embargo, si ha deshabilitado esta característica con la \_ marca de validación de credenciales manuales de REQ de ISC \_ \_ \_ , debe validar el certificado proporcionado por el servidor que está intentando establecer su identidad.

Para validar manualmente el certificado de servidor, primero debe obtenerlo. Use la función [**QueryContextAttributes (general)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) y especifique el \_ valor del \_ atributo de contexto de certificado remoto de SECPKG ATTR \_ \_ . Este atributo devuelve una estructura de [**\_ contexto de certificado**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) que contiene el certificado proporcionado por el servidor. Este certificado se denomina certificado de hoja porque es el último certificado de la cadena de certificados y está más alejado del [*certificado raíz*](../secgloss/r-gly.md).

Con el certificado hoja debe comprobar lo siguiente:

-   La cadena de certificados se ha completado y la raíz es un certificado de una [*entidad de certificación*](../secgloss/c-gly.md) (CA) de confianza.
-   La hora actual no va más allá de las fechas de inicio y finalización de cada uno de los certificados de la cadena de certificados.
-   Ninguno de los certificados de la cadena de certificados se ha revocado.
-   La profundidad del certificado de hoja no es más profunda que la profundidad máxima permitida especificada en la extensión de certificado. Esta comprobación solo es necesaria si se especifica una profundidad.
-   El uso del certificado es correcto, por ejemplo, no se debe usar un [*certificado de cliente*](../secgloss/c-gly.md) para autenticar un servidor.
-   Para la autenticación de servidor, la identidad del servidor incluida en el certificado de hoja del servidor coincide con el servidor al que el cliente intenta ponerse en contacto. Normalmente, el cliente coincidirá con algún elemento del campo de nombre de sujeto del certificado con la dirección IP o el nombre DNS del servidor.

 

 
