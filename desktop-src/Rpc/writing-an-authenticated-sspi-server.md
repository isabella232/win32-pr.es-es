---
title: Escribir un servidor SSPI autenticado
description: Antes de que la comunicación autenticada pueda tener lugar entre los programas de cliente y servidor, el servidor debe registrar su información de autenticación.
ms.assetid: 723ae1ee-d729-4748-9ef1-062a0c6f60d0
keywords:
- RPC llamada a procedimiento remoto, tareas, escribir un servidor SSPI autenticado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b1cb06cfc626bc8130f3c4b0cee0a7b6d7893e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075673"
---
# <a name="writing-an-authenticated-sspi-server"></a><span data-ttu-id="3b861-104">Escribir un servidor SSPI autenticado</span><span class="sxs-lookup"><span data-stu-id="3b861-104">Writing an Authenticated SSPI Server</span></span>

<span data-ttu-id="3b861-105">Antes de que la comunicación autenticada pueda tener lugar entre los programas de cliente y servidor, el servidor debe registrar su información de autenticación.</span><span class="sxs-lookup"><span data-stu-id="3b861-105">Before authenticated communication can take place between the client and server programs, the server must register its authentication information.</span></span> <span data-ttu-id="3b861-106">En concreto, el servidor debe registrar su nombre principal y especificar el servicio de autenticación que usa.</span><span class="sxs-lookup"><span data-stu-id="3b861-106">In particular, the server must register its principal name and specify the authentication service it uses.</span></span> <span data-ttu-id="3b861-107">Para obtener más información sobre los nombres de entidad de seguridad, consulte [nombres principales](principal-names.md).</span><span class="sxs-lookup"><span data-stu-id="3b861-107">For more information on principal names, see [Principal Names](principal-names.md).</span></span> <span data-ttu-id="3b861-108">Para obtener más información acerca de los servicios de autenticación, vea [servicios de autenticación](authentication-services.md).</span><span class="sxs-lookup"><span data-stu-id="3b861-108">For details about authentication services, see [Authentication Services](authentication-services.md).</span></span>

<span data-ttu-id="3b861-109">Para registrar la información de autenticación, los servidores llaman a la función [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) .</span><span class="sxs-lookup"><span data-stu-id="3b861-109">To register its authentication information, servers call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function.</span></span> <span data-ttu-id="3b861-110">Pase un puntero al nombre de la entidad de seguridad como el valor del primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="3b861-110">Pass a pointer to the principal name as the value of the first parameter.</span></span> <span data-ttu-id="3b861-111">Establezca el segundo parámetro en una constante que indique el servicio de autenticación que usará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b861-111">Set the second parameter to a constant indicating the authentication service that the application will use.</span></span> <span data-ttu-id="3b861-112">Para obtener una descripción de los servicios de autenticación, vea [Authentication-Service constantes](authentication-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3b861-112">For a description of authentication services, see [Authentication-Service Constants](authentication-service-constants.md).</span></span>

