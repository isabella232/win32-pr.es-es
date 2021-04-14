---
description: Cuando una aplicación realiza una comprobación de acceso mediante una llamada a la función AuthzAccessCheck, los resultados de esa comprobación de acceso se pueden almacenar en caché.
ms.assetid: d79a5683-6c67-487f-b9a6-4e80da38b827
title: Almacenar en caché comprobaciones de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967e0a5398d93c1715d7d08e5c7c75695e4120ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361716"
---
# <a name="caching-access-checks"></a><span data-ttu-id="97ac9-103">Almacenar en caché comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="97ac9-103">Caching Access Checks</span></span>

<span data-ttu-id="97ac9-104">Cuando una aplicación realiza una comprobación de acceso mediante una llamada a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , los resultados de esa comprobación de acceso se pueden almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="97ac9-104">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span> <span data-ttu-id="97ac9-105">Cuando el parámetro *pAuthzHandle* de la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) no es **null**, la función realiza una comprobación de acceso independiente, con una [**\_ máscara de acceso**](access-mask.md) solicitada de **máximo \_ permitido** y almacena en caché los resultados de esa comprobación.</span><span class="sxs-lookup"><span data-stu-id="97ac9-105">When the *pAuthzHandle* parameter of the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function is not **NULL**, the function performs a separate access check, with a requested [**ACCESS\_MASK**](access-mask.md) of **MAXIMUM\_ALLOWED**, and caches the results of that check.</span></span> <span data-ttu-id="97ac9-106">A continuación, se puede pasar un identificador a los resultados de esa comprobación como el parámetro *AuthzHandle* a la función [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="97ac9-106">A handle to the results of that check can then be passed as the *AuthzHandle* parameter to the [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck) function.</span></span> <span data-ttu-id="97ac9-107">Esto permite una comprobación de acceso más rápida para un cliente determinado y [*descriptores de seguridad*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="97ac9-107">This allows faster access checking for a given client and [*security descriptors*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="97ac9-108">Solo se puede almacenar en caché la parte estática de una comprobación de acceso.</span><span class="sxs-lookup"><span data-stu-id="97ac9-108">Only the static portion of an access check can be cached.</span></span> <span data-ttu-id="97ac9-109">Todas las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) de devolución de llamada o las ACE que contienen el SID **\_ propio** de la entidad de seguridad deben evaluarse para cada comprobación de acceso.</span><span class="sxs-lookup"><span data-stu-id="97ac9-109">Any callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) or ACEs that contain the **PRINCIPAL\_SELF** SID must be evaluated for each access check.</span></span>

<span data-ttu-id="97ac9-110">Las variables de atributo deben tener el formato de una expresión cuando se utilizan con operadores lógicos; de lo contrario, se evalúan como Unknown.</span><span class="sxs-lookup"><span data-stu-id="97ac9-110">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="97ac9-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="97ac9-111">Example</span></span>

<span data-ttu-id="97ac9-112">En el siguiente ejemplo se comprueba el acceso a un resultado almacenado en caché de una comprobación de acceso anterior.</span><span class="sxs-lookup"><span data-stu-id="97ac9-112">The following example checks access against a cached result from a previous access check.</span></span> <span data-ttu-id="97ac9-113">La comprobación de acceso anterior se realizó en el ejemplo de [comprobación del acceso con la API de authz](checking-access-with-authz-api.md).</span><span class="sxs-lookup"><span data-stu-id="97ac9-113">The previous access check was performed in the example in [Checking Access with Authz API](checking-access-with-authz-api.md).</span></span>


```C++
BOOL CheckCachedAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{
    #define MY_MAX 4096


    PSECURITY_DESCRIPTOR                pSecurityDescriptor = NULL;
    ULONG                                cbSecurityDescriptorSize = 0;
    AUTHZ_ACCESS_REQUEST                Request;
    CHAR                                ReplyBuffer[MY_MAX];
    CHAR                                CachedReplyBuffer[MY_MAX];
    PAUTHZ_ACCESS_REPLY                    pReply = (PAUTHZ_ACCESS_REPLY)ReplyBuffer;
    PAUTHZ_ACCESS_REPLY                    pCachedReply = (PAUTHZ_ACCESS_REPLY)CachedReplyBuffer;
    DWORD                                AuthzError =0;
    AUTHZ_ACCESS_CHECK_RESULTS_HANDLE    hCached;

    //Allocate memory for the access request structure.
    RtlZeroMemory(&Request, sizeof(AUTHZ_ACCESS_REQUEST));

    //Set up the access request structure.
    Request.DesiredAccess = READ_CONTROL;
    
    //Allocate memory for the initial access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the access reply structure.
    pReply->ResultListLength = 1;
    pReply->Error = (PDWORD) ((PCHAR) pReply + sizeof(AUTHZ_ACCESS_REPLY));
    pReply->GrantedAccessMask = (PACCESS_MASK) (pReply->Error + pReply->ResultListLength);
    pReply->SaclEvaluationResults = NULL;

    //Allocate memory for the cached access reply structure.
    RtlZeroMemory(ReplyBuffer, MY_MAX);

    //Set up the cached access reply structure.
    pCachedReply->ResultListLength = 1;
    pCachedReply->Error = (PDWORD) ((PCHAR) pCachedReply + sizeof(AUTHZ_ACCESS_REPLY));
    pCachedReply->GrantedAccessMask = (PACCESS_MASK) (pCachedReply->Error + pCachedReply->ResultListLength);
    pCachedReply->SaclEvaluationResults = NULL;

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

    //Call AuthzAccessCheck and cache results.
    if(!AuthzAccessCheck(
        0,
        hClientContext,
        &Request,
        NULL,
        pSecurityDescriptor,
        NULL,
        0,
        pReply,
        &hCached))
    {
        printf_s("AuthzAccessCheck failed with %d\n", GetLastError());
        
    LocalFree(pSecurityDescriptor);
        
        return FALSE;
    }

    //Call AuthzCachedAccessCheck with the cached result from the previous call.
    if(!AuthzCachedAccessCheck(
        0,
        hCached,
        &Request,
        NULL,
        pCachedReply))
    {
        printf_s("AuthzCachedAccessCheck failed with %d\n", GetLastError());
        
        LocalFree(pSecurityDescriptor);
    AuthzFreeHandle(hCached);
    
        return FALSE;
    }

    //Print results.
    if(*pCachedReply->GrantedAccessMask & READ_CONTROL)
    {
        printf_s("Access granted.\n");
    }
    else
    {
        printf_s("Access denied.\n");
    }


  LocalFree(pSecurityDescriptor);
  AuthzFreeHandle(hCached);
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="97ac9-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97ac9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97ac9-115">Agregar SID a un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="97ac9-115">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="97ac9-116">Comprobación del acceso con la API de authz</span><span class="sxs-lookup"><span data-stu-id="97ac9-116">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="97ac9-117">Inicializar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="97ac9-117">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="97ac9-118">Consultar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="97ac9-118">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
