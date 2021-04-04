---
title: Marcas de salto siguiente
description: Marcas de salto siguiente
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Siguientes
- Marcas de salto siguiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076208"
---
# <a name="next-hop-flags"></a><span data-ttu-id="4100f-105">Marcas de salto siguiente</span><span class="sxs-lookup"><span data-stu-id="4100f-105">Next Hop Flags</span></span>

## <a name="next-hop-state-flags"></a><span data-ttu-id="4100f-106">Marcas de estado de próximo salto</span><span class="sxs-lookup"><span data-stu-id="4100f-106">Next Hop State Flags</span></span>



| <span data-ttu-id="4100f-107">Constante</span><span class="sxs-lookup"><span data-stu-id="4100f-107">Constant</span></span>                     | <span data-ttu-id="4100f-108">Value</span><span class="sxs-lookup"><span data-stu-id="4100f-108">Value</span></span> | <span data-ttu-id="4100f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4100f-109">Description</span></span>                              |
|------------------------------|-------|------------------------------------------|
| <span data-ttu-id="4100f-110">Estado de NEXTHOP de RTM \_ \_ \_ creado</span><span class="sxs-lookup"><span data-stu-id="4100f-110">RTM\_NEXTHOP\_STATE\_CREATED</span></span> | <span data-ttu-id="4100f-111">0</span><span class="sxs-lookup"><span data-stu-id="4100f-111">0</span></span>     | <span data-ttu-id="4100f-112">Indica que se ha creado el próximo salto.</span><span class="sxs-lookup"><span data-stu-id="4100f-112">Indicates that the next hop was created.</span></span> |
| <span data-ttu-id="4100f-113">Estado de NEXTHOP de RTM \_ \_ \_ eliminado</span><span class="sxs-lookup"><span data-stu-id="4100f-113">RTM\_NEXTHOP\_STATE\_DELETED</span></span> | <span data-ttu-id="4100f-114">1</span><span class="sxs-lookup"><span data-stu-id="4100f-114">1</span></span>     | <span data-ttu-id="4100f-115">Indica que se eliminó el próximo salto.</span><span class="sxs-lookup"><span data-stu-id="4100f-115">Indicates that the next hop was deleted.</span></span> |



 

## <a name="next-hop-flags"></a><span data-ttu-id="4100f-116">Marcas de salto siguiente</span><span class="sxs-lookup"><span data-stu-id="4100f-116">Next Hop Flags</span></span>



| <span data-ttu-id="4100f-117">Constante</span><span class="sxs-lookup"><span data-stu-id="4100f-117">Constant</span></span>                    | <span data-ttu-id="4100f-118">Value</span><span class="sxs-lookup"><span data-stu-id="4100f-118">Value</span></span>  | <span data-ttu-id="4100f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4100f-119">Description</span></span>                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4100f-120">marcas de salto de RTM \_ \_ \_ remotas</span><span class="sxs-lookup"><span data-stu-id="4100f-120">RTM\_NEXTHOP\_FLAGS\_REMOTE</span></span> | <span data-ttu-id="4100f-121">0x0001</span><span class="sxs-lookup"><span data-stu-id="4100f-121">0x0001</span></span> | <span data-ttu-id="4100f-122">Este próximo salto apunta a un destino remoto que no es accesible directamente.</span><span class="sxs-lookup"><span data-stu-id="4100f-122">This next hop points to a remote destination that is not directly reachable.</span></span> <span data-ttu-id="4100f-123">Para obtener la ruta de acceso completa, el cliente debe realizar una búsqueda recursiva.</span><span class="sxs-lookup"><span data-stu-id="4100f-123">To obtain the complete path, the client must perform a recursive lookup.</span></span> |
| <span data-ttu-id="4100f-124">marcas de salto de RTM \_ \_ \_ inactivas</span><span class="sxs-lookup"><span data-stu-id="4100f-124">RTM\_NEXTHOP\_FLAGS\_DOWN</span></span>   | <span data-ttu-id="4100f-125">0x0002</span><span class="sxs-lookup"><span data-stu-id="4100f-125">0x0002</span></span> | <span data-ttu-id="4100f-126">Esta marca se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4100f-126">This flag is reserved for future use.</span></span>                                                                                                                 |



 

## <a name="next-hop-added"></a><span data-ttu-id="4100f-127">Próximo salto agregado</span><span class="sxs-lookup"><span data-stu-id="4100f-127">Next Hop Added</span></span>



| <span data-ttu-id="4100f-128">Constante</span><span class="sxs-lookup"><span data-stu-id="4100f-128">Constant</span></span>                  | <span data-ttu-id="4100f-129">Value</span><span class="sxs-lookup"><span data-stu-id="4100f-129">Value</span></span> | <span data-ttu-id="4100f-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="4100f-130">Description</span></span>                 |
|---------------------------|-------|-----------------------------|
| <span data-ttu-id="4100f-131">cambio de NEXTHOP de RTM \_ \_ \_ nuevo</span><span class="sxs-lookup"><span data-stu-id="4100f-131">RTM\_NEXTHOP\_CHANGE\_NEW</span></span> | <span data-ttu-id="4100f-132">0x01</span><span class="sxs-lookup"><span data-stu-id="4100f-132">0x01</span></span>  | <span data-ttu-id="4100f-133">Se creó un próximo salto nuevo.</span><span class="sxs-lookup"><span data-stu-id="4100f-133">A new next hop was created.</span></span> |



 

 

 




