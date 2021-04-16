---
description: Una aplicación puede agregar identificadores de seguridad (SID) a un contexto de cliente existente llamando a la función AuthzAddSidsToContext.
ms.assetid: d49ce47b-e91a-452b-b423-07e8d282d28a
title: Agregar SID a un contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a601f485110ddacea0fdb54cb7dcef587a25cb9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546331"
---
# <a name="adding-sids-to-a-client-context"></a><span data-ttu-id="7341a-103">Agregar SID a un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="7341a-103">Adding SIDs to a Client Context</span></span>

<span data-ttu-id="7341a-104">Una aplicación puede agregar [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) a un contexto de cliente existente llamando a la función [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .</span><span class="sxs-lookup"><span data-stu-id="7341a-104">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span> <span data-ttu-id="7341a-105">La función [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) permite a una aplicación especificar una lista de SID y una lista de restricciones de SID para el contexto de cliente especificado.</span><span class="sxs-lookup"><span data-stu-id="7341a-105">The [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function allows an application to specify both a list of SIDs and a list of restricting SIDs to the specified client context.</span></span>

<span data-ttu-id="7341a-106">El sistema utiliza la lista de restricciones de SID cuando comprueba el acceso del token a un objeto protegible.</span><span class="sxs-lookup"><span data-stu-id="7341a-106">The system uses the list of restricting SIDs when it checks the token's access to a securable object.</span></span> <span data-ttu-id="7341a-107">Cuando un proceso o subproceso restringido intenta tener acceso a un objeto protegible, el sistema realiza dos comprobaciones de acceso: una con los SID habilitados del token y otra mediante la lista de SID restrictivos.</span><span class="sxs-lookup"><span data-stu-id="7341a-107">When a restricted process or thread tries to access a securable object, the system performs two access checks: one using the token's enabled SIDs, and another using the list of restricting SIDs.</span></span> <span data-ttu-id="7341a-108">El acceso se concede solo si ambas comprobaciones de acceso permiten los derechos de acceso solicitados.</span><span class="sxs-lookup"><span data-stu-id="7341a-108">Access is granted only if both access checks allow the requested access rights.</span></span>

<span data-ttu-id="7341a-109">Las variables de atributo deben tener el formato de una expresión cuando se utilizan con operadores lógicos; de lo contrario, se evalúan como Unknown.</span><span class="sxs-lookup"><span data-stu-id="7341a-109">Attribute variables must be in the form of an expression when used with logical operators; otherwise, they are evaluated as unknown.</span></span>

## <a name="example"></a><span data-ttu-id="7341a-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7341a-110">Example</span></span>

<span data-ttu-id="7341a-111">En el ejemplo siguiente se agrega un SID y un SID restrictivo al contexto del cliente creado por el ejemplo en la [inicialización de un contexto de cliente](initializing-a-client-context.md).</span><span class="sxs-lookup"><span data-stu-id="7341a-111">The following example adds a SID and a restricting SID to the client context created by the example in [Initializing a Client Context](initializing-a-client-context.md).</span></span>


```C++
BOOL AddSidsToContext(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{
    AUTHZ_CLIENT_CONTEXT_HANDLE        NewContext = NULL;
    PSID                            pEveryoneSid = NULL;
    PSID                            pLocalSid = NULL;
    SID_AND_ATTRIBUTES                Sids;
    SID_AND_ATTRIBUTES                RestrictedSids;
    DWORD                            SidCount = 0;
    DWORD                            RestrictedSidCount = 0;

    //Create a PSID from the "Everyone" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-1-0", &pEveryoneSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError());
        return FALSE;
    }

    //Create a PSID from the "Local" well-known SID.
    if(!ConvertStringSidToSid(L"S-1-2-0", &pLocalSid))
    {
        printf_s("ConvertStringSidToSid failed with %d\n", GetLastError);
        return FALSE;
    }

    //Set the members of the SID_AND_ATTRIBUTES structure to be added.
    Sids.Sid = pEveryoneSid;
    Sids.Attributes = SE_GROUP_ENABLED;

    //Set the members of the SID_AND_ATTRIBUTES structure for the restricting SID.
    RestrictedSids.Sid = pLocalSid;
    RestrictedSids.Attributes = SE_GROUP_ENABLED;

    

    //Create a new context with the new "Everyone" SID and "Local" restricting SID.
    if(!AuthzAddSidsToContext(
        *phClientContext,
        &Sids,
        1,
        &RestrictedSids,
        1,
        &NewContext))
    {
        printf_s("AuthzAddSidsToContext failed with %d\n", GetLastError());
        if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        return FALSE;
    }

    if(pEveryoneSid)
        {
            FreeSid(pEveryoneSid);
        }
        if(pLocalSid)
        {
            FreeSid(pLocalSid);
        }
        
        AuthzFreeContext(*phClientContext);
        *phClientContext = NewContext;

    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="7341a-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7341a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7341a-113">Almacenar en caché comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="7341a-113">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="7341a-114">Comprobación del acceso con la API de authz</span><span class="sxs-lookup"><span data-stu-id="7341a-114">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="7341a-115">Inicializar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="7341a-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="7341a-116">Consultar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="7341a-116">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> </dl>

 

 
