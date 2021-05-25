---
description: Marcas de funcionalidad del controlador D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6296db9b338d5f9a8c8ede702a784baf1fdfd462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343210"
---
# <a name="d3ddevcaps2"></a><span data-ttu-id="25d83-103">D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="25d83-103">D3DDEVCAPS2</span></span>

<span data-ttu-id="25d83-104">Marcas de funcionalidad del controlador D3DDEVCAPS2.</span><span class="sxs-lookup"><span data-stu-id="25d83-104">D3DDEVCAPS2 driver capability flags.</span></span>



| <span data-ttu-id="25d83-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="25d83-105">\#define</span></span>                                        | <span data-ttu-id="25d83-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="25d83-106">Description</span></span>                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25d83-107">D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH</span><span class="sxs-lookup"><span data-stu-id="25d83-107">D3DDEVCAPS2\_ADAPTIVETESSRTPATCH</span></span>                | <span data-ttu-id="25d83-108">El dispositivo admite la teselación adaptable de revisiones RT</span><span class="sxs-lookup"><span data-stu-id="25d83-108">Device supports adaptive tessellation of RT-patches</span></span>                                                                                                                                                                       |
| <span data-ttu-id="25d83-109">D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH</span><span class="sxs-lookup"><span data-stu-id="25d83-109">D3DDEVCAPS2\_ADAPTIVETESSNPATCH</span></span>                 | <span data-ttu-id="25d83-110">El dispositivo admite la teselación adaptable de N revisiones.</span><span class="sxs-lookup"><span data-stu-id="25d83-110">Device supports adaptive tessellation of N-patches.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="25d83-111">D3DDEVCAPS2 \_ PUEDE \_ EXTENDERSE DESDE \_ \_ TEXTURAS</span><span class="sxs-lookup"><span data-stu-id="25d83-111">D3DDEVCAPS2\_CAN\_STRETCHRECT\_FROM\_TEXTURES</span></span>   | <span data-ttu-id="25d83-112">El dispositivo [**admite StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) mediante una textura como origen.</span><span class="sxs-lookup"><span data-stu-id="25d83-112">Device supports [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) using a texture as the source.</span></span>                                                                                                                       |
| <span data-ttu-id="25d83-113">D3DDEVCAPS2 \_ DMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="25d83-113">D3DDEVCAPS2\_DMAPNPATCH</span></span>                         | <span data-ttu-id="25d83-114">El dispositivo admite mapas de desplazamiento para N revisiones.</span><span class="sxs-lookup"><span data-stu-id="25d83-114">Device supports displacement maps for N-patches.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="25d83-115">D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="25d83-115">D3DDEVCAPS2\_PRESAMPLEDDMAPNPATCH</span></span>               | <span data-ttu-id="25d83-116">El dispositivo admite mapas de desplazamiento previamente muestreados para N revisiones.</span><span class="sxs-lookup"><span data-stu-id="25d83-116">Device supports presampled displacement maps for N-patches.</span></span> <span data-ttu-id="25d83-117">Para obtener más información sobre la asignación de desplazamiento, vea [Asignación de desplazamiento (Direct3D 9).](displacement-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="25d83-117">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span>                                           |
| <span data-ttu-id="25d83-118">D3DDEVCAPS2 \_ STREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="25d83-118">D3DDEVCAPS2\_STREAMOFFSET</span></span>                       | <span data-ttu-id="25d83-119">El dispositivo admite desplazamientos de flujo.</span><span class="sxs-lookup"><span data-stu-id="25d83-119">Device supports stream offsets.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="25d83-120">D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="25d83-120">D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET</span></span> | <span data-ttu-id="25d83-121">Varios elementos de vértice pueden compartir el mismo desplazamiento en una secuencia si el dispositivo establece D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET y la declaración de vértice no tiene un elemento con \_ D3DDECLUSAGE \_ POSITIONT0.</span><span class="sxs-lookup"><span data-stu-id="25d83-121">Multiple vertex elements can share the same offset in a stream if D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET is set by the device and the vertex declaration does not have an element with D3DDECLUSAGE\_POSITIONT0.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="25d83-122">Información constante</span><span class="sxs-lookup"><span data-stu-id="25d83-122">Constant Information</span></span>



| <span data-ttu-id="25d83-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="25d83-123">Requirement</span></span>                         | <span data-ttu-id="25d83-124">Value</span><span class="sxs-lookup"><span data-stu-id="25d83-124">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="25d83-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25d83-125">Header</span></span>                   | <span data-ttu-id="25d83-126">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="25d83-126">d3d9caps.h</span></span> |
| <span data-ttu-id="25d83-127">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="25d83-127">Minimum operating system</span></span> | <span data-ttu-id="25d83-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="25d83-128">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="25d83-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="25d83-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25d83-130">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="25d83-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
