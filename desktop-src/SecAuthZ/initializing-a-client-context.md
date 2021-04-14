---
description: Una aplicación debe crear un contexto de cliente para poder usar la API de authz para realizar comprobaciones de acceso o auditoría.
ms.assetid: 82f207ff-cac4-4e9a-a9e6-ddb3f6c8b30a
title: Inicializar un contexto de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be229a60a12e33ab0c2bbd3e52fc533cf29ed1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668398"
---
# <a name="initializing-a-client-context"></a><span data-ttu-id="ccfd4-103">Inicializar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="ccfd4-103">Initializing a Client Context</span></span>

<span data-ttu-id="ccfd4-104">Una aplicación debe crear un contexto de cliente para poder usar la API de authz para realizar comprobaciones de acceso o auditoría.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-104">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span>

<span data-ttu-id="ccfd4-105">Una aplicación debe llamar a la función [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) para inicializar el administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-105">An application must call the [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager) function to initialize the resource manager.</span></span> <span data-ttu-id="ccfd4-106">A continuación, la aplicación puede llamar a una de varias funciones para crear un contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-106">The application can then call one of several functions to create a client context.</span></span> <span data-ttu-id="ccfd4-107">Además, si está realizando comprobaciones de acceso o auditorías de forma remota, debe usar la función [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="ccfd4-107">Additionally, if you are performing access checks or auditing remotely, you must use the [**AuthzInitializeRemoteResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager) function.</span></span>

<span data-ttu-id="ccfd4-108">Para crear un contexto de cliente basado en un contexto de cliente existente, llame a la función [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) .</span><span class="sxs-lookup"><span data-stu-id="ccfd4-108">To create a client context based on an existing client context, call the [**AuthzInitializeContextFromAuthzContext**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromauthzcontext) function.</span></span>

<span data-ttu-id="ccfd4-109">La función [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) crea un nuevo contexto de cliente usando información en un token de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-109">The [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function creates a new client context by using information in a logon token.</span></span> <span data-ttu-id="ccfd4-110">La función [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) crea un nuevo contexto de cliente mediante el [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)especificado.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-110">The [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid) function creates a new client context by using the specified [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid).</span></span>

<span data-ttu-id="ccfd4-111">Si es posible, llame a la función [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) en lugar de a [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span><span class="sxs-lookup"><span data-stu-id="ccfd4-111">If possible, call the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function instead of [**AuthzInitializeContextFromSid**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromsid).</span></span> <span data-ttu-id="ccfd4-112">**AuthzInitializeContextFromSid** intenta recuperar la información disponible en un token de inicio de sesión en el que el cliente ha iniciado sesión realmente.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-112">**AuthzInitializeContextFromSid** attempts to retrieve the information available in a logon token had the client actually logged on.</span></span> <span data-ttu-id="ccfd4-113">Un token de inicio de sesión real proporciona más información, como el tipo de inicio de sesión y las propiedades de inicio de sesión, y refleja el comportamiento del paquete de autenticación usado para el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-113">An actual logon token provides more information, such as logon type and logon properties, and reflects the behavior of the authentication package used for the logon.</span></span> <span data-ttu-id="ccfd4-114">El contexto de cliente creado por **AuthzInitializeContextFromToken** utiliza un token de inicio de sesión y el contexto de cliente resultante es más completo y preciso que un contexto de cliente creado por **AuthzInitializeContextFromSid**.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-114">The client context created by **AuthzInitializeContextFromToken** uses a logon token, and the resulting client context is more complete and accurate than a client context created by **AuthzInitializeContextFromSid**.</span></span>

> [!Note]  
> <span data-ttu-id="ccfd4-115">Las variables de atributo de seguridad deben estar presentes en el contexto del cliente si se hace referencia a ellas en una expresión condicional; de lo contrario, el término de expresión condicional que hace referencia a ellos se evaluará como desconocido.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-115">Security attribute variables must be present in the client context if referred to in a conditional expression; otherwise, the conditional expression term referencing them will be evaluated as unknown.</span></span> <span data-ttu-id="ccfd4-116">Para obtener más información sobre las expresiones condicionales, vea el tema [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md) .</span><span class="sxs-lookup"><span data-stu-id="ccfd4-116">For more information on conditional expressions, see the [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md) topic.</span></span>

 

## <a name="example"></a><span data-ttu-id="ccfd4-117">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ccfd4-117">Example</span></span>

<span data-ttu-id="ccfd4-118">En el ejemplo siguiente se inicializa el administrador de recursos de authz y se llama a la función [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) para crear un contexto de cliente a partir del token de inicio de sesión asociado al proceso actual.</span><span class="sxs-lookup"><span data-stu-id="ccfd4-118">The following example initializes the Authz resource manager and calls the [**AuthzInitializeContextFromToken**](/windows/desktop/api/Authz/nf-authz-authzinitializecontextfromtoken) function to create a client context from the logon token associated with the current process.</span></span>


```C++
BOOL AuthzInitFromToken(AUTHZ_CLIENT_CONTEXT_HANDLE *phClientContext)
{

    HANDLE                            hToken = NULL;
    LUID                            Luid = {0, 0};

    
    ULONG                            uFlags = 0;


    //Initialize Resource Manager
    if(!AuthzInitializeResourceManager(
        AUTHZ_RM_FLAG_NO_AUDIT,
        NULL,
        NULL,
        NULL,
        L"My Resource Manager",
        &g_hResourceManager
        ))
    {
        printf_s("AuthzInitializeResourceManager failed with %d\n", GetLastError);
        return FALSE;
    }
    

    //Get the current token.

    if(!OpenProcessToken(GetCurrentProcess(), TOKEN_ALL_ACCESS, &hToken))
    {
        printf_s("OpenProcessToken failed with %d\n", GetLastError);
        return FALSE;
    }


    //Initialize the client context

    if(!AuthzInitializeContextFromToken(
        0,
        hToken,
        g_hResourceManager,
        NULL,
        Luid,
        NULL,
        phClientContext
        ))
    {    
        printf_s("AuthzInitializeContextFromToken failed with %d\n", GetLastError);
        return FALSE;
    }

    
    printf_s("Initialized client context. \n");
    return TRUE;

}
```



## <a name="related-topics"></a><span data-ttu-id="ccfd4-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ccfd4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccfd4-120">Agregar SID a un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="ccfd4-120">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="ccfd4-121">Almacenar en caché comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="ccfd4-121">Caching Access Checks</span></span>](caching-access-checks.md)
</dt> <dt>

[<span data-ttu-id="ccfd4-122">Comprobación del acceso con la API de authz</span><span class="sxs-lookup"><span data-stu-id="ccfd4-122">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)
</dt> <dt>

[<span data-ttu-id="ccfd4-123">Cómo funciona AccessCheck</span><span class="sxs-lookup"><span data-stu-id="ccfd4-123">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="ccfd4-124">Consultar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="ccfd4-124">Querying a Client Context</span></span>](querying-a-client-context.md)
</dt> <dt>

[<span data-ttu-id="ccfd4-125">Lenguaje de definición de descriptores de seguridad para ACE condicionales</span><span class="sxs-lookup"><span data-stu-id="ccfd4-125">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="ccfd4-126">**AuthzInitializeRemoteResourceManager**</span><span class="sxs-lookup"><span data-stu-id="ccfd4-126">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="ccfd4-127">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="ccfd4-127">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

 



