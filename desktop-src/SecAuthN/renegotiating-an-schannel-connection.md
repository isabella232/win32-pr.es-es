---
description: Para cambiar los atributos de una conexión, como el conjunto de cifrado o la autenticación del cliente, puede solicitar una &\# 0034; rehacer&\# 0034; o volver a negociar la conexión.
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: Renegociación de una conexión de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fbcd25dad39ab7f35e77277eee9275004cd8a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652652"
---
# <a name="renegotiating-an-schannel-connection"></a>Renegociación de una conexión de Schannel

Para cambiar los atributos de una conexión, como el conjunto de cifrado o la autenticación del cliente, puede solicitar una "Rehacer" o volver a negociar la conexión.

Si los atributos que desea cambiar se controlan mediante credenciales, debe obtener nuevas credenciales antes de volver a negociar la conexión. Para obtener más información, consulte [obtención de credenciales de Schannel](obtaining-schannel-credentials.md).

Para solicitar una rehacer desde una aplicación cliente, llame a la función [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) . Las aplicaciones de servidor llaman a la función [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) . Establezca los parámetros de la manera siguiente:

-   Especifique el [*contexto de seguridad*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) existente en el parámetro *phContext* .
-   (Solo clientes) Especifique el mismo nombre de servidor (en el parámetro *pszTargetName* ) tal y como se especificó al establecer el contexto.
-   Especifique nuevas credenciales mediante el parámetro *phCredential* , si procede.
-   Si desea cambiar los atributos de contexto no relacionados con las credenciales, especifique estos atributos mediante el parámetro *fContextReq* .

Después de llamar a la función adecuada, la aplicación debe enviar los resultados al cliente y seguir procesando los mensajes entrantes mediante la función [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) .

La función [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) devolverá los segundos \_ que \_ renegociar cuando Schannel está listo para que la aplicación pueda continuar. Cuando reciba el \_ \_ código de retorno de renegociar la SEC, la aplicación debe llamar a [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (Servers) o [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (clientes), y pasar el contenido de SECBUFFER_EXTRA devuelto desde DecryptMessage en el SECBUFFER_TOKEN. Después de que esta llamada devuelva un valor, continúe como si la aplicación estuviera creando una nueva conexión.

 

 
