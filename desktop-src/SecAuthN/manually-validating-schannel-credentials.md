---
description: Explica cómo validar las credenciales de Schannel manualmente.
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: Validación manual de credenciales de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71ddff50ab674825d8effd1a08477116ee0c654d031e7f353a30c95e4f1249f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787007"
---
# <a name="manually-validating-schannel-credentials"></a>Validación manual de credenciales de Schannel

De forma predeterminada, Schannel valida el certificado [*de servidor mediante*](../secgloss/s-gly.md) una llamada a la función [**WinVerifyTrust;**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) Sin embargo, si ha deshabilitado esta característica mediante la marca MANUAL CRED VALIDATION de ISC REQ, debe validar el certificado proporcionado por el servidor que está intentando establecer \_ \_ su \_ \_ identidad.

Para validar manualmente el certificado de servidor, primero debe obtenerlo. Use la [**función QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) y especifique el valor del atributo SECPKG \_ ATTR \_ REMOTE CERT \_ \_ CONTEXT. Este atributo devuelve una [**estructura CERT \_ CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) que contiene el certificado proporcionado por el servidor. Este certificado se denomina certificado de hoja porque es el último certificado de la cadena de certificados y está más lejos del [*certificado raíz.*](../secgloss/r-gly.md)

Con el certificado hoja debe comprobar lo siguiente:

-   La cadena de certificados está completa y la raíz es un certificado de una entidad de [*certificación (CA) de*](../secgloss/c-gly.md) confianza.
-   La hora actual no va más allá de las fechas de inicio y finalización de cada uno de los certificados de la cadena de certificados.
-   Ninguno de los certificados de la cadena de certificados se ha revocado.
-   La profundidad del certificado hoja no es más profunda que la profundidad máxima permitido especificada en la extensión de certificado. Esta comprobación solo es necesaria si se especifica una profundidad.
-   El uso del certificado es correcto, [](../secgloss/c-gly.md) por ejemplo, no se debe usar un certificado de cliente para autenticar un servidor.
-   Para la autenticación de servidor, la identidad del servidor contenida en el certificado hoja del servidor coincide con el servidor con el que el cliente está intentando ponerse en contacto. Normalmente, el cliente hará coincidir algún elemento del campo Nombre de sujeto del certificado con la dirección IP o el nombre DNS del servidor.

 

 
