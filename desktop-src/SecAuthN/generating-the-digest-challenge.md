---
description: El desafío Microsoft Digest se genera mediante la llamada inicial del servidor a la función AcceptSecurityContext (síntesis).
ms.assetid: d33383c2-5c0d-401f-ab28-2a985f6508e0
title: Generar el desafío de síntesis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511ec4f01c90acf08669835f9728cc711dfd1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278586"
---
# <a name="generating-the-digest-challenge"></a>Generar el desafío de síntesis

El desafío Microsoft Digest se genera mediante la llamada inicial del servidor a la función [**AcceptSecurityContext (síntesis)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Esta llamada de función genera un valor de seguridad (nonce), que es un valor único que contiene información que se puede usar para detectar infracciones de seguridad. Esta llamada también genera un [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) parcial que se usa para mantener la información de estado. Cuando se llama a **AcceptSecurityContext (digest)** , se especifican marcas de requisitos de contexto para controlar el comportamiento de Microsoft Digest y para establecer la calidad de protección. Para obtener más información, vea [requisitos de contexto de desafío de síntesis](#digest-challenge-context-requirements).

La salida de la llamada inicial a la [*función*](/windows/desktop/SecGloss/c-gly) [**AcceptSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) es un búfer de seguridad que contiene un token que se envía al cliente con una respuesta http 401 (acceso denegado).

> [!Note]  
> Las llamadas a [**AcceptSecurityContext (digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) que no contienen información en los búferes de entrada devuelven un desafío de síntesis.

 

## <a name="digest-challenge-context-requirements"></a>Requisitos de contexto de desafío de síntesis

Los requisitos de contexto son marcas que determinan:

-   Si Microsoft Digest funciona como un mecanismo SASL o un protocolo de autenticación HTTP.
-   Calidad de protección admitida por el contexto de seguridad compartido por el cliente y el servidor.

De forma predeterminada, Microsoft Digest funciona como un mecanismo SASL. Para usarlo para la autenticación HTTP, el \_ \_ servidor debe establecer la marca ASC req http (0x10000000).

Los requisitos de contexto se especifican como marcas pasadas al parámetro *fContextReq* de la función [**AcceptSecurityContext (implícita)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) . Las marcas afectan a la calidad de protección del contexto de seguridad mediante el control de la Directiva qop en el desafío.

De forma predeterminada, la Directiva qop se establece en "auth". Para generar un desafío que establezca la Directiva qop en "auth-int", el servidor debe especificar una o varias de las marcas siguientes:

-   \_integridad de REQ de ASC \_
-   \_detección de \_ repeticiones de ASC req \_
-   \_detección de \_ secuencia de REQ de ASC \_

Solo para SASL: genera un desafío con la Directiva qop establecida en "auth-conf" mediante la especificación de la \_ marca de requisito de contexto de confidencialidad de ASC req \_ . Dado que esta marca no es válida para la autenticación HTTP, no se puede usar con la \_ marca de http req de ASC \_ .

Para obtener más información sobre la Directiva qop, vea [calidad de protección y cifrado](quality-of-protection-and-ciphers.md).

Para obtener más información sobre los desafíos, consulte [contenido de un desafío de síntesis](contents-of-a-digest-challenge.md).

 

 
