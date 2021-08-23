---
description: El Microsoft Digest desafío se genera mediante la llamada inicial del servidor a la función AcceptSecurityContext (Digest).
ms.assetid: d33383c2-5c0d-401f-ab28-2a985f6508e0
title: Generación del desafío de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a01a7edfa6498ed621e351c114e65a6d4ff6ef7a75b459cb29e00f0dc668a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623335"
---
# <a name="generating-the-digest-challenge"></a>Generación del desafío de resumen

El Microsoft Digest desafío se genera mediante la llamada inicial del servidor a la [**función AcceptSecurityContext (Digest).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Esta llamada de función genera un valor nonce, que es un valor único que contiene información que se puede usar para detectar infracciones de seguridad. Esta llamada también genera un contexto de [*seguridad parcial*](/windows/desktop/SecGloss/s-gly) que se usa para mantener la información de estado. Al llamar **a AcceptSecurityContext (Digest),** se especifican marcas de requisitos de contexto para controlar el comportamiento de Microsoft Digest y para establecer la calidad de protección. Para obtener más información, vea [Requisitos de contexto de desafío de resumen](#digest-challenge-context-requirements).

La salida de la llamada inicial a la función [**AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) [](/windows/desktop/SecGloss/c-gly) es un búfer de seguridad que contiene un token que se envía al cliente con una respuesta HTTP 401 (acceso denegado).

> [!Note]  
> Las llamadas [**a AcceptSecurityContext (Digest)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) que no contienen información en los búferes de entrada devuelven un desafío de resumen.

 

## <a name="digest-challenge-context-requirements"></a>Requisitos de contexto de desafío de resumen

Los requisitos de contexto son marcas que determinan:

-   Si Microsoft Digest funciona como un mecanismo SASL o un protocolo de autenticación HTTP.
-   Calidad de protección admitida por el contexto de seguridad compartido por el cliente y el servidor.

De forma predeterminada, Microsoft Digest funciones como un mecanismo SASL. Para usarlo para la autenticación HTTP, el servidor debe establecer la marca HTTP de ASC \_ REQ \_ (0x10000000).

Los requisitos de contexto se especifican como marcas que se pasan al *parámetro fContextReq* de la [**función AcceptSecurityContext (Digest).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) Las marcas afectan a la calidad de protección del contexto de seguridad mediante el control de la directiva qop en el desafío.

De forma predeterminada, la directiva qop se establece en "auth". Para generar un desafío que establece la directiva qop en "auth-int", el servidor debe especificar una o varias de las marcas siguientes:

-   INTEGRIDAD DE ASC \_ REQ \_
-   ASC \_ REQ \_ REPLAY \_ DETECT
-   ASC \_ REQ \_ SEQUENCE \_ DETECT

Solo para SASL: genere un desafío con la directiva qop establecida en "auth-conf" especificando la marca de requisito de contexto \_ ASC REQ \_ CONFIDENTIALITY. Dado que esta marca no es válida para la autenticación HTTP, no se puede usar con la marca \_ HTTP ASC REQ. \_

Para obtener más información sobre la directiva qop, vea [Calidad de protección y cifrados.](quality-of-protection-and-ciphers.md)

Para obtener más información sobre los desafíos, vea [Contenido de un desafío de resumen.](contents-of-a-digest-challenge.md)

 

 
