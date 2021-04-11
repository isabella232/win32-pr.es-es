---
description: Marcas de capacidad del controlador D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e774076f5ad93abf5ab1ffc343f573497592728f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274938"
---
# <a name="d3ddevcaps2"></a><span data-ttu-id="e93cf-103">D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="e93cf-103">D3DDEVCAPS2</span></span>

<span data-ttu-id="e93cf-104">Marcas de capacidad del controlador D3DDEVCAPS2.</span><span class="sxs-lookup"><span data-stu-id="e93cf-104">D3DDEVCAPS2 driver capability flags.</span></span>



|                                                 |                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e93cf-105">\#define</span><span class="sxs-lookup"><span data-stu-id="e93cf-105">\#define</span></span>                                        | <span data-ttu-id="e93cf-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="e93cf-106">Description</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="e93cf-107">D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH</span><span class="sxs-lookup"><span data-stu-id="e93cf-107">D3DDEVCAPS2\_ADAPTIVETESSRTPATCH</span></span>                | <span data-ttu-id="e93cf-108">El dispositivo admite teselación adaptable de RT-patchs</span><span class="sxs-lookup"><span data-stu-id="e93cf-108">Device supports adaptive tessellation of RT-patches</span></span>                                                                                                                                                                       |
| <span data-ttu-id="e93cf-109">D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH</span><span class="sxs-lookup"><span data-stu-id="e93cf-109">D3DDEVCAPS2\_ADAPTIVETESSNPATCH</span></span>                 | <span data-ttu-id="e93cf-110">El dispositivo admite teselación adaptable de N-patches.</span><span class="sxs-lookup"><span data-stu-id="e93cf-110">Device supports adaptive tessellation of N-patches.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="e93cf-111">D3DDEVCAPS2 \_ puede \_ STRETCHRECT \_ de \_ texturas</span><span class="sxs-lookup"><span data-stu-id="e93cf-111">D3DDEVCAPS2\_CAN\_STRETCHRECT\_FROM\_TEXTURES</span></span>   | <span data-ttu-id="e93cf-112">El dispositivo admite [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) con una textura como origen.</span><span class="sxs-lookup"><span data-stu-id="e93cf-112">Device supports [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) using a texture as the source.</span></span>                                                                                                                       |
| <span data-ttu-id="e93cf-113">D3DDEVCAPS2 \_ DMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="e93cf-113">D3DDEVCAPS2\_DMAPNPATCH</span></span>                         | <span data-ttu-id="e93cf-114">El dispositivo admite los mapas de desplazamiento para N-patches.</span><span class="sxs-lookup"><span data-stu-id="e93cf-114">Device supports displacement maps for N-patches.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="e93cf-115">D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="e93cf-115">D3DDEVCAPS2\_PRESAMPLEDDMAPNPATCH</span></span>               | <span data-ttu-id="e93cf-116">El dispositivo admite los mapas de desplazamiento premuestreados para N-patches.</span><span class="sxs-lookup"><span data-stu-id="e93cf-116">Device supports presampled displacement maps for N-patches.</span></span> <span data-ttu-id="e93cf-117">Para obtener más información acerca de la asignación de desplazamiento, vea [asignación de desplazamiento (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="e93cf-117">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span>                                           |
| <span data-ttu-id="e93cf-118">D3DDEVCAPS2 \_ STREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="e93cf-118">D3DDEVCAPS2\_STREAMOFFSET</span></span>                       | <span data-ttu-id="e93cf-119">El dispositivo admite desplazamientos de flujo.</span><span class="sxs-lookup"><span data-stu-id="e93cf-119">Device supports stream offsets.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="e93cf-120">D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="e93cf-120">D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET</span></span> | <span data-ttu-id="e93cf-121">Varios elementos VERTEX pueden compartir el mismo desplazamiento en un flujo si \_ el dispositivo establece D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET y la declaración de vértices no tiene un elemento con D3DDECLUSAGE \_ POSITIONT0.</span><span class="sxs-lookup"><span data-stu-id="e93cf-121">Multiple vertex elements can share the same offset in a stream if D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET is set by the device and the vertex declaration does not have an element with D3DDECLUSAGE\_POSITIONT0.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="e93cf-122">Información constante</span><span class="sxs-lookup"><span data-stu-id="e93cf-122">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="e93cf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e93cf-123">Header</span></span>                   | <span data-ttu-id="e93cf-124">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="e93cf-124">d3d9caps.h</span></span> |
| <span data-ttu-id="e93cf-125">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="e93cf-125">Minimum operating system</span></span> | <span data-ttu-id="e93cf-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e93cf-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e93cf-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e93cf-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e93cf-128">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="e93cf-128">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
