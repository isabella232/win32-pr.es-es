---
title: Escribir un cliente SSPI autenticado
description: Escribir un cliente SSPI autenticado y una llamada a procedimiento remoto (RPC).
ms.assetid: db39d3bf-84fa-466e-9ba1-ba17f64c8f8d
keywords:
- RPC llamada a procedimiento remoto, tareas, escribir un cliente SSPI autenticado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8476772a2ed652f6646b078c2876234cbcc0d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149467"
---
# <a name="writing-an-authenticated-sspi-client"></a><span data-ttu-id="0ffac-104">Escribir un cliente SSPI autenticado</span><span class="sxs-lookup"><span data-stu-id="0ffac-104">Writing an Authenticated SSPI Client</span></span>

<span data-ttu-id="0ffac-105">Todas las sesiones de cliente/servidor RPC requieren un enlace entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="0ffac-105">All RPC client/server sessions require a binding between the client and the server.</span></span> <span data-ttu-id="0ffac-106">Para agregar seguridad a las aplicaciones cliente/servidor, los programas deben usar un enlace autenticado.</span><span class="sxs-lookup"><span data-stu-id="0ffac-106">To add security to client/server applications, the programs must use an authenticated binding.</span></span> <span data-ttu-id="0ffac-107">En esta sección se describe el proceso de creación de un enlace autenticado entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="0ffac-107">This section describes the process of creating an authenticated binding between the client and the server.</span></span>

