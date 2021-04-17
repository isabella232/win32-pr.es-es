---
description: Las aplicaciones pueden llamar a la función AuthzGetInformationFromContext para consultar información sobre un contexto de cliente existente.
ms.assetid: 32655e54-499e-439e-8d4f-f2b4eaa0b184
title: Consultar un contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101c35466e675d9ecba942089bbe7b5e82cffd90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666666"
---
# <a name="querying-a-client-context"></a><span data-ttu-id="630c0-103">Consultar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="630c0-103">Querying a Client Context</span></span>

<span data-ttu-id="630c0-104">Las aplicaciones pueden llamar a la función [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) para consultar información sobre un contexto de cliente existente.</span><span class="sxs-lookup"><span data-stu-id="630c0-104">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span>

<span data-ttu-id="630c0-105">El parámetro *InfoClass* de la función [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) toma un valor de la enumeración de la [**\_ \_ \_ clase de información de contexto de AUTHZ**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) que especifica qué tipo de información consulta la función.</span><span class="sxs-lookup"><span data-stu-id="630c0-105">The *InfoClass* parameter of the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function takes a value from the [**AUTHZ\_CONTEXT\_INFORMATION\_CLASS**](/windows/desktop/api/Authz/ne-authz-authz_context_information_class) enumeration that specifies what type of information the function queries.</span></span>

<span data-ttu-id="630c0-106">Las variables de atributo de seguridad deben estar presentes en el contexto del cliente si se hace referencia a ellas en una expresión condicional; de lo contrario, el término de expresión condicional que hace referencia a ellos se evaluará como desconocido.</span><span class="sxs-lookup"><span data-stu-id="630c0-106">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="630c0-107">Para obtener más información sobre las expresiones condicionales, vea el tema [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="630c0-107">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

## <a name="example"></a><span data-ttu-id="630c0-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="630c0-108">Example</span></span>

<span data-ttu-id="630c0-109">En el ejemplo siguiente se consulta el contexto de cliente creado en el ejemplo de [inicialización de un contexto de cliente](initializing-a-client-context.md) para recuperar la lista de [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) de grupos asociados a ese contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="630c0-109">The following example queries the client context created in the example from [Initializing a Client Context](initializing-a-client-context.md) to retrieve the list of [**SIDs**](/windows/desktop/api/Winnt/ns-winnt-sid) of groups associated with that client context.</span></span>


```C++
BOOL GetGroupsFromContext(AUTHZ_CLIENT_CONTEXT_HANDLE hClientContext)
{

    DWORD                cbSize = 0;
    PTOKEN_GROUPS        pTokenGroups=NULL;
    LPTSTR                StringSid = NULL;
    BOOL                bResult = FALSE;
    int i = 0;

    //Call the AuthzGetInformationFromContext function with a NULL output buffer to get the required buffer size.
    AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, 0, &cbSize, NULL);
    
        
    

    //Allocate the buffer for the TOKEN_GROUPS structure.
    pTokenGroups = (PTOKEN_GROUPS)malloc(cbSize);
    if (!pTokenGroups)
        return FALSE;

    //Get the SIDs of groups associated with the client context. 
    if(!AuthzGetInformationFromContext(hClientContext, AuthzContextInfoGroupsSids, cbSize, &cbSize, pTokenGroups))
    {    
        printf_s("AuthzGetInformationFromContext failed with %d\n", GetLastError);
        free(pTokenGroups);
        return FALSE;
    }

    //Enumerate and display the group SIDs.
    for (i=pTokenGroups->GroupCount-1; i >= 0; --i)
    {
        //Convert a SID to a string.
        if(!ConvertSidToStringSid(
            pTokenGroups->Groups[i].Sid,
            &StringSid
            ))
        {
            LocalFree(StringSid);
            return FALSE;
        }


        wprintf_s(L"%s \n", StringSid);
        
    }

    free(pTokenGroups);

    return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="630c0-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="630c0-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="630c0-111">Agregar SID a un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="630c0-111">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="630c0-112">Almacenar en caché comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="630c0-112">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="630c0-113">Comprobación del acceso con la API de authz</span><span class="sxs-lookup"><span data-stu-id="630c0-113">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="630c0-114">Cómo funciona AccessCheck</span><span class="sxs-lookup"><span data-stu-id="630c0-114">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="630c0-115">Inicializar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="630c0-115">Initializing a Client Context</span></span>](initializing-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="630c0-116">Lenguaje de definición de descriptores de seguridad para ACE condicionales</span><span class="sxs-lookup"><span data-stu-id="630c0-116">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> </dl>

 

 



