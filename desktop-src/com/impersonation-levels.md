---
title: Niveles de suplantación (COM)
description: Si la suplantación se realiza correctamente, significa que el cliente ha acordado dejar que el servidor sea el cliente hasta cierto punto.
ms.assetid: 7539bbee-063f-4788-aece-7b70684826c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85286e5fa880ea7620d6f6ccb6107bf139ec2005
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904833"
---
# <a name="impersonation-levels"></a><span data-ttu-id="c6423-103">Niveles de suplantación</span><span class="sxs-lookup"><span data-stu-id="c6423-103">Impersonation Levels</span></span>

<span data-ttu-id="c6423-104">Si la suplantación se realiza correctamente, significa que el cliente ha acordado dejar que el servidor sea el cliente hasta cierto punto.</span><span class="sxs-lookup"><span data-stu-id="c6423-104">If impersonation succeeds, it means that the client has agreed to let the server be the client to some degree.</span></span> <span data-ttu-id="c6423-105">Los distintos grados de suplantación se denominan *niveles de suplantación* e indican la cantidad de autoridad que se asigna al servidor cuando suplanta al cliente.</span><span class="sxs-lookup"><span data-stu-id="c6423-105">The varying degrees of impersonation are called *impersonation levels*, and they indicate how much authority is given to the server when it is impersonating the client.</span></span>

<span data-ttu-id="c6423-106">Actualmente, hay cuatro niveles de suplantación: *anónimo*, *identificación*, *Suplantar* y *delegado*.</span><span class="sxs-lookup"><span data-stu-id="c6423-106">Currently, there are four impersonation levels: *anonymous*, *identify*, *impersonate*, and *delegate*.</span></span> <span data-ttu-id="c6423-107">En la lista siguiente se describe brevemente cada nivel de suplantación:</span><span class="sxs-lookup"><span data-stu-id="c6423-107">The following list briefly describes each impersonation level:</span></span>

<dl> <dt>

<span data-ttu-id="c6423-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anónimo ( \_ nivel Imp de RPC C \_ \_ \_ anónimo)</span><span class="sxs-lookup"><span data-stu-id="c6423-108"><span id="anonymous__RPC_C_IMP_LEVEL_ANONYMOUS_"></span><span id="anonymous__rpc_c_imp_level_anonymous_"></span><span id="ANONYMOUS__RPC_C_IMP_LEVEL_ANONYMOUS_"></span>anonymous (RPC\_C\_IMP\_LEVEL\_ANONYMOUS)</span></span>
</dt> <dd>

<span data-ttu-id="c6423-109">El cliente es anónimo para el servidor.</span><span class="sxs-lookup"><span data-stu-id="c6423-109">The client is anonymous to the server.</span></span> <span data-ttu-id="c6423-110">El proceso de servidor puede suplantar al cliente, pero el token de suplantación no contiene información sobre el cliente.</span><span class="sxs-lookup"><span data-stu-id="c6423-110">The server process can impersonate the client, but the impersonation token does not contain any information about the client.</span></span> <span data-ttu-id="c6423-111">Este nivel solo se admite en el transporte de comunicación local entre procesos.</span><span class="sxs-lookup"><span data-stu-id="c6423-111">This level is only supported over the local interprocess communication transport.</span></span> <span data-ttu-id="c6423-112">Todos los demás transportes promueven de forma silenciosa este nivel para identificar.</span><span class="sxs-lookup"><span data-stu-id="c6423-112">All other transports silently promote this level to identify.</span></span>

</dd> <dt>

<span data-ttu-id="c6423-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>Identify ( \_ \_ \_ identificación del nivel Imp de RPC C \_ )</span><span class="sxs-lookup"><span data-stu-id="c6423-113"><span id="identify__RPC_C_IMP_LEVEL_IDENTIFY_"></span><span id="identify__rpc_c_imp_level_identify_"></span><span id="IDENTIFY__RPC_C_IMP_LEVEL_IDENTIFY_"></span>identify (RPC\_C\_IMP\_LEVEL\_IDENTIFY)</span></span>
</dt> <dd>

<span data-ttu-id="c6423-114">Nivel predeterminado del sistema.</span><span class="sxs-lookup"><span data-stu-id="c6423-114">The system default level.</span></span> <span data-ttu-id="c6423-115">El servidor puede obtener la identidad del cliente y suplantarlo para realizar comprobaciones ACL.</span><span class="sxs-lookup"><span data-stu-id="c6423-115">The server can obtain the client's identity, and the server can impersonate the client to do ACL checks.</span></span>

