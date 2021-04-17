---
description: Las siguientes estructuras admiten las funciones de la API de la tabla de enrutamiento distribuida (DRT).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Estructuras de tabla de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667443"
---
# <a name="distributed-routing-table-structures"></a><span data-ttu-id="26d3f-103">Estructuras de tabla de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="26d3f-103">Distributed Routing Table Structures</span></span>

<span data-ttu-id="26d3f-104">Las siguientes estructuras admiten las funciones de la API de la tabla de enrutamiento distribuida (DRT).</span><span class="sxs-lookup"><span data-stu-id="26d3f-104">The following structures support the Distributed Routing Table (DRT) API functions.</span></span>



| <span data-ttu-id="26d3f-105">Estructura</span><span class="sxs-lookup"><span data-stu-id="26d3f-105">Structure</span></span>                                                  | <span data-ttu-id="26d3f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="26d3f-106">Description</span></span>                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26d3f-107">**datos de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="26d3f-107">**DRT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_data)                              | <span data-ttu-id="26d3f-108">Contiene un BLOB de datos.</span><span class="sxs-lookup"><span data-stu-id="26d3f-108">Contains a data blob.</span></span> <span data-ttu-id="26d3f-109">Varias funciones DRT utilizan esta estructura.</span><span class="sxs-lookup"><span data-stu-id="26d3f-109">This structure is used by several DRT functions.</span></span>                                                                                                                   |
| [<span data-ttu-id="26d3f-110">**registro de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="26d3f-110">**DRT\_REGISTRATION**</span></span>](/windows/desktop/api/drt/ns-drt-drt_registration)              | <span data-ttu-id="26d3f-111">Contiene el registro de claves.</span><span class="sxs-lookup"><span data-stu-id="26d3f-111">Contains the key registration.</span></span> <span data-ttu-id="26d3f-112">Este es un miembro de la estructura del [**\_ \_ resultado**](/windows/desktop/api/drt/ns-drt-drt_search_result) de la búsqueda de DRT y es un argumento pasado a [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span><span class="sxs-lookup"><span data-stu-id="26d3f-112">This is a member of the [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) structure and is an argument passed to [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span></span> |
| [<span data-ttu-id="26d3f-113">**Dirección de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="26d3f-113">**DRT\_ADDRESS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address)                        | <span data-ttu-id="26d3f-114">Contiene información de extremo sobre un nodo DRT que participó en una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="26d3f-114">Contains endpoint information about a DRT node that participated in a search.</span></span> <span data-ttu-id="26d3f-115">Esta información está pensada para su uso en la depuración de problemas de conectividad.</span><span class="sxs-lookup"><span data-stu-id="26d3f-115">This information is intended for use in debugging connectivity problems.</span></span>                                   |
| [<span data-ttu-id="26d3f-116">**\_lista de direcciones de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="26d3f-116">**DRT\_ADDRESS\_LIST**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address_list)             | <span data-ttu-id="26d3f-117">Contiene un conjunto de estructuras de [**\_ direcciones de DRT**](/windows/desktop/api/drt/ns-drt-drt_address) que representan los nodos a los que se pone en contacto durante una búsqueda de una clave.</span><span class="sxs-lookup"><span data-stu-id="26d3f-117">Contains a set of [**DRT\_ADDRESS**](/windows/desktop/api/drt/ns-drt-drt_address) structures representing the nodes contacted during a search for a key.</span></span>                                                             |
| [<span data-ttu-id="26d3f-118">**\_proveedor de seguridad de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="26d3f-118">**DRT\_SECURITY\_PROVIDER**</span></span>](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | <span data-ttu-id="26d3f-119">Define la interfaz que debe ser implementada por un proveedor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="26d3f-119">Defines the interface that must be implemented by a security provider.</span></span>                                                                                                                   |
| [<span data-ttu-id="26d3f-120">**\_proveedor de arranque de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="26d3f-120">**DRT\_BOOTSTRAP\_PROVIDER**</span></span>](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | <span data-ttu-id="26d3f-121">Define la interfaz que debe ser implementada por un proveedor de arranque.</span><span class="sxs-lookup"><span data-stu-id="26d3f-121">Defines the interface that must be implemented by a bootstrap provider.</span></span>                                                                                                                  |
| [<span data-ttu-id="26d3f-122">**configuración de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="26d3f-122">**DRT\_SETTINGS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_settings)                      | <span data-ttu-id="26d3f-123">Define la configuración de DRT en la inicialización.</span><span class="sxs-lookup"><span data-stu-id="26d3f-123">Defines DRT settings at initialization.</span></span> <span data-ttu-id="26d3f-124">Esta estructura se pasa como argumento a [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).</span><span class="sxs-lookup"><span data-stu-id="26d3f-124">This structure is passed as an argument to [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).</span></span>                                                                           |
| [<span data-ttu-id="26d3f-125">**\_información de búsqueda de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="26d3f-125">**DRT\_SEARCH\_INFO**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_info)               | <span data-ttu-id="26d3f-126">Define una consulta de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="26d3f-126">Defines a search query.</span></span> <span data-ttu-id="26d3f-127">Esta estructura se pasa como argumento a [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span><span class="sxs-lookup"><span data-stu-id="26d3f-127">This structure is passed as an argument to [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span></span>                                                                             |
| [<span data-ttu-id="26d3f-128">**resultado de la búsqueda de DRT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="26d3f-128">**DRT\_SEARCH\_RESULT**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_result)           | <span data-ttu-id="26d3f-129">Contiene un resultado de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="26d3f-129">Contains a search result.</span></span> <span data-ttu-id="26d3f-130">[**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)devuelve esta estructura.</span><span class="sxs-lookup"><span data-stu-id="26d3f-130">This structure is returned by [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).</span></span>                                                                                |
| [<span data-ttu-id="26d3f-131">**\_datos de eventos de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="26d3f-131">**DRT\_EVENT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | <span data-ttu-id="26d3f-132">Contiene los datos de evento devueltos mediante una llamada a [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) después de que una aplicación reciba una señal de evento.</span><span class="sxs-lookup"><span data-stu-id="26d3f-132">Contains the event data returned by calling [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) after an application receives an event signal.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="26d3f-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26d3f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26d3f-134">Enumeraciones de tabla de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="26d3f-134">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="26d3f-135">Funciones de tabla de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="26d3f-135">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="26d3f-136">Referencia de Table API de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="26d3f-136">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



