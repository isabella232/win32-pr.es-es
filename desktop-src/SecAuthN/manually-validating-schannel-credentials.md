---
description: Explica cómo validar las credenciales de Schannel manualmente.
ms.assetid: 0229486a-5812-4a7e-98ad-446292997ee3
title: Validación manual de credenciales de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ec87b662cf9d3711c1ae729d2dd3b14ac5f79e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173490"
---
# <a name="manually-validating-schannel-credentials"></a>Validación manual de credenciales de Schannel

De forma predeterminada, Schannel valida el certificado [*de servidor mediante*](../secgloss/s-gly.md) una llamada a la función [**WinVerifyTrust;**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) Sin embargo, si ha deshabilitado esta característica mediante la marca ISC \_ REQ \_ MANUAL \_ CRED VALIDATION, debe validar el certificado proporcionado por el servidor que está intentando establecer \_ su identidad.

Para validar manualmente el certificado de servidor, primero debe obtenerlo. Use la [**función QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) y especifique el valor del atributo SECPKG \_ ATTR \_ REMOTE CERT \_ \_ CONTEXT. Este atributo devuelve una [**estructura CERT \_ CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) que contiene el certificado proporcionado por el servidor. Este certificado se denomina certificado hoja porque es el último certificado de la cadena de certificados y está más lejos del [*certificado raíz.*](../secgloss/r-gly.md)

Con el certificado hoja debe comprobar lo siguiente:

-   La cadena de certificados está completa y la raíz es un certificado de una entidad de [*certificación (CA) de*](../secgloss/c-gly.md) confianza.
-   La hora actual no va más allá de las fechas de inicio y finalización de cada uno de los certificados de la cadena de certificados.
-   No se ha revocado ninguno de los certificados de la cadena de certificados.
-   La profundidad del certificado hoja no es más profunda que la profundidad máxima permitido especificada en la extensión de certificado. Esta comprobación solo es necesaria si se especifica una profundidad.
-   El uso del certificado es correcto, [](../secgloss/c-gly.md) por ejemplo, no se debe usar un certificado de cliente para autenticar un servidor.
-   Para la autenticación del servidor, la identidad del servidor contenida en el certificado hoja del servidor coincide con el servidor con el que el cliente está intentando ponerse en contacto. Normalmente, el cliente coincidirá con algún elemento del campo Nombre de sujeto del certificado con la dirección IP o el nombre DNS del servidor.

 

 