</dd> <dt>

<span data-ttu-id="c6423-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>Impersonate ( \_ la \_ \_ suplantación de nivel Imp de RPC C \_ )</span><span class="sxs-lookup"><span data-stu-id="c6423-116"><span id="impersonate__RPC_C_IMP_LEVEL_IMPERSONATE_"></span><span id="impersonate__rpc_c_imp_level_impersonate_"></span><span id="IMPERSONATE__RPC_C_IMP_LEVEL_IMPERSONATE_"></span>impersonate (RPC\_C\_IMP\_LEVEL\_IMPERSONATE)</span></span>
</dt> <dd>

<span data-ttu-id="c6423-117">El servidor puede suplantar el contexto de seguridad del cliente mientras actúa en su nombre.</span><span class="sxs-lookup"><span data-stu-id="c6423-117">The server can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="c6423-118">El servidor puede obtener acceso a los recursos locales como el cliente.</span><span class="sxs-lookup"><span data-stu-id="c6423-118">The server can access local resources as the client.</span></span> <span data-ttu-id="c6423-119">Si el servidor es local, puede tener acceso a los recursos de red como el cliente.</span><span class="sxs-lookup"><span data-stu-id="c6423-119">If the server is local, it can access network resources as the client.</span></span> <span data-ttu-id="c6423-120">Si el servidor es remoto, solo podrá tener acceso a los recursos que se encuentren en el mismo equipo que el servidor.</span><span class="sxs-lookup"><span data-stu-id="c6423-120">If the server is remote, it can access only resources that are on the same computer as the server.</span></span>

</dd> <dt>

<span data-ttu-id="c6423-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>Delegado (delegado de nivel de Imp de RPC \_ C \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="c6423-121"><span id="delegate__RPC_C_IMP_LEVEL_DELEGATE_"></span><span id="delegate__rpc_c_imp_level_delegate_"></span><span id="DELEGATE__RPC_C_IMP_LEVEL_DELEGATE_"></span>delegate (RPC\_C\_IMP\_LEVEL\_DELEGATE)</span></span>
</dt> <dd>

<span data-ttu-id="c6423-122">Nivel de suplantación más completo.</span><span class="sxs-lookup"><span data-stu-id="c6423-122">The most powerful impersonation level.</span></span> <span data-ttu-id="c6423-123">Cuando se selecciona este nivel, el servidor (ya sea local o remoto) puede suplantar el contexto de seguridad del cliente mientras actúa en su nombre.</span><span class="sxs-lookup"><span data-stu-id="c6423-123">When this level is selected, the server (whether local or remote) can impersonate the client's security context while acting on behalf of the client.</span></span> <span data-ttu-id="c6423-124">Durante la suplantación, las credenciales del cliente (locales y de red) se pueden pasar a cualquier número de equipos.</span><span class="sxs-lookup"><span data-stu-id="c6423-124">During impersonation, the client's credentials (both local and network) can be passed to any number of computers.</span></span>

<span data-ttu-id="c6423-125">Para que la suplantación funcione en el nivel de delegado, deben cumplirse los siguientes requisitos:</span><span class="sxs-lookup"><span data-stu-id="c6423-125">For impersonation to work at the delegate level, the following requirements must be met:</span></span>

-   <span data-ttu-id="c6423-126">El cliente debe establecer el nivel de suplantación en \_ el \_ delegado de nivel Imp de RPC C \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c6423-126">The client must set the impersonation level to RPC\_C\_IMP\_LEVEL\_DELEGATE.</span></span>
-   <span data-ttu-id="c6423-127">La cuenta de cliente no debe estar marcada como "la cuenta es importante y no se puede delegar" en el servicio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6423-127">The client account must not be marked "Account is sensitive and cannot be delegated" in the Active Directory Service.</span></span>
-   <span data-ttu-id="c6423-128">La cuenta del servidor se debe marcar con el atributo "Trusted for delegation" en el servicio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c6423-128">The server account must be marked with the "Trusted for delegation" attribute in the Active Directory Service.</span></span>
-   <span data-ttu-id="c6423-129">Los equipos que hospedan el cliente, el servidor y los servidores de "nivel inferior" deben ejecutarse en un dominio.</span><span class="sxs-lookup"><span data-stu-id="c6423-129">The computers hosting the client, the server, and any "downstream" servers must all be running in a domain.</span></span>

