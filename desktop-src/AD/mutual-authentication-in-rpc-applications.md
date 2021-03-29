---
title: Autenticación mutua en aplicaciones RPC
description: Los servicios RPC pueden usar puntos de conexión de servicio para publicarse por sí mismos o pueden usar las API del servicio de nombres de RPC (RpcNs).
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Autenticación mutua en aplicaciones RPC AD
- Active Directory, usar, autenticación mutua, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a8591056293c916205b5b600c1b1a061d169f0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904487"
---
# <a name="mutual-authentication-in-rpc-applications"></a><span data-ttu-id="1ec46-105">Autenticación mutua en aplicaciones RPC</span><span class="sxs-lookup"><span data-stu-id="1ec46-105">Mutual Authentication in RPC Applications</span></span>

<span data-ttu-id="1ec46-106">Los servicios RPC pueden usar puntos de conexión de servicio para publicarse por sí mismos o pueden usar las API del servicio de nombres de RPC (RpcNs).</span><span class="sxs-lookup"><span data-stu-id="1ec46-106">RPC services can use service connection points to publish themselves, or they can use the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="1ec46-107">En este tema se describe cómo realizar la autenticación mutua con un servicio RPC que se publica mediante las API del servicio de nombres de RPC (RpcNs).</span><span class="sxs-lookup"><span data-stu-id="1ec46-107">This topic discusses how to perform mutual authentication with an RPC service that publishes itself using the RPC name service (RpcNs) APIs.</span></span>

<span data-ttu-id="1ec46-108">**Para registrar un SPN en el directorio**</span><span class="sxs-lookup"><span data-stu-id="1ec46-108">**To register an SPN in the directory**</span></span>

