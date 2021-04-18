---
description: Negociación del nivel de autenticación
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: Negociación del nivel de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b9983bd2a2df1d85cc6df4bfc0ba2a757b200f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705389"
---
# <a name="negotiation-of-authentication-level"></a><span data-ttu-id="016fe-103">Negociación del nivel de autenticación</span><span class="sxs-lookup"><span data-stu-id="016fe-103">Negotiation of Authentication Level</span></span>

<span data-ttu-id="016fe-104">Tanto el cliente como el servidor deben participar en la autenticación y cada parte indica que desea realizar un cierto nivel de autenticación.</span><span class="sxs-lookup"><span data-stu-id="016fe-104">Both client and server must participate in authentication, and each party indicates that it wants to perform a certain level of authentication.</span></span> <span data-ttu-id="016fe-105">Al principio de una llamada, el nivel de autenticación se negocia entre las dos partes, se elige un servicio adecuado y la llamada se autentica y continúa (con posible cifrado, según el nivel de autenticación elegido).</span><span class="sxs-lookup"><span data-stu-id="016fe-105">At the beginning of a call, the authentication level is negotiated between the two parties, an appropriate service is chosen, and the call is authenticated and proceeds (with possible encryption, depending on the authentication level chosen).</span></span> <span data-ttu-id="016fe-106">El nivel de autenticación negociado entre el cliente y el servidor se determina como máximo (*preferencia de cliente*, *preferencia de servidor*).</span><span class="sxs-lookup"><span data-stu-id="016fe-106">The authentication level negotiated between client and server is determined as Maximum(*Client preference*, *Server preference*).</span></span> <span data-ttu-id="016fe-107">El efecto de esto significa que el servidor siempre puede dictar un nivel mínimo de autenticación con el que se sienta cómodo; es decir, la autenticación se puede dictar administrativamente desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="016fe-107">The effect of this means that the server can always dictate a minimum level of authentication that it is comfortable with; that is, authentication can be administratively dictated from the server.</span></span>

<span data-ttu-id="016fe-108">El cliente especifica que desea realizar la autenticación en cierto nivel como con cualquier aplicación COM.</span><span class="sxs-lookup"><span data-stu-id="016fe-108">The client specifies that it wants to perform authentication at a certain level as with any COM application.</span></span> <span data-ttu-id="016fe-109">El nivel de autenticación del cliente se puede indicar de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="016fe-109">The client authentication level can be indicated as follows:</span></span>

-   <span data-ttu-id="016fe-110">Por equipo cliente, con el nivel de autenticación COM en todo el equipo establecido mediante [dcomcnfg](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) o la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="016fe-110">Per client machine, with the machine-wide COM authentication level set by using either [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) or the Component Services administrative tool.</span></span>
-   <span data-ttu-id="016fe-111">Por aplicación cliente administrativamente, con [dcomcnfg](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) o con la herramienta administrativa Servicios de componentes si el cliente debe ser una aplicación com+.</span><span class="sxs-lookup"><span data-stu-id="016fe-111">Per client application administratively, using [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) or using the Component Services administrative tool if the client should be a COM+ application.</span></span>
-   <span data-ttu-id="016fe-112">Por proceso de cliente mediante programación, con [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="016fe-112">Per client process programmatically, with [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="016fe-113">En cualquier momento mediante programación, usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="016fe-113">At any point programmatically, using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="016fe-114">La aplicación de servidor COM+ especifica un nivel de autenticación administrativa mediante la herramienta administrativa Servicios de componentes (o a través de un script administrativo).</span><span class="sxs-lookup"><span data-stu-id="016fe-114">The COM+ server application specifies an authentication level administratively by using the Component Services administrative tool (or through an administrative script).</span></span>

<span data-ttu-id="016fe-115">La negociación de la autenticación para una llamada continúa en la secuencia siguiente:</span><span class="sxs-lookup"><span data-stu-id="016fe-115">Negotiating authentication for a call proceeds in the following sequence:</span></span>

1.  <span data-ttu-id="016fe-116">El nivel de autenticación se elige como MAX (*cliente*, *servidor*).</span><span class="sxs-lookup"><span data-stu-id="016fe-116">Authentication level is chosen as MAX(*client*, *server*).</span></span>
2.  <span data-ttu-id="016fe-117">Negociación del Protocolo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="016fe-117">Negotiation of authentication protocol.</span></span>
3.  <span data-ttu-id="016fe-118">El servidor autentica la identidad del cliente.</span><span class="sxs-lookup"><span data-stu-id="016fe-118">Server authenticates client identity.</span></span>
4.  <span data-ttu-id="016fe-119">Opcionalmente, el cliente autentica la identidad del servidor, según el protocolo de autenticación.</span><span class="sxs-lookup"><span data-stu-id="016fe-119">Optionally, client authenticates server identity, depending on the authentication protocol.</span></span>
5.  <span data-ttu-id="016fe-120">Las llamadas a métodos se comunican con el nivel de autenticación elegido.</span><span class="sxs-lookup"><span data-stu-id="016fe-120">Method calls are communicated with the chosen level of authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="016fe-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="016fe-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="016fe-122">Autenticación de cliente</span><span class="sxs-lookup"><span data-stu-id="016fe-122">Client Authentication</span></span>](client-authentication.md)
</dt> </dl>

 

 
