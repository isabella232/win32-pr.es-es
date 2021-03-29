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
# <a name="renegotiating-an-schannel-connection"></a><span data-ttu-id="6e68f-103">Renegociación de una conexión de Schannel</span><span class="sxs-lookup"><span data-stu-id="6e68f-103">Renegotiating an Schannel Connection</span></span>

<span data-ttu-id="6e68f-104">Para cambiar los atributos de una conexión, como el conjunto de cifrado o la autenticación del cliente, puede solicitar una "Rehacer" o volver a negociar la conexión.</span><span class="sxs-lookup"><span data-stu-id="6e68f-104">To change a connection's attributes, such as the cipher suite or client authentication, you can request a "redo" or renegotiation of the connection.</span></span>

<span data-ttu-id="6e68f-105">Si los atributos que desea cambiar se controlan mediante credenciales, debe obtener nuevas credenciales antes de volver a negociar la conexión.</span><span class="sxs-lookup"><span data-stu-id="6e68f-105">If the attributes you want to change are controlled by credentials, you must obtain new credentials before you renegotiate the connection.</span></span> <span data-ttu-id="6e68f-106">Para obtener más información, consulte [obtención de credenciales de Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="6e68f-106">For more information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

<span data-ttu-id="6e68f-107">Para solicitar una rehacer desde una aplicación cliente, llame a la función [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="6e68f-107">To request a redo from a client application, call the [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="6e68f-108">Las aplicaciones de servidor llaman a la función [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="6e68f-108">Server applications call the [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) function.</span></span> <span data-ttu-id="6e68f-109">Establezca los parámetros de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="6e68f-109">Set the parameters as follows:</span></span>

-   <span data-ttu-id="6e68f-110">Especifique el [*contexto de seguridad*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) existente en el parámetro *phContext* .</span><span class="sxs-lookup"><span data-stu-id="6e68f-110">Specify the existing [*security context*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) in the *phContext* parameter.</span></span>
-   <span data-ttu-id="6e68f-111">(Solo clientes) Especifique el mismo nombre de servidor (en el parámetro *pszTargetName* ) tal y como se especificó al establecer el contexto.</span><span class="sxs-lookup"><span data-stu-id="6e68f-111">(Clients only) Specify the same server name (in the *pszTargetName* parameter) as specified when establishing the context.</span></span>
-   <span data-ttu-id="6e68f-112">Especifique nuevas credenciales mediante el parámetro *phCredential* , si procede.</span><span class="sxs-lookup"><span data-stu-id="6e68f-112">Specify new credentials, using the *phCredential* parameter, if applicable.</span></span>
-   <span data-ttu-id="6e68f-113">Si desea cambiar los atributos de contexto no relacionados con las credenciales, especifique estos atributos mediante el parámetro *fContextReq* .</span><span class="sxs-lookup"><span data-stu-id="6e68f-113">If you want to change context attributes unrelated to the credentials, specify these attributes using the *fContextReq* parameter.</span></span>

<span data-ttu-id="6e68f-114">Después de llamar a la función adecuada, la aplicación debe enviar los resultados al cliente y seguir procesando los mensajes entrantes mediante la función [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) .</span><span class="sxs-lookup"><span data-stu-id="6e68f-114">After calling the appropriate function, your application should send the results to the client and continue processing incoming messages using the [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) function.</span></span>

<span data-ttu-id="6e68f-115">La función [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) devolverá los segundos \_ que \_ renegociar cuando Schannel está listo para que la aplicación pueda continuar.</span><span class="sxs-lookup"><span data-stu-id="6e68f-115">The [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) function will return SEC\_I\_RENEGOTIATE when Schannel is ready for your application to proceed.</span></span> <span data-ttu-id="6e68f-116">Cuando reciba el \_ \_ código de retorno de renegociar la SEC, la aplicación debe llamar a [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (Servers) o [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (clientes), y pasar el contenido de SECBUFFER_EXTRA devuelto desde DecryptMessage en el SECBUFFER_TOKEN.</span><span class="sxs-lookup"><span data-stu-id="6e68f-116">When you receive the SEC\_I\_RENEGOTIATE return code, your application must call [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (servers) or [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (clients), and pass the contents of SECBUFFER_EXTRA returned from DecryptMessage in the SECBUFFER_TOKEN.</span></span> <span data-ttu-id="6e68f-117">Después de que esta llamada devuelva un valor, continúe como si la aplicación estuviera creando una nueva conexión.</span><span class="sxs-lookup"><span data-stu-id="6e68f-117">After this call returns a value, proceed as though your application were creating a new connection.</span></span>

 

 