1.  <span data-ttu-id="1ec46-109">Llame a la función [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para crear un nombre de entidad de seguridad de servicio (SPN) para el servicio.</span><span class="sxs-lookup"><span data-stu-id="1ec46-109">Call the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose a service principal name (SPN) for the service.</span></span>
2.  <span data-ttu-id="1ec46-110">Llame a la función [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) para registrar el SPN en la cuenta de servicio o en la cuenta de equipo en cuyo contexto se ejecutará el servicio.</span><span class="sxs-lookup"><span data-stu-id="1ec46-110">Call the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function to register the SPN on the service account or computer account in whose context the service will run.</span></span>

<span data-ttu-id="1ec46-111">**Para registrar un servicio con el servicio de nombres de RPC**</span><span class="sxs-lookup"><span data-stu-id="1ec46-111">**To register a service with the RPC naming service**</span></span>

1.  <span data-ttu-id="1ec46-112">Compruebe que los SPN adecuados están registrados en la cuenta en la que se está ejecutando el servicio.</span><span class="sxs-lookup"><span data-stu-id="1ec46-112">Verify that the appropriate SPNs are registered on the account under which the service is running.</span></span> <span data-ttu-id="1ec46-113">Para obtener más información, consulte tareas de mantenimiento de la [cuenta de inicio de sesión](logon-account-maintenance-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="1ec46-113">For more information, see [Logon Account Maintenance Tasks](logon-account-maintenance-tasks.md).</span></span>
2.  <span data-ttu-id="1ec46-114">Llame a la función [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) para registrar el SPN del servicio con el servicio de autenticación RPC y especifique el **RPC \_ C \_ authn \_ GSS \_ Negotiate** como el servicio de autenticación que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="1ec46-114">Call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function to register the service SPN with the RPC authentication service, and specify **RPC\_C\_AUTHN\_GSS\_NEGOTIATE** as the authentication service to use.</span></span>

<span data-ttu-id="1ec46-115">Para obtener más información acerca de cómo realizar la autenticación mutua en un servicio RPC, consulte [escribir un servidor SSPI autenticado](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span><span class="sxs-lookup"><span data-stu-id="1ec46-115">For more information about performing mutual authentication in an RPC service, see [Writing an Authenticated SSPI Server](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span></span>

<span data-ttu-id="1ec46-116">**Para autenticar el servicio desde el cliente**</span><span class="sxs-lookup"><span data-stu-id="1ec46-116">**To authenticate the service from the client**</span></span>

1.  <span data-ttu-id="1ec46-117">Extraiga el nombre de host del enlace RPC.</span><span class="sxs-lookup"><span data-stu-id="1ec46-117">Extract the host name from the RPC Binding.</span></span>
2.  <span data-ttu-id="1ec46-118">Cree el SPN para el servicio mediante una llamada a la función [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) con la clase de servicio, el nombre de host DNS y el nombre del servicio. es el nombre distintivo del punto de conexión en el caso de RpcNs.</span><span class="sxs-lookup"><span data-stu-id="1ec46-118">Compose the SPN for the service by calling the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function with the service class, the DNS host name, and the service name; that is the distinguished name of the connection point in the case of RpcNs.</span></span>

    <span data-ttu-id="1ec46-119">Para obtener más información acerca de la creación de un SPN para un servicio RpcNs, consulte [composición de SPN para un servicio RpcNs](composing-spns-for-an-rpcns-service.md).</span><span class="sxs-lookup"><span data-stu-id="1ec46-119">For more information about composing an SPN for an RpcNs service, see [Composing SPNs for an RpcNs Service](composing-spns-for-an-rpcns-service.md).</span></span>

3.  <span data-ttu-id="1ec46-120">Configure una [**estructura \_ \_ QoS de seguridad RPC**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) para solicitar la autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="1ec46-120">Set up an [**RPC\_SECURITY\_QOS**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) structure to request mutual authentication.</span></span>
4.  <span data-ttu-id="1ec46-121">Llame a la función [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para establecer los datos de autenticación para el enlace RPC.</span><span class="sxs-lookup"><span data-stu-id="1ec46-121">Call the [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function to set the authentication data for the RPC binding.</span></span> <span data-ttu-id="1ec46-122">El cliente debe solicitar al menos **\_ integridad de \_ nivel de \_ autenticación \_ \_ de RPC C** para asegurarse de que las comunicaciones no se han alterado.</span><span class="sxs-lookup"><span data-stu-id="1ec46-122">The client must request at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY** to ensure that communications have not been tampered.</span></span> <span data-ttu-id="1ec46-123">Para mayor seguridad, el cliente debe especificar **la \_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C** para solicitar el cifrado.</span><span class="sxs-lookup"><span data-stu-id="1ec46-123">For increased security, the client should specify **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** to request encryption.</span></span>
5.  <span data-ttu-id="1ec46-124">Realizar la llamada RPC.</span><span class="sxs-lookup"><span data-stu-id="1ec46-124">Perform the RPC call.</span></span>

<span data-ttu-id="1ec46-125">Para obtener más información sobre cómo realizar la autenticación mutua en un cliente RPC, consulte [escribir un cliente SSPI autenticado](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span><span class="sxs-lookup"><span data-stu-id="1ec46-125">For more information about performing mutual authentication in an RPC client, see [Writing an Authenticated SSPI Client](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span></span>

<span data-ttu-id="1ec46-126">**Para autenticar el cliente desde el servicio**</span><span class="sxs-lookup"><span data-stu-id="1ec46-126">**To authenticate the client from the service**</span></span>

1.  <span data-ttu-id="1ec46-127">Llame a la función [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) para comprobar los parámetros de autenticación especificados por el cliente.</span><span class="sxs-lookup"><span data-stu-id="1ec46-127">Call the [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) function to verify the authentication parameters specified by the client.</span></span> <span data-ttu-id="1ec46-128">Si el cliente no ha solicitado el nivel deseado de autenticación, rechace la llamada.</span><span class="sxs-lookup"><span data-stu-id="1ec46-128">If the client has not requested the desired level of authentication, reject the call.</span></span> <span data-ttu-id="1ec46-129">Tenga en cuenta que un servicio RPC debe comprobar el nivel de autenticación, el servicio de autenticación y la identidad del cliente en cada llamada para asegurarse de que el cliente se ha autenticado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1ec46-129">Be aware that an RPC service must verify the authentication level, authentication service, and client identity on every call to ensure that the client has been properly authenticated.</span></span>
2.  <span data-ttu-id="1ec46-130">Llame a la función [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) para suplantar al cliente.</span><span class="sxs-lookup"><span data-stu-id="1ec46-130">Call the [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) function to impersonate the client.</span></span>
3.  <span data-ttu-id="1ec46-131">Realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="1ec46-131">Perform the requested operation.</span></span>
4.  <span data-ttu-id="1ec46-132">Llame a la función [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) para revertir al contexto de seguridad del servicio.</span><span class="sxs-lookup"><span data-stu-id="1ec46-132">Call the [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) function to revert to the service security context.</span></span>

<span data-ttu-id="1ec46-133">Para obtener más información acerca de la suplantación de cliente RPC, consulte [suplantación de cliente](/windows/desktop/Rpc/client-impersonation).</span><span class="sxs-lookup"><span data-stu-id="1ec46-133">For more information about RPC client impersonation, see [Client Impersonation](/windows/desktop/Rpc/client-impersonation).</span></span>

<span data-ttu-id="1ec46-134">Para más información, consulte:</span><span class="sxs-lookup"><span data-stu-id="1ec46-134">For more information, see:</span></span>

-   [<span data-ttu-id="1ec46-135">Publicación con el servicio de nombres RPC (RpcNs)</span><span class="sxs-lookup"><span data-stu-id="1ec46-135">Publishing with the RPC Name Service (RpcNs)</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="1ec46-136">Aspectos básicos de seguridad de RPC</span><span class="sxs-lookup"><span data-stu-id="1ec46-136">RPC Security Essentials</span></span>](/windows/desktop/Rpc/rpc-security-essentials)

 

 