<span data-ttu-id="3b861-113">El servidor también puede pasar la dirección de una función de adquisición de claves como el valor del tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="3b861-113">The server may also pass the address of a key acquisition function as the value of the third parameter.</span></span> <span data-ttu-id="3b861-114">Consulte [funciones de adquisición de claves](key-acquisition-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3b861-114">See [Key Acquisition Functions](key-acquisition-functions.md).</span></span> <span data-ttu-id="3b861-115">Para usar la función de adquisición de clave predeterminada para el servicio de autenticación seleccionado, establezca el tercer parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="3b861-115">To use the default key acquisition function for the selected authentication service, set the third parameter to **NULL**.</span></span> <span data-ttu-id="3b861-116">El último parámetro de la función [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) es un puntero que se pasa a la función de adquisición de clave, si se proporciona una función de adquisición de claves.</span><span class="sxs-lookup"><span data-stu-id="3b861-116">The last parameter to the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function is a pointer data to pass to the key acquisition function, if you provide a key acquisition function.</span></span> <span data-ttu-id="3b861-117">En el fragmento de código siguiente se muestra una llamada a **RpcServerRegisterAuthInfo** .</span><span class="sxs-lookup"><span data-stu-id="3b861-117">A call to **RpcServerRegisterAuthInfo** is shown in the following code fragment.</span></span>


```C++
dwStatus = DsMakeSpn(
    "ldap",
    "ServerName.domain.com",
    NULL,
    0,
    NULL,
    &pcSpnLength,
    pszSpn);

rpcStatus = RpcServerRegisterAuthInfo (
    psz,                                   // Server principal name
    RPC_C_AUTHN_GSS_NEGOTIATE,             // Authentication service
    NULL,                                  // Use default key function
    NULL);                                 // No arg for key function
```



<span data-ttu-id="3b861-118">Además, el servidor puede proporcionar la biblioteca en tiempo de ejecución de RPC con una función de autorización.</span><span class="sxs-lookup"><span data-stu-id="3b861-118">In addition, the server may provide the RPC run-time library with an authorization function.</span></span> <span data-ttu-id="3b861-119">Para establecer una función de autorización, llame a la función [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) .</span><span class="sxs-lookup"><span data-stu-id="3b861-119">To set an authorization function, call the [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) function.</span></span>

<span data-ttu-id="3b861-120">La parte del servidor de una aplicación distribuida puede llamar a la función [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) o [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) para consultar un identificador de enlace para obtener información de autenticación.</span><span class="sxs-lookup"><span data-stu-id="3b861-120">The server portion of a distributed application can call the function [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex) to query a binding handle for authentication information.</span></span>

<span data-ttu-id="3b861-121">Si el servidor se registra con un proveedor de soporte técnico de seguridad, no se enviarán llamadas de cliente con credenciales no válidas.</span><span class="sxs-lookup"><span data-stu-id="3b861-121">If your server registers with a security support provider, client calls with invalid credentials will not be dispatched.</span></span> <span data-ttu-id="3b861-122">Sin embargo, se enviarán llamadas sin credenciales.</span><span class="sxs-lookup"><span data-stu-id="3b861-122">However, calls with no credentials will be dispatched.</span></span> <span data-ttu-id="3b861-123">Hay tres formas de evitar que esto suceda:</span><span class="sxs-lookup"><span data-stu-id="3b861-123">There are three ways to prevent this from happening:</span></span>

-   <span data-ttu-id="3b861-124">Registre la interfaz con [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), con una función de devolución de llamada de seguridad. Esto hará que la biblioteca en tiempo de ejecución de RPC rechace automáticamente las llamadas no autenticadas a esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="3b861-124">Register the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex), with a security callback function; this will cause the RPC run-time library to automatically reject unauthenticated calls to that interface.</span></span> <span data-ttu-id="3b861-125">El registro de una función de devolución de llamada es compatible con otros métodos para comprobar las credenciales de acceso; la función de devolución de llamada puede llamar a las funciones [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient)o [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) , u otras.</span><span class="sxs-lookup"><span data-stu-id="3b861-125">Registering a callback function is compatible with other methods of checking access credentials; the callback function can itself call the [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient), [**RpcGetAuthorizationContextForClient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient), or [**RpcBindingInqAuthClientEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) functions, or others.</span></span> <span data-ttu-id="3b861-126">Sin embargo, estas funciones no pueden utilizar los argumentos pasados a la función, ya que no se han desordenado en ese momento.</span><span class="sxs-lookup"><span data-stu-id="3b861-126">However, these functions cannot use the arguments passed to the function, as they are not unmarshalled at that point.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b861-127">Registrar la interfaz mediante [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) con una función de devolución de llamada de seguridad es el método más recomendado para comprobar las credenciales del cliente.</span><span class="sxs-lookup"><span data-stu-id="3b861-127">Registering the interface using [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) with a security callback function is the most heavily recommended method of checking client credentials.</span></span>

 

-   <span data-ttu-id="3b861-128">Llame a [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) para determinar el nivel de seguridad que usa el cliente.</span><span class="sxs-lookup"><span data-stu-id="3b861-128">Call [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) to determine the security level that the client is using.</span></span> <span data-ttu-id="3b861-129">El código auxiliar puede devolver un error si el cliente no está autenticado.</span><span class="sxs-lookup"><span data-stu-id="3b861-129">Your stub can then return an error if the client is unauthenticated.</span></span>

 

 