</dd> </dl>

<span data-ttu-id="c6423-130">Al elegir el nivel de suplantación, el cliente indica al servidor hasta qué punto puede llegar a suplantar al cliente.</span><span class="sxs-lookup"><span data-stu-id="c6423-130">By choosing the impersonation level, the client tells the server how far it can go in impersonating the client.</span></span> <span data-ttu-id="c6423-131">El cliente establece el nivel de suplantación en el proxy que usa para comunicarse con el servidor.</span><span class="sxs-lookup"><span data-stu-id="c6423-131">The client sets the impersonation level on the proxy it uses to communicate with the server.</span></span>

## <a name="setting-the-impersonation-level"></a><span data-ttu-id="c6423-132">Establecimiento del nivel de suplantación</span><span class="sxs-lookup"><span data-stu-id="c6423-132">Setting the Impersonation Level</span></span>

<span data-ttu-id="c6423-133">Hay dos maneras de establecer el nivel de suplantación:</span><span class="sxs-lookup"><span data-stu-id="c6423-133">There are two ways to set the impersonation level:</span></span>

-   <span data-ttu-id="c6423-134">El cliente puede establecerlo en processwide, a través de una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="c6423-134">The client can set it processwide, through a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="c6423-135">Un cliente puede establecer la seguridad de nivel de proxy en una interfaz de un objeto remoto a través de una llamada a [**IClientSecurity:: SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (o la función auxiliar [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span><span class="sxs-lookup"><span data-stu-id="c6423-135">A client can set proxy-level security on an interface of a remote object through a call to [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (or the helper function [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)).</span></span>

<span data-ttu-id="c6423-136">Establezca el nivel de suplantación pasando un \_ valor XXX de nivel de Imp de RPC C adecuado \_ \_ \_ a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) a través del parámetro *dwImpLevel* .</span><span class="sxs-lookup"><span data-stu-id="c6423-136">You set the impersonation level by passing an appropriate RPC\_C\_IMP\_LEVEL\_xxx value to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) through the *dwImpLevel* parameter.</span></span>

<span data-ttu-id="c6423-137">Distintos servicios de autenticación admiten la suplantación de nivel de delegado en diferentes extensiones.</span><span class="sxs-lookup"><span data-stu-id="c6423-137">Different authentication services support delegate-level impersonation to different extents.</span></span> <span data-ttu-id="c6423-138">Por ejemplo, NTLMSSP admite la suplantación multiproceso y de nivel de delegado entre procesos, pero no entre equipos.</span><span class="sxs-lookup"><span data-stu-id="c6423-138">For instance, NTLMSSP supports cross-thread and cross-process delegate-level impersonation, but not cross-computer.</span></span> <span data-ttu-id="c6423-139">Por otro lado, el protocolo Kerberos admite la suplantación de nivel de delegado a través de los límites del equipo, mientras que Schannel no admite la suplantación en el nivel de delegado.</span><span class="sxs-lookup"><span data-stu-id="c6423-139">On the other hand, the Kerberos protocol supports delegate-level impersonation across computer boundaries, while Schannel does not support any impersonation at the delegate level.</span></span> <span data-ttu-id="c6423-140">Si tiene un proxy en el nivel de suplantación y desea establecer el nivel de suplantación en Delegate, debe llamar a [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) con las constantes predeterminadas para cada parámetro, excepto el nivel de suplantación.</span><span class="sxs-lookup"><span data-stu-id="c6423-140">If you have a proxy at impersonate level and you want to set the impersonation level to delegate, you should call [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) using the default constants for every parameter except the impersonation level.</span></span> <span data-ttu-id="c6423-141">COM elegirá NTLM localmente y el protocolo Kerberos de forma remota (cuando el protocolo Kerberos funcione).</span><span class="sxs-lookup"><span data-stu-id="c6423-141">COM will choose NTLM locally and the Kerberos protocol remotely (when the Kerberos protocol will work).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6423-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6423-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6423-143">Delegación y suplantación</span><span class="sxs-lookup"><span data-stu-id="c6423-143">Delegation and Impersonation</span></span>](delegation-and-impersonation.md)
</dt> </dl>

 

 