---
title: Qué proveedor de seguridad usar
description: Todas las demás cosas son iguales, use \_ el \_ Protocolo RPC c authn \_ GSS \_ Kerberos o RPC \_ c \_ authn \_ GSS \_ Negotiate.
ms.assetid: 921975ae-17e7-433a-bbc5-e6b95989d31a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33248d989031390b1b57730c637829922d15166a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776105"
---
# <a name="which-security-provider-to-use"></a><span data-ttu-id="21c51-103">Qué proveedor de seguridad usar</span><span class="sxs-lookup"><span data-stu-id="21c51-103">Which Security Provider to Use</span></span>

<span data-ttu-id="21c51-104">Todas las demás cosas son iguales, use \_ el \_ Protocolo RPC c authn \_ GSS \_ Kerberos o RPC \_ c \_ authn \_ GSS \_ Negotiate.</span><span class="sxs-lookup"><span data-stu-id="21c51-104">All other things being equal, use RPC\_C\_AUTHN\_GSS\_KERBEROS or RPC\_C\_AUTHN\_GSS\_NEGOTIATE.</span></span> <span data-ttu-id="21c51-105">Cada una de ellas proporciona el servicio más seguro y escalable.</span><span class="sxs-lookup"><span data-stu-id="21c51-105">Each provides the most scalable and secure service.</span></span> <span data-ttu-id="21c51-106">Si usa \_ \_ \_ la negociación de GSS de RPC C authn \_ en el servidor, permite que los clientes de nivel inferior, como los clientes NTLM, se conecten al servidor.</span><span class="sxs-lookup"><span data-stu-id="21c51-106">If you use RPC\_C\_AUTHN\_GSS\_NEGOTIATE on the server, this allows down-level clients, such as NTLM clients, to connect to your server.</span></span> <span data-ttu-id="21c51-107">Si eso no es deseable, limite la elección a la opción de \_ \_ Kerberos C authn \_ GSS \_ solo para Kerberos, o llame a [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) para determinar qué proveedor de seguridad usa el cliente y deniegue el acceso a los clientes mediante NTLM.</span><span class="sxs-lookup"><span data-stu-id="21c51-107">If that is undesirable, either limit the choice to RPC\_C\_AUTHN\_GSS\_KERBEROS only, or call [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to determine which security provider the client is using, and deny access to clients using NTLM.</span></span> <span data-ttu-id="21c51-108">El método preferido para establecer el proveedor de seguridad que utiliza el cliente es la función [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) .</span><span class="sxs-lookup"><span data-stu-id="21c51-108">The preferred method of establishing which security provider the client is using is the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function.</span></span>

 

 




