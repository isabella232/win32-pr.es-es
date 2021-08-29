---
description: Después de recibir un desafío del servidor, el cliente crea la respuesta del desafío digest mediante una llamada a la función InitializeSecurityContext (Digest).
ms.assetid: b26b5676-a614-4017-a4e5-a5395292a667
title: Generación de la respuesta del desafío de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5e763591294eb14fce6ac79225bbe24ba40bc875ab731c986a694df956ee356
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101305"
---
# <a name="generating-the-digest-challenge-response"></a>Generación de la respuesta del desafío de resumen

Después de recibir un desafío del servidor, el cliente crea la respuesta del desafío digest mediante una llamada a la [**función InitializeSecurityContext (Digest).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) Esta función genera una huella digital [*hash*](/windows/desktop/SecGloss/h-gly) MD5 mediante el uso de información sobre el recurso solicitado y los datos del desafío, y genera un token de seguridad que representa un contexto [*de seguridad parcial*](/windows/desktop/SecGloss/s-gly). Para completar la autenticación, el cliente debe devolver el token al servidor que emitió el desafío.

En la tabla siguiente se describen los parámetros de la función [**InitializeSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) [](/windows/desktop/SecGloss/c-gly)y los valores que se deben proporcionar al construir una respuesta de desafío de resumen.



| Parámetro                  | Descripción                                                                                                                                                                                               |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *fContextReq*<br/>   | Atributos de contexto de seguridad solicitados por el cliente. Para obtener más información, vea Requisitos del contexto de respuesta del desafío de resumen.<br/>                                                             |
| *pszTargetName*<br/> | HTTP: cadena terminada en NULL que especifica la dirección URL de destino.<br/> SASL: cadena terminada en NULL que especifica el destino DNS/SPN.<br/>                                                         |
| *pInput*<br/>        | Búferes que contienen información requerida por el SSP de resumen. Para obtener más información, vea [Búferes de entrada para la respuesta de desafío de resumen](input-buffers-for-the-digest-challenge-response.md).<br/> |
| *pfContextAttr*<br/> | Recibe los atributos admitidos por el contexto de seguridad devuelto. Para obtener más información, vea Requisitos del contexto de respuesta del desafío de resumen.<br/>                                                  |
| *pOutput*<br/>       | Dirección de un búfer de tipo \_ SECBUFFER TOKEN que recibe un token de seguridad para enviarlo de vuelta al servidor.<br/>                                                                                           |



 

## <a name="digest-challenge-response-context-requirements"></a>Requisitos de contexto de respuesta de desafío de resumen

Los requisitos de contexto son marcas que determinan:

-   Si Microsoft Digest funciona como un mecanismo SASL o un protocolo de autenticación HTTP.
-   Calidad de protección admitida por el contexto [*de seguridad compartido*](/windows/desktop/SecGloss/s-gly) por el cliente y el servidor.

De forma predeterminada, Microsoft Digest funciones como un mecanismo SASL.

Los requisitos de contexto se especifican como marcas que se pasan al *parámetro fContextReq* de la [**función InitializeSecurityContext.**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) Las marcas afectan a la calidad de protección del contexto de seguridad mediante el control de la directiva qop en la respuesta del desafío.

De forma predeterminada, la directiva qop se establece en "auth". Para generar una respuesta de desafío que establece qop en "auth-int", debe producirse lo siguiente:

1.  El desafío digest debe haber tenido una directiva qop establecida en "auth-int".
2.  El cliente debe especificar una o varias de las marcas siguientes:

    -   INTEGRIDAD DE ISC \_ REQ \_
    -   ISC \_ REQ \_ REPLAY \_ DETECT
    -   ISC \_ REQ \_ SEQUENCE \_ DETECT

Solo para SASL: genere una respuesta de desafío con la directiva qop establecida en "auth-conf" especificando la marca DE CONFIDENCIALIDAD DE ISC \_ \_ REQ. Dado que esta marca no es válida para la autenticación HTTP, no se puede usar con la marca HTTP DE ISC \_ \_ REQ.

## <a name="verifying-the-quality-of-protection"></a>Comprobación de la calidad de protección

El cliente debe examinar las marcas de atributos de contexto de seguridad devueltas en el *parámetro pfContextAttr* de la función [**InitializeSecurityContext.**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) El cliente debe enviar la respuesta de desafío al servidor solo si la calidad de protección indicada por las marcas es suficiente para sus fines. Las marcas pertinentes pueden ser cualquier combinación de lo siguiente:

-   INTEGRIDAD DE RET DE ISC \_ \_
-   ISC \_ RET \_ REPLAY \_ DETECT
-   DETECCIÓN DE \_ SECUENCIA DE RET \_ de ISC \_
-   CONFIDENCIALIDAD DE RET DE ISC \_ \_ (solo contextos SASL)

Para obtener más información sobre la directiva qop, vea [Calidad de protección y cifrado.](quality-of-protection-and-ciphers.md)

Para obtener más información sobre las directivas de respuesta a desafíos, vea [Contenido de una respuesta implícita al desafío.](contents-of-a-digest-challenge-response.md)

 