-   [<span data-ttu-id="0ffac-108">Crear identificadores de enlace del lado cliente</span><span class="sxs-lookup"><span data-stu-id="0ffac-108">Creating Client-side Binding Handles</span></span>](#creating-client-side-binding-handles)
-   [<span data-ttu-id="0ffac-109">Proporcionar credenciales de cliente al servidor</span><span class="sxs-lookup"><span data-stu-id="0ffac-109">Providing Client Credentials to the Server</span></span>](#providing-client-credentials-to-the-server)

<span data-ttu-id="0ffac-110">Para obtener información relacionada, vea [procedimientos usados con la mayoría de los paquetes de seguridad y protocolos](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="0ffac-110">For related information, see [Procedures Used with Most Security Packages and Protocols](/windows/desktop/SecAuthN/procedures-used-with-most-security-packages-and-protocols) in the Platform Software Development Kit (SDK).</span></span>

## <a name="creating-client-side-binding-handles"></a><span data-ttu-id="0ffac-111">Crear identificadores de enlace del lado cliente</span><span class="sxs-lookup"><span data-stu-id="0ffac-111">Creating Client-side Binding Handles</span></span>

<span data-ttu-id="0ffac-112">Para crear una sesión autenticada con un programa de servidor, las aplicaciones cliente deben proporcionar información de autenticación con su identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="0ffac-112">To create an authenticated session with a server program, client applications must provide authentication information with their binding handle.</span></span> <span data-ttu-id="0ffac-113">Para configurar un identificador de enlace autenticado, los clientes invocan a la función [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) .</span><span class="sxs-lookup"><span data-stu-id="0ffac-113">To set up an authenticated binding handle, clients invoke the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function.</span></span> <span data-ttu-id="0ffac-114">Estas dos funciones son casi idénticas.</span><span class="sxs-lookup"><span data-stu-id="0ffac-114">These two functions are nearly identical.</span></span> <span data-ttu-id="0ffac-115">La única diferencia entre ellos es que el cliente puede especificar la calidad de servicio con la función **RpcBindingSetAuthInfoEx** .</span><span class="sxs-lookup"><span data-stu-id="0ffac-115">The only difference between them is that the client can specify the quality of service with the **RpcBindingSetAuthInfoEx** function.</span></span>

<span data-ttu-id="0ffac-116">En el fragmento de código siguiente se muestra cómo puede ser una llamada a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) .</span><span class="sxs-lookup"><span data-stu-id="0ffac-116">The following code fragment shows how a call to [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) might look.</span></span>


```C++
// This code fragment assumes that rpcBinding is a valid binding 
// handle between the client and the server. It also assumes that
// pAuthCredentials is a valid pointer to a data structure which
// contains the user's authentication credentials.

dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

//...

rpcStatus = RpcBindingSetAuthInfo(
    rpcBinding,                       // Valid binding handle
    pszSpn,                           // Principal name 
    RPC_C_AUTHN_LEVEL_PKT_INTEGRITY,  // Authentication level
    RPC_C_AUTHN_GSS_NEGOTIATE,        // Use Negotiate SSP
    NULL,                             // Authentication credentials <entity type="ndash"/> use current thread credentials
    RPC_C_AUTHZ_NAME);                // Authorization service
```



<span data-ttu-id="0ffac-117">Una vez que el cliente llama correctamente a las funciones [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) , la biblioteca en tiempo de ejecución de RPC autentica automáticamente todas las llamadas RPC en el enlace.</span><span class="sxs-lookup"><span data-stu-id="0ffac-117">After the client successfully calls the [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) or [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) functions, the RPC run-time library automatically authenticates all RPC calls on the binding.</span></span> <span data-ttu-id="0ffac-118">El nivel de seguridad y autenticación que selecciona el cliente solo se aplica a ese identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="0ffac-118">The level of security and authentication that the client selects applies only to that binding handle.</span></span> <span data-ttu-id="0ffac-119">Los identificadores de contexto derivados del identificador de enlace utilizarán la misma información de seguridad, pero las modificaciones posteriores en el identificador de enlace no se reflejarán en los identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="0ffac-119">Context handles derived from the binding handle will use the same security information, but subsequent modifications to the binding handle will not be reflected in the context handles.</span></span> <span data-ttu-id="0ffac-120">Para obtener más información, vea [identificadores de contexto](context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="0ffac-120">For more information, see [Context Handles](context-handles.md).</span></span>

<span data-ttu-id="0ffac-121">El nivel de autenticación permanece en vigor hasta que el cliente elige otro nivel o hasta que finaliza el proceso.</span><span class="sxs-lookup"><span data-stu-id="0ffac-121">The authentication level stays in effect until the client chooses another level, or until the process terminates.</span></span> <span data-ttu-id="0ffac-122">La mayoría de las aplicaciones no requerirán un cambio en el nivel de seguridad.</span><span class="sxs-lookup"><span data-stu-id="0ffac-122">Most applications will not require a change in the security level.</span></span> <span data-ttu-id="0ffac-123">El cliente puede consultar cualquier identificador de enlace para obtener su información de autorización mediante la invocación de [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) y pasándole el identificador de enlace.</span><span class="sxs-lookup"><span data-stu-id="0ffac-123">The client can query any binding handle to obtain its authorization information by invoking [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) and passing it the binding handle.</span></span>

## <a name="providing-client-credentials-to-the-server"></a><span data-ttu-id="0ffac-124">Proporcionar credenciales de cliente al servidor</span><span class="sxs-lookup"><span data-stu-id="0ffac-124">Providing Client Credentials to the Server</span></span>

<span data-ttu-id="0ffac-125">Los servidores usan la información de enlace del cliente para aplicar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="0ffac-125">Servers use the client's binding information to enforce security.</span></span> <span data-ttu-id="0ffac-126">Los clientes siempre pasan un identificador de enlace como primer parámetro de una llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="0ffac-126">Clients always pass a binding handle as the first parameter of a remote procedure call.</span></span> <span data-ttu-id="0ffac-127">Sin embargo, los servidores no pueden usar el identificador a menos que se declare como el primer parámetro para los procedimientos remotos en el archivo IDL o en el archivo de configuración de la aplicación (ACF) del servidor.</span><span class="sxs-lookup"><span data-stu-id="0ffac-127">However, servers cannot use the handle unless it is declared as the first parameter to remote procedures in either the IDL file or in the server's application configuration file (ACF).</span></span> <span data-ttu-id="0ffac-128">Puede optar por mostrar el identificador de enlace en el archivo IDL, pero esto obliga a todos los clientes a declarar y manipular el identificador de enlace en lugar de usar el enlace automático o implícito.</span><span class="sxs-lookup"><span data-stu-id="0ffac-128">You can choose to list the binding handle in the IDL file, but this forces all clients to declare and manipulate the binding handle rather than using automatic or implicit binding.</span></span> <span data-ttu-id="0ffac-129">Para obtener más información, vea [los archivos IDL y ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="0ffac-129">For further information, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="0ffac-130">Otro método consiste en dejar los controladores de enlace fuera del archivo IDL y colocar el atributo **de \_ identificador explícito** en el ACF del servidor.</span><span class="sxs-lookup"><span data-stu-id="0ffac-130">Another method is to leave the binding handles out of the IDL file and to place the **explicit\_handle** attribute into the server's ACF.</span></span> <span data-ttu-id="0ffac-131">De esta manera, el cliente puede utilizar el tipo de enlace que mejor se adapte a la aplicación, mientras que el servidor utiliza el controlador de enlace como si se hubiera declarado explícitamente.</span><span class="sxs-lookup"><span data-stu-id="0ffac-131">In this way, the client can use the type of binding best suited to the application, while the server uses the binding handle as though it were declared explicitly.</span></span>

<span data-ttu-id="0ffac-132">El proceso de extracción de las credenciales del cliente desde el identificador de enlace tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="0ffac-132">The process of extracting the client credentials from the binding handle occurs as follows:</span></span>

-   <span data-ttu-id="0ffac-133">Los clientes RPC llaman a [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) e incluyen su información de autenticación como parte de la información de enlace que se pasa al servidor.</span><span class="sxs-lookup"><span data-stu-id="0ffac-133">RPC clients call [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) and include their authentication information as part of the binding information passed to the server.</span></span>
-   <span data-ttu-id="0ffac-134">Normalmente, el servidor llama a [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) para comportarse como si fuera el cliente.</span><span class="sxs-lookup"><span data-stu-id="0ffac-134">Usually, the server calls [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) in order to behave as though it were the client.</span></span> <span data-ttu-id="0ffac-135">Si el identificador de enlace no está autenticado, se produce un error en la llamada con RPC \_ S \_ no hay ningún \_ contexto \_ disponible.</span><span class="sxs-lookup"><span data-stu-id="0ffac-135">If the binding handle is not authenticated, the call fails with RPC\_S\_NO\_CONTEXT\_AVAILABLE.</span></span> <span data-ttu-id="0ffac-136">Para obtener el nombre de usuario del cliente, llame a [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) durante la suplantación, o en Windows XP o versiones posteriores de Windows, llame a [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) para obtener el contexto de autorización y, a continuación, use las funciones de authz para recuperar el nombre.</span><span class="sxs-lookup"><span data-stu-id="0ffac-136">To obtain the client's user name, call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) while impersonating, or on Windows XP or later versions of Windows, call [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) to get the authorization context, then use Authz functions to retrieve the name.</span></span>
-   <span data-ttu-id="0ffac-137">Normalmente, el servidor llamará a [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) para crear objetos con ACL.</span><span class="sxs-lookup"><span data-stu-id="0ffac-137">The server will normally call [**CreatePrivateObjectSecurity**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) to create objects with ACLs.</span></span> <span data-ttu-id="0ffac-138">Una vez hecho esto, las comprobaciones de seguridad posteriores se vuelven automáticas.</span><span class="sxs-lookup"><span data-stu-id="0ffac-138">After this is accomplished, later security checks become automatic.</span></span>

 

 