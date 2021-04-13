---
description: Authz API permite a las aplicaciones realizar comprobaciones de acceso personalizables con un mejor rendimiento y un desarrollo más simplificado que los Access Control de bajo nivel.
ms.assetid: 83df96ff-f3d6-43f8-88b2-6387914b3503
title: Uso de la API de authz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86394c0df408307ae4c49377af4a1ae8cc1f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361540"
---
# <a name="using-authz-api"></a><span data-ttu-id="dcbe3-103">Uso de la API de authz</span><span class="sxs-lookup"><span data-stu-id="dcbe3-103">Using Authz API</span></span>

<span data-ttu-id="dcbe3-104">Authz API permite a las aplicaciones realizar comprobaciones de acceso personalizables con un mejor rendimiento y un desarrollo más simplificado que los [Access Control de bajo nivel](low-level-access-control.md).</span><span class="sxs-lookup"><span data-stu-id="dcbe3-104">Authz API allows applications to perform customizable access checks with better performance and more simplified development than [Low-level Access Control](low-level-access-control.md).</span></span>

<span data-ttu-id="dcbe3-105">Authz API permite a las aplicaciones almacenar en caché las comprobaciones de acceso para mejorar el rendimiento, consultar y modificar contextos de cliente, y definir reglas de negocios que se pueden usar para evaluar dinámicamente el permiso de acceso.</span><span class="sxs-lookup"><span data-stu-id="dcbe3-105">Authz API allows applications to cache access checks for improved performance, to query and modify client contexts, and to define business rules that can be used to evaluate access permission dynamically.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dcbe3-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="dcbe3-106">In This Section</span></span>



| <span data-ttu-id="dcbe3-107">Tema</span><span class="sxs-lookup"><span data-stu-id="dcbe3-107">Topic</span></span>                                                                             | <span data-ttu-id="dcbe3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcbe3-108">Description</span></span>                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dcbe3-109">Inicializar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="dcbe3-109">Initializing a Client Context</span></span>](initializing-a-client-context.md)<br/>     | <span data-ttu-id="dcbe3-110">Una aplicación debe crear un contexto de cliente para poder usar la API de authz para realizar comprobaciones de acceso o auditoría.</span><span class="sxs-lookup"><span data-stu-id="dcbe3-110">An application must create a client context before it can use Authz API to perform access checks or auditing.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="dcbe3-111">Consultar un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="dcbe3-111">Querying a Client Context</span></span>](querying-a-client-context.md)<br/>             | <span data-ttu-id="dcbe3-112">Las aplicaciones pueden llamar a la función [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) para consultar información sobre un contexto de cliente existente.</span><span class="sxs-lookup"><span data-stu-id="dcbe3-112">Applications can call the [**AuthzGetInformationFromContext**](/windows/desktop/api/Authz/nf-authz-authzgetinformationfromcontext) function to query information about an existing client context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="dcbe3-113">Agregar SID a un contexto de cliente</span><span class="sxs-lookup"><span data-stu-id="dcbe3-113">Adding SIDs to a Client Context</span></span>](adding-sids-to-a-client-context.md)<br/> | <span data-ttu-id="dcbe3-114">Una aplicación puede agregar [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) a un contexto de cliente existente llamando a la función [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) .</span><span class="sxs-lookup"><span data-stu-id="dcbe3-114">An application can add [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) to an existing client context by calling the [**AuthzAddSidsToContext**](/windows/desktop/api/Authz/nf-authz-authzaddsidstocontext) function.</span></span><br/> |
| [<span data-ttu-id="dcbe3-115">Comprobación del acceso con la API de authz</span><span class="sxs-lookup"><span data-stu-id="dcbe3-115">Checking Access with Authz API</span></span>](checking-access-with-authz-api.md)<br/>   | <span data-ttu-id="dcbe3-116">Las aplicaciones determinan si se debe conceder acceso a los objetos protegibles mediante una llamada a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="dcbe3-116">Applications determine whether to grant access to securable objects by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="dcbe3-117">Almacenar en caché comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="dcbe3-117">Caching Access Checks</span></span>](caching-access-checks.md)<br/>                     | <span data-ttu-id="dcbe3-118">Cuando una aplicación realiza una comprobación de acceso mediante una llamada a la función [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) , los resultados de esa comprobación de acceso se pueden almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="dcbe3-118">When an application performs an access check by calling the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function, the results of that access check can be cached.</span></span><br/>                                                                                       |



 

 

