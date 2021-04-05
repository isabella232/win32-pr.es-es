---
description: Después de recibir un desafío del servidor, el cliente crea la respuesta del desafío de síntesis mediante una llamada a la función InitializeSecurityContext (síntesis).
ms.assetid: b26b5676-a614-4017-a4e5-a5395292a667
title: Generar la respuesta de desafío de síntesis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b577334348745425db23d3de41431ba4e37b7af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912494"
---
# <a name="generating-the-digest-challenge-response"></a>Generar la respuesta de desafío de síntesis

Después de recibir un desafío del servidor, el cliente crea la respuesta del desafío de síntesis mediante una llamada a la función [**InitializeSecurityContext (síntesis)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Esta función genera una huella digital de [*hash*](/windows/desktop/SecGloss/h-gly) MD5 usando información sobre el recurso y los datos solicitados del desafío y genera un token de seguridad que representa un [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly)parcial. Para completar la autenticación, el cliente debe devolver el token al servidor que emitió el desafío.

En la tabla siguiente se describen los parámetros de la [*función*](/windows/desktop/SecGloss/c-gly) [**InitializeSecurityContext (síntesis)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) y los valores que se deben proporcionar al construir una respuesta de desafío de síntesis.



| Parámetro                  | Descripción                                                                                                                                                                                               |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *fContextReq*<br/>   | Atributos de contexto de seguridad solicitados por el cliente. Para obtener más información, vea requisitos de contexto de respuesta de desafío de síntesis.<br/>                                                             |
| *pszTargetName*<br/> | HTTP: cadena terminada en null que especifica la dirección URL de destino.<br/> SASL: cadena terminada en null que especifica el destino DNS o SPN.<br/>                                                         |
| *pInput*<br/>        | Búferes que contienen información requerida por el SSP de síntesis. Para obtener más información, consulte [búferes de entrada para la respuesta de desafío de síntesis](input-buffers-for-the-digest-challenge-response.md).<br/> |
| *pfContextAttr*<br/> | Recibe los atributos admitidos por el contexto de seguridad devuelto. Para obtener más información, vea requisitos de contexto de respuesta de desafío de síntesis.<br/>                                                  |
| *pOutput*<br/>       | Dirección de un búfer de tipo de token de SECBUFFER \_ que recibe un token de seguridad para devolverlo al servidor.<br/>                                                                                           |



 

## <a name="digest-challenge-response-context-requirements"></a>Requisitos de contexto de respuesta de desafío de síntesis

Los requisitos de contexto son marcas que determinan:

-   Si Microsoft Digest funciona como un mecanismo SASL o un protocolo de autenticación HTTP.
-   Calidad de protección admitida por el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) compartido por el cliente y el servidor.

De forma predeterminada, Microsoft Digest funciona como un mecanismo SASL.

Los requisitos de contexto se especifican como marcas que se pasan al parámetro *fContextReq* de la función [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . Las marcas afectan a la calidad de protección del contexto de seguridad mediante el control de la Directiva qop en la respuesta de desafío.

De forma predeterminada, la Directiva qop se establece en "auth". Para generar una respuesta de desafío que establezca qop en "auth-int", debe ocurrir lo siguiente:

1.  El desafío de síntesis debe haber tenido una directiva qop establecida en "auth-int".
2.  El cliente debe especificar una o varias de las marcas siguientes:

    -   \_integridad de REQ de ISC \_
    -   detección de la reproducción de REQ de ISC \_ \_ \_
    -   \_detección de \_ secuencia de REQ de ISC \_

Solo para SASL: genere una respuesta de desafío con la Directiva qop establecida en "auth-conf" especificando la \_ marca de confidencialidad de REQ de ISC \_ . Dado que esta marca no es válida para la autenticación HTTP, no se puede usar con \_ la \_ marca http req de ISC.

## <a name="verifying-the-quality-of-protection"></a>Comprobar la calidad de la protección

El cliente debe examinar las marcas de atributos de contexto de seguridad devueltas en el parámetro *pfContextAttr* de la función [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) . El cliente debe enviar la respuesta de desafío al servidor solo si la calidad de protección indicada por las marcas es suficiente para sus fines. Las marcas relevantes pueden ser cualquier combinación de lo siguiente:

-   integridad de ISC \_ RET \_
-   detección de reproducción de ISC \_ RET \_ \_
-   detección de secuencia de ISC \_ RET \_ \_
-   \_Confidencialidad de ISC RET \_ (solo contextos SASL)

Para obtener más información sobre la Directiva qop, vea [calidad de protección y cifrado](quality-of-protection-and-ciphers.md).

Para obtener más información sobre las directivas de respuesta a desafíos, consulte [contenido de una respuesta de desafío de síntesis](contents-of-a-digest-challenge-response.md).

 

