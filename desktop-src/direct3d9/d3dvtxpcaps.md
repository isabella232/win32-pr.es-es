---
description: Obtenga información sobre una combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo en la constante D3DVTXPCAPS.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b544f3e4a69de23607366832aca110e42c61d6d
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011088"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="04364-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="04364-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="04364-104">Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04364-104">A combination of one or more flags that control the device create behavior.</span></span>



| <span data-ttu-id="04364-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="04364-105">\#define</span></span>                                | <span data-ttu-id="04364-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="04364-106">Description</span></span>                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04364-107">D3DVTXPCAPS \_ DIRECTIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="04364-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="04364-108">El dispositivo puede hacer luces direccionales.</span><span class="sxs-lookup"><span data-stu-id="04364-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="04364-109">D3DVTXPCAPS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="04364-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="04364-110">El dispositivo puede hacer visor local.</span><span class="sxs-lookup"><span data-stu-id="04364-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="04364-111">D3DVTXPCAPS \_ MATERIALSOURCE7</span><span class="sxs-lookup"><span data-stu-id="04364-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="04364-112">Cuando se establece este límite, el dispositivo admite los estados de material de color: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE y D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="04364-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="04364-113">D3DVTXPCAPS \_ NO TIENE UN \_ \_ NOLOCALVIEWER DE TEXGEN</span><span class="sxs-lookup"><span data-stu-id="04364-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="04364-114">El dispositivo no admite la generación de texturas en modo de visor no local.</span><span class="sxs-lookup"><span data-stu-id="04364-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="04364-115">D3DVTXPCAPS \_ POSITIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="04364-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="04364-116">El dispositivo puede hacer luces posicionales (incluye un punto y un punto).</span><span class="sxs-lookup"><span data-stu-id="04364-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="04364-117">D3DVTXPCAPS \_ TEXGEN</span><span class="sxs-lookup"><span data-stu-id="04364-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="04364-118">El dispositivo puede hacer el hazgen.</span><span class="sxs-lookup"><span data-stu-id="04364-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="04364-119">D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="04364-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="04364-120">El dispositivo admite D3DTSS \_ TCI \_ SPHEREMAP.</span><span class="sxs-lookup"><span data-stu-id="04364-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="04364-121">INTERPOLACIÓN DE D3DVTXPCAPS \_</span><span class="sxs-lookup"><span data-stu-id="04364-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="04364-122">El dispositivo puede realizar la interpolación de vértices.</span><span class="sxs-lookup"><span data-stu-id="04364-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="04364-123">Información constante</span><span class="sxs-lookup"><span data-stu-id="04364-123">Constant Information</span></span>



| <span data-ttu-id="04364-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="04364-124">Requirement</span></span>                         | <span data-ttu-id="04364-125">Value</span><span class="sxs-lookup"><span data-stu-id="04364-125">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="04364-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04364-126">Header</span></span>                   | <span data-ttu-id="04364-127">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="04364-127">d3d9caps.h</span></span> |
| <span data-ttu-id="04364-128">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="04364-128">Minimum operating system</span></span> | <span data-ttu-id="04364-129">Windows 98</span><span class="sxs-lookup"><span data-stu-id="04364-129">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="04364-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04364-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04364-131">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="04364-131">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



