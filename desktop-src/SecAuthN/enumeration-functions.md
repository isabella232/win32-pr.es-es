---
description: Si el proveedor de red necesita admitir la exploración de sus recursos de red, debe implementar las siguientes funciones. MPR llama a estas funciones para enumerar los recursos.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Funciones de enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2670424be1540aad3e46e32c5b0606eb02e04bdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082060"
---
# <a name="enumeration-functions"></a><span data-ttu-id="3c75f-104">Funciones de enumeración</span><span class="sxs-lookup"><span data-stu-id="3c75f-104">Enumeration Functions</span></span>

<span data-ttu-id="3c75f-105">Si el proveedor de red necesita admitir la exploración de sus recursos de red, debe implementar las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="3c75f-105">If your network provider needs to support browsing of its network resources, it should implement the following functions.</span></span> <span data-ttu-id="3c75f-106">MPR llama a estas funciones para enumerar los recursos.</span><span class="sxs-lookup"><span data-stu-id="3c75f-106">MPR calls these functions to enumerate the resources.</span></span>

<span data-ttu-id="3c75f-107">No es necesario que un proveedor de red implemente ninguna de las funciones de enumeración.</span><span class="sxs-lookup"><span data-stu-id="3c75f-107">A network provider is not required to implement any of the enumeration functions.</span></span> <span data-ttu-id="3c75f-108">Sin embargo, si un proveedor de red implementa [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)o [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), también debe implementar las otras dos funciones de enumeración.</span><span class="sxs-lookup"><span data-stu-id="3c75f-108">If, however, a network provider implements either [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource), or [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), it must also implement the other two enumeration functions.</span></span>



| <span data-ttu-id="3c75f-109">Función</span><span class="sxs-lookup"><span data-stu-id="3c75f-109">Function</span></span>                                                     | <span data-ttu-id="3c75f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c75f-110">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c75f-111">**NPOpenEnum**</span><span class="sxs-lookup"><span data-stu-id="3c75f-111">**NPOpenEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | <span data-ttu-id="3c75f-112">Abre una enumeración de recursos de red o conexiones existentes.</span><span class="sxs-lookup"><span data-stu-id="3c75f-112">Opens an enumeration of network resources or existing connections.</span></span>                                                                                                  |
| [<span data-ttu-id="3c75f-113">**NPEnumResource**</span><span class="sxs-lookup"><span data-stu-id="3c75f-113">**NPEnumResource**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | <span data-ttu-id="3c75f-114">Realiza una enumeración en un identificador devuelto por [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span><span class="sxs-lookup"><span data-stu-id="3c75f-114">Performs an enumeration on a handle returned by [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).</span></span>                                                                                   |
| [<span data-ttu-id="3c75f-115">**NPCloseEnum**</span><span class="sxs-lookup"><span data-stu-id="3c75f-115">**NPCloseEnum**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | <span data-ttu-id="3c75f-116">Cierra una enumeración.</span><span class="sxs-lookup"><span data-stu-id="3c75f-116">Closes an enumeration.</span></span>                                                                                                                                              |
| [<span data-ttu-id="3c75f-117">**NPGetResourceInformation**</span><span class="sxs-lookup"><span data-stu-id="3c75f-117">**NPGetResourceInformation**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | <span data-ttu-id="3c75f-118">Determina si el proveedor es el proveedor correcto para responder a una solicitud de un recurso de red especificado y devuelve información sobre el tipo del recurso.</span><span class="sxs-lookup"><span data-stu-id="3c75f-118">Determines whether the provider is the correct provider to respond to a request for a specified network resource and returns information about the resource's type.</span></span> |
| [<span data-ttu-id="3c75f-119">**NPGetResourceParent**</span><span class="sxs-lookup"><span data-stu-id="3c75f-119">**NPGetResourceParent**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | <span data-ttu-id="3c75f-120">Devuelve el elemento primario de un recurso de red especificado en la jerarquía de exploración.</span><span class="sxs-lookup"><span data-stu-id="3c75f-120">Returns the parent of a specified network resource in the browse hierarchy.</span></span>                                                                                         |



 

 

 



