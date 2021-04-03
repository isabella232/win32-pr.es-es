---
description: Las aplicaciones determinan si se debe conceder acceso a los objetos protegibles mediante una llamada a la función AuthzAccessCheck.
ms.assetid: dad0a102-08ed-4cd2-bef5-87bc48fc7fc2
title: Comprobación del acceso con la API de authz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e129b690a7c1f701b5f669a8f0705c5a5e9a2eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908091"
---
# <a name="checking-access-with-authz-api"></a><span data-ttu-id="d3a58-103">Comprobación del acceso con la API de authz</span><span class="sxs-lookup"><span data-stu-id="d3a58-103">Checking Access with Authz API</span></span>

<span data-ttu-id="d3a58-104">Las aplicaciones determinan si se debe conceder acceso a los objetos protegibles mediante una llamada a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="d3a58-104">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

<span data-ttu-id="d3a58-105">La función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) toma las estructuras de [**\_ \_ solicitud de acceso**](/windows/desktop/api/Authz/ns-authz-authz_access_request) y [**\_ descriptor de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) de AUTHZ como parámetros.</span><span class="sxs-lookup"><span data-stu-id="d3a58-105">The [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function takes both [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) and [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) structures as parameters.</span></span> <span data-ttu-id="d3a58-106">La estructura de **\_ \_ solicitud de acceso de AUTHZ** especifica un nivel de acceso solicitado.</span><span class="sxs-lookup"><span data-stu-id="d3a58-106">The **AUTHZ\_ACCESS\_REQUEST** structure specifies a level of access requested.</span></span> <span data-ttu-id="d3a58-107">La función **AuthzAccessCheck** evalúa el acceso solicitado con el **\_ descriptor de seguridad** especificado para un contexto de cliente especificado.</span><span class="sxs-lookup"><span data-stu-id="d3a58-107">The **AuthzAccessCheck** function evaluates the requested access against the specified **SECURITY\_DESCRIPTOR** for a specified client context.</span></span> <span data-ttu-id="d3a58-108">Para obtener información sobre cómo un descriptor de seguridad controla el acceso a un objeto, vea [Cómo controlan el acceso a un objeto las DACL](how-dacls-control-access-to-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="d3a58-108">For information about how a security descriptor controls access to an object, see [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).</span></span>

<span data-ttu-id="d3a58-109">Las variables de atributo deben tener el formato de una expresión cuando se utilizan con operadores lógicos; de lo contrario, se evalúan como Unknown.</span><span class="sxs-lookup"><span data-stu-id="d3a58-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="callback-function"></a><span data-ttu-id="d3a58-110">Función de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="d3a58-110">Callback Function</span></span>

<span data-ttu-id="d3a58-111">Si la [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del [**\_ descriptor de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) del objeto que se va a comprobar contiene las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) de devolución de llamada, [**AUTHZACCESSCHECK**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) llama a la función [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) para cada ACE de devolución de llamada contenida en la DACL.</span><span class="sxs-lookup"><span data-stu-id="d3a58-111">If the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) of the object to be checked contains any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) calls the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function for each callback ACE contained in the DACL.</span></span> <span data-ttu-id="d3a58-112">Una ACE de devolución de llamada es cualquier estructura ACE cuyo tipo ACE contenga la palabra "callback".</span><span class="sxs-lookup"><span data-stu-id="d3a58-112">A callback ACE is any ACE structure whose ACE type contains the word "callback."</span></span> <span data-ttu-id="d3a58-113">La función **AuthzAccessCheckCallback** es una función definida por la aplicación que se debe registrar cuando se inicializa el administrador de recursos mediante una llamada a la función [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="d3a58-113">The **AuthzAccessCheckCallback** function is an application-defined function that must be registered when the resource manager is initialized by calling the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function.</span></span>

<span data-ttu-id="d3a58-114">Una función de devolución de llamada permite a una aplicación definir la lógica de negocios que se va a evaluar en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d3a58-114">A callback function allows an application to define business logic to be evaluated at runtime.</span></span> <span data-ttu-id="d3a58-115">Cuando se llama a la función [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) , se pasa la ACE de devolución de llamada que causó la llamada a la función de devolución de llamada para su evaluación.</span><span class="sxs-lookup"><span data-stu-id="d3a58-115">When the [**AuthzAccessCheckCallback**](authzaccesscheckcallback.md) function is called, the callback ACE that caused the call is passed to the callback function for evaluation.</span></span> <span data-ttu-id="d3a58-116">Si la lógica definida por la aplicación se evalúa como **true**, la ACE de devolución de llamada se incluye en la comprobación de acceso.</span><span class="sxs-lookup"><span data-stu-id="d3a58-116">If the application-defined logic evaluates as **TRUE**, then the callback ACE is included in the access check.</span></span> <span data-ttu-id="d3a58-117">De lo contrario, se omite.</span><span class="sxs-lookup"><span data-stu-id="d3a58-117">Otherwise, it is ignored.</span></span>

## <a name="caching-access-results"></a><span data-ttu-id="d3a58-118">Almacenar en caché los resultados de acceso</span><span class="sxs-lookup"><span data-stu-id="d3a58-118">Caching Access Results</span></span>

<span data-ttu-id="d3a58-119">Los resultados de una comprobación de acceso se pueden almacenar en caché y usar en futuras llamadas a la función [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="d3a58-119">The results of an access check can be cached and used in future calls to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="d3a58-120">Para obtener más información sobre las comprobaciones de acceso de almacenamiento en caché, incluido un ejemplo, vea [caching Access Checks](caching-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="d3a58-120">For more information about caching access checks, including an example, see [Caching Access Checks](caching-access-checks.md).</span></span>

## <a name="example"></a><span data-ttu-id="d3a58-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d3a58-121">Example</span></span>

<span data-ttu-id="d3a58-122">En el ejemplo siguiente se crea un [**\_ descriptor de seguridad**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) que permite el acceso de **\_ control de lectura** a los administradores integrados.</span><span class="sxs-lookup"><span data-stu-id="d3a58-122">The following example creates a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/Winnt/ns-winnt-security_descriptor) that allows **READ\_CONTROL** access to built-in administrators.</span></span> <span data-ttu-id="d3a58-123">Usa ese descriptor de seguridad para comprobar el acceso del cliente especificado por el contexto de cliente creado en el ejemplo de [inicializar un contexto de cliente](initializing-a-client-context.md).</span><span class="sxs-lookup"><span data-stu-id="d3a58-123">It uses that security descriptor to check access for the client specified by the client context created in the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


```C++
BOOL CheckAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR    pSecurityDescriptor = NULL;
    ULONG                    cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST    Request;
    CHAR                    ReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY        pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    DWORD                    AuthzError =0;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

    //Create security descriptor.
    if(!ConvertStringSecurityDescriptorToSecurityDescriptor(
        L"O:LAG:BAD:(A;;RC;;;BA)",
        SDDL_REVISION_1,
        &pSecurityDescriptor,
        NULL))
    {
        printf_s("ConvertStringSecurityDescriptorToSecurityDescriptor failed with %d\n", GetLastError()); 
        return FALSE;
    }

    //Call AuthzAccessCheck.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        NULL))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
    
        return FALSE;
    }


    //Print results.
    if(*pReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }

  LocalFree(pSecurityDescriptor);
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="d3a58-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d3a58-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3a58-125">Agregar SID a un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="d3a58-125">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="d3a58-126">Almacenar en caché comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="d3a58-126">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="d3a58-127">Inicializar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="d3a58-127">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="d3a58-128">Consultar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="d3a58-128">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
