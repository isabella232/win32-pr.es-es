---
title: Ver marcas
description: Use las marcas de vista para controlar las vistas de tabla de enrutamiento.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676243"
---
# <a name="view-flags"></a><span data-ttu-id="af1a0-103">Ver marcas</span><span class="sxs-lookup"><span data-stu-id="af1a0-103">View Flags</span></span>

<span data-ttu-id="af1a0-104">Use las marcas de vista para controlar las vistas de tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="af1a0-104">Use the View Flags to control routing table views.</span></span>



| <span data-ttu-id="af1a0-105">Constante</span><span class="sxs-lookup"><span data-stu-id="af1a0-105">Constant</span></span>                 | <span data-ttu-id="af1a0-106">Value</span><span class="sxs-lookup"><span data-stu-id="af1a0-106">Value</span></span>      | <span data-ttu-id="af1a0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="af1a0-107">Description</span></span>                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| <span data-ttu-id="af1a0-108">\_tamaño máximo de la \_ Dirección RTM \_</span><span class="sxs-lookup"><span data-stu-id="af1a0-108">RTM\_MAX \_ADDRESS\_SIZE</span></span> | <span data-ttu-id="af1a0-109">16</span><span class="sxs-lookup"><span data-stu-id="af1a0-109">16</span></span>         | <span data-ttu-id="af1a0-110">Tamaño máximo de la dirección de una familia de direcciones.</span><span class="sxs-lookup"><span data-stu-id="af1a0-110">Max address size for an address family.</span></span>                          |
| <span data-ttu-id="af1a0-111">\_vistas máximas de RTM \_</span><span class="sxs-lookup"><span data-stu-id="af1a0-111">RTM\_MAX\_VIEWS</span></span>          | <span data-ttu-id="af1a0-112">32</span><span class="sxs-lookup"><span data-stu-id="af1a0-112">32</span></span>         | <span data-ttu-id="af1a0-113">Número máximo de vistas que pueden estar activas en la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="af1a0-113">Maximum number of views that can be active in the routing table.</span></span> |
| <span data-ttu-id="af1a0-114">\_ID. de vista RTM \_ \_ UCAST</span><span class="sxs-lookup"><span data-stu-id="af1a0-114">RTM\_VIEW\_ID\_UCAST</span></span>     | <span data-ttu-id="af1a0-115">0</span><span class="sxs-lookup"><span data-stu-id="af1a0-115">0</span></span>          | <span data-ttu-id="af1a0-116">Especifica una vista de unidifusión.</span><span class="sxs-lookup"><span data-stu-id="af1a0-116">Specifies a unicast view.</span></span>                                        |
| <span data-ttu-id="af1a0-117">\_ID. de vista RTM \_ \_ MCAST</span><span class="sxs-lookup"><span data-stu-id="af1a0-117">RTM\_VIEW\_ID\_MCAST</span></span>     | <span data-ttu-id="af1a0-118">1</span><span class="sxs-lookup"><span data-stu-id="af1a0-118">1</span></span>          | <span data-ttu-id="af1a0-119">Especifica una vista de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="af1a0-119">Specifies a multicast view.</span></span>                                      |
| <span data-ttu-id="af1a0-120">tamaño de la \_ máscara de vista RTM \_ \_</span><span class="sxs-lookup"><span data-stu-id="af1a0-120">RTM\_VIEW\_MASK\_SIZE</span></span>    | <span data-ttu-id="af1a0-121">0x20</span><span class="sxs-lookup"><span data-stu-id="af1a0-121">0x20</span></span>       | <span data-ttu-id="af1a0-122">Especifica el número máximo de vistas que se pueden configurar.</span><span class="sxs-lookup"><span data-stu-id="af1a0-122">Specifies the maximum number of views that can be configured.</span></span>    |
| <span data-ttu-id="af1a0-123">vista de RTM de la \_ \_ máscara \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="af1a0-123">RTM\_VIEW\_MASK\_NONE</span></span>    | <span data-ttu-id="af1a0-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af1a0-124">0x00000000</span></span> | <span data-ttu-id="af1a0-125">Devuelve información independientemente de la vista.</span><span class="sxs-lookup"><span data-stu-id="af1a0-125">Returns information regardless of the view.</span></span>                      |
| <span data-ttu-id="af1a0-126">RTM \_ Ver \_ máscara \_ cualquiera</span><span class="sxs-lookup"><span data-stu-id="af1a0-126">RTM\_VIEW\_MASK\_ANY</span></span>     | <span data-ttu-id="af1a0-127">0x00000000</span><span class="sxs-lookup"><span data-stu-id="af1a0-127">0x00000000</span></span> | <span data-ttu-id="af1a0-128">Devuelve destinos de todas las vistas.</span><span class="sxs-lookup"><span data-stu-id="af1a0-128">Returns destinations from all views.</span></span> <span data-ttu-id="af1a0-129">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="af1a0-129">This is the default value.</span></span>  |
| <span data-ttu-id="af1a0-130">RTM \_ vista de \_ máscara de \_ UCAST</span><span class="sxs-lookup"><span data-stu-id="af1a0-130">RTM\_VIEW\_MASK\_UCAST</span></span>   | <span data-ttu-id="af1a0-131">0x00000001</span><span class="sxs-lookup"><span data-stu-id="af1a0-131">0x00000001</span></span> | <span data-ttu-id="af1a0-132">Devuelve destinos de la vista de unidifusión.</span><span class="sxs-lookup"><span data-stu-id="af1a0-132">Returns destinations from the unicast view.</span></span>                      |
| <span data-ttu-id="af1a0-133">RTM \_ vista de \_ máscara de \_ MCAST</span><span class="sxs-lookup"><span data-stu-id="af1a0-133">RTM\_VIEW\_MASK\_MCAST</span></span>   | <span data-ttu-id="af1a0-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="af1a0-134">0x00000002</span></span> | <span data-ttu-id="af1a0-135">Devuelve destinos de la vista multidifusión.</span><span class="sxs-lookup"><span data-stu-id="af1a0-135">Returns destinations from the multicast view.</span></span>                    |
| <span data-ttu-id="af1a0-136">RTM \_ Ver \_ máscara \_ todo</span><span class="sxs-lookup"><span data-stu-id="af1a0-136">RTM\_VIEW\_MASK\_ALL</span></span>     | <span data-ttu-id="af1a0-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="af1a0-137">0xFFFFFFFF</span></span> | <span data-ttu-id="af1a0-138">Devuelve información de todas las vistas.</span><span class="sxs-lookup"><span data-stu-id="af1a0-138">Returns information from all views.</span></span>                              |



 

 

 




