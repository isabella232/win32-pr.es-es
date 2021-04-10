---
title: Servicios de seguridad de MSMQ
description: Los mensajes RPC sincrónicos pueden utilizar cualquiera de las características de seguridad disponibles en el tiempo de ejecución de RPC. Consulte seguridad para obtener más detalles.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149446"
---
# <a name="msmq-security-services"></a><span data-ttu-id="6f163-104">Servicios de seguridad de MSMQ</span><span class="sxs-lookup"><span data-stu-id="6f163-104">MSMQ Security Services</span></span>

<span data-ttu-id="6f163-105">Los mensajes RPC sincrónicos pueden utilizar cualquiera de las características de seguridad disponibles en el tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="6f163-105">Synchronous RPC messages can use any of the security features available from the RPC run time.</span></span> <span data-ttu-id="6f163-106">Consulte [seguridad](security.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="6f163-106">See [Security](security.md) for more details.</span></span>

<span data-ttu-id="6f163-107">Las llamadas asincrónicas \[ [](/windows/desktop/Midl/message) \] a mensajes no pueden utilizar la seguridad RPC porque no hay ningún protocolo de enlace entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="6f163-107">Asynchronous \[ [message](/windows/desktop/Midl/message)\] calls cannot use RPC security because there is no handshake between client and server.</span></span> <span data-ttu-id="6f163-108">De hecho, es posible que el servidor no se esté ejecutando en el momento de la llamada.</span><span class="sxs-lookup"><span data-stu-id="6f163-108">In fact, the server may not even be running at the time of the call.</span></span> <span data-ttu-id="6f163-109">Para tener acceso a los servicios de seguridad proporcionados por servicios de Message Queuing (MSMQ), la aplicación cliente debe llamar a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) para controlar el nivel de autenticación y privacidad de sus llamadas al servidor.</span><span class="sxs-lookup"><span data-stu-id="6f163-109">To access the security services provided by Message Queuing Services (MSMQ), the client application should call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) to control the level of authentication and privacy for its calls to the server.</span></span>

<span data-ttu-id="6f163-110">La aplicación de servidor puede llamar a [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) desde dentro de una llamada a procedimiento remoto para determinar el nivel de seguridad de esa llamada.</span><span class="sxs-lookup"><span data-stu-id="6f163-110">The server application can call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) from within a remote procedure call to determine the security level for that call.</span></span> <span data-ttu-id="6f163-111">En la tabla siguiente se muestra la asignación entre las constantes de seguridad de RPC y la seguridad de MSMQ.</span><span class="sxs-lookup"><span data-stu-id="6f163-111">The mapping between RPC security constants and MSMQ security is shown in the following table.</span></span>



| <span data-ttu-id="6f163-112">Nivel de seguridad de RPC</span><span class="sxs-lookup"><span data-stu-id="6f163-112">RPC security level</span></span>                | <span data-ttu-id="6f163-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f163-113">Description</span></span>                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f163-114">\_ \_ nivel ninguno de autenticación \_ RPC</span><span class="sxs-lookup"><span data-stu-id="6f163-114">RPC\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="6f163-115">La llamada no se ha autenticado ni cifrado.</span><span class="sxs-lookup"><span data-stu-id="6f163-115">The call is not authenticated or encrypted.</span></span>                                                |
| <span data-ttu-id="6f163-116">integridad de la PKT de nivel de autenticación de RPC \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6f163-116">RPC\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="6f163-117">La llamada se autentica mediante la seguridad de MSMQ.</span><span class="sxs-lookup"><span data-stu-id="6f163-117">The call is authenticated using MSMQ security.</span></span>                                             |
| <span data-ttu-id="6f163-118">privacidad de nivel de autenticación de RPC \_ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="6f163-118">RPC\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="6f163-119">La llamada se autentica y se cifra mientras viaja entre la cola del cliente y del servidor.</span><span class="sxs-lookup"><span data-stu-id="6f163-119">The call is authenticated and encrypted as it travels between the client and server queue.</span></span> |



 

<span data-ttu-id="6f163-120">El servidor también puede forzar la autenticación y el cifrado de llamadas mediante una llamada a [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) y el establecimiento de las marcas de privacidad de nivel de autenticación de RPC c MQ authn nivel \_ \_ \_ \_ \_ ninguno, RPC \_ c \_ MQ \_ authn \_ \_ \_ y RPC \_ c \_ MQ \_ authn \_ \_ \_ en la estructura de [**\_ directivas RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) .</span><span class="sxs-lookup"><span data-stu-id="6f163-120">The server can also force call authentication and encryption by calling [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) and setting the RPC\_C\_MQ\_AUTHN\_LEVEL\_NONE, RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_INTEGRITY and RPC\_C\_MQ\_AUTHN\_LEVEL\_PKT\_PRIVACY flags in the [**RPC\_POLICY**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) structure.</span></span>

 

 