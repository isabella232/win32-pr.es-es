---
description: Para cambiar los atributos de una conexión, como el conjunto de cifrado o la autenticación de cliente, puede solicitar un &\# 0034;rehacer&\# 0034; o renegociar la conexión.
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: Renegociación de una conexión de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b904400f5a440046214c39ea736c296685e0e56859f43b3a458f621d2a07d273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919404"
---
# <a name="renegotiating-an-schannel-connection"></a>Renegociación de una conexión de Schannel

Para cambiar los atributos de una conexión, como el conjunto de cifrado o la autenticación de cliente, puede solicitar una "rehacer" o volver a negociar la conexión.

Si los atributos que desea cambiar están controlados por credenciales, debe obtener nuevas credenciales antes de volver a negociar la conexión. Para obtener más información, vea [Obtención de credenciales de Schannel.](obtaining-schannel-credentials.md)

Para solicitar una rehacer desde una aplicación cliente, llame a la [**función InitializeSecurityContext (Schannel).**](./initializesecuritycontext--schannel.md) Las aplicaciones de servidor [**llaman a la función AcceptSecurityContext (Schannel).**](acceptsecuritycontext--schannel.md) Establezca los parámetros de la manera siguiente:

-   Especifique el contexto [*de seguridad existente*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) en el parámetro *phContext.*
-   (Solo clientes) Especifique el mismo nombre de servidor (en el *parámetro pszTargetName)* que se especificó al establecer el contexto.
-   Especifique nuevas credenciales mediante el *parámetro phCredential,* si procede.
-   Si desea cambiar los atributos de contexto no relacionados con las credenciales, especifique estos atributos mediante el *parámetro fContextReq.*

Después de llamar a la función adecuada, la aplicación debe enviar los resultados al cliente y continuar procesando los mensajes entrantes mediante la [**función DecryptMessage (Schannel).**](decryptmessage--schannel.md)

La [**función DecryptMessage (Schannel)**](decryptmessage--schannel.md) devolverá SEC \_ I \_ RENEGOTIATE cuando Schannel esté listo para que la aplicación continúe. Cuando recibe el código de retorno SEC I RENEGOTIATE, la aplicación debe llamar \_ \_ a [**AcceptSecurityContext (Schannel) (servidores)**](acceptsecuritycontext--schannel.md) o [**InitializeSecurityContext (Schannel) (clientes)**](./initializesecuritycontext--schannel.md) y pasar el contenido de SECBUFFER_EXTRA devuelto desde DecryptMessage en el SECBUFFER_TOKEN. Después de que esta llamada devuelva un valor, continúe como si la aplicación estuviera creando una nueva conexión.

 

 
