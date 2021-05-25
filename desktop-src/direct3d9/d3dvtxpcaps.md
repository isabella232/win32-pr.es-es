---
description: Obtenga información sobre una combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ad3b5eca7a264e489382d80b336f5b2c660e1a
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342920"
---
# <a name="d3dvtxpcaps"></a><span data-ttu-id="7807d-103">D3DVTXPCAPS</span><span class="sxs-lookup"><span data-stu-id="7807d-103">D3DVTXPCAPS</span></span>

<span data-ttu-id="7807d-104">Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7807d-104">A combination of one or more flags that control the device create behavior.</span></span>



| <span data-ttu-id="7807d-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="7807d-105">\#define</span></span>                                | <span data-ttu-id="7807d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="7807d-106">Description</span></span>                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7807d-107">D3DVTXPCAPS \_ DIRECTIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="7807d-107">D3DVTXPCAPS\_DIRECTIONALLIGHTS</span></span>          | <span data-ttu-id="7807d-108">El dispositivo puede hacer luces direccionales.</span><span class="sxs-lookup"><span data-stu-id="7807d-108">Device can do directional lights.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="7807d-109">D3DVTXPCAPS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="7807d-109">D3DVTXPCAPS\_LOCALVIEWER</span></span>                | <span data-ttu-id="7807d-110">El dispositivo puede hacer visor local.</span><span class="sxs-lookup"><span data-stu-id="7807d-110">Device can do local viewer.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="7807d-111">D3DVTXPCAPS \_ MATERIALSOURCE7</span><span class="sxs-lookup"><span data-stu-id="7807d-111">D3DVTXPCAPS\_MATERIALSOURCE7</span></span>            | <span data-ttu-id="7807d-112">Cuando se establece este límite, el dispositivo admite los estados de material de color: D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE y D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="7807d-112">When this cap is set, the device supports the color material states: D3DRS\_AMBIENTMATERIALSOURCE, D3DRS\_DIFFUSEMATERIALSOURCE, D3DRS\_EMISSIVEMATERIALSOURCE, and D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="7807d-113">D3DVTXPCAPS \_ NO HAY NINGÚN \_ \_ NOLOCALVIEWER DE TEXASGEN</span><span class="sxs-lookup"><span data-stu-id="7807d-113">D3DVTXPCAPS\_NO\_TEXGEN\_NONLOCALVIEWER</span></span> | <span data-ttu-id="7807d-114">El dispositivo no admite la generación de texturas en el modo de visor no local.</span><span class="sxs-lookup"><span data-stu-id="7807d-114">Device does not support texture generation in non-local viewer mode.</span></span>                                                                                                                               |
| <span data-ttu-id="7807d-115">D3DVTXPCAPS \_ POSITIONALLIGHTS</span><span class="sxs-lookup"><span data-stu-id="7807d-115">D3DVTXPCAPS\_POSITIONALLIGHTS</span></span>           | <span data-ttu-id="7807d-116">El dispositivo puede realizar luces posicionales (incluye un punto y un punto).</span><span class="sxs-lookup"><span data-stu-id="7807d-116">Device can do positional lights (includes point and spot).</span></span>                                                                                                                                         |
| <span data-ttu-id="7807d-117">D3DVTXPCAPS \_ TEXGEN</span><span class="sxs-lookup"><span data-stu-id="7807d-117">D3DVTXPCAPS\_TEXGEN</span></span>                     | <span data-ttu-id="7807d-118">El dispositivo puede realizar la hazgen.</span><span class="sxs-lookup"><span data-stu-id="7807d-118">Device can do texgen.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="7807d-119">D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP</span><span class="sxs-lookup"><span data-stu-id="7807d-119">D3DVTXPCAPS\_TEXGEN\_SPHEREMAP</span></span>          | <span data-ttu-id="7807d-120">El dispositivo admite D3DTSS \_ TCI \_ SPHEREMAP.</span><span class="sxs-lookup"><span data-stu-id="7807d-120">Device supports D3DTSS\_TCI\_SPHEREMAP.</span></span>                                                                                                                                                            |
| <span data-ttu-id="7807d-121">INTERPOLACIÓN DE D3DVTXPCAPS \_</span><span class="sxs-lookup"><span data-stu-id="7807d-121">D3DVTXPCAPS\_TWEENING</span></span>                   | <span data-ttu-id="7807d-122">El dispositivo puede realizar la interpolación de vértices.</span><span class="sxs-lookup"><span data-stu-id="7807d-122">Device can do vertex tweening.</span></span>                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="7807d-123">Información constante</span><span class="sxs-lookup"><span data-stu-id="7807d-123">Constant Information</span></span>



| <span data-ttu-id="7807d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7807d-124">Requirement</span></span>                         | <span data-ttu-id="7807d-125">Value</span><span class="sxs-lookup"><span data-stu-id="7807d-125">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="7807d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7807d-126">Header</span></span>                   | <span data-ttu-id="7807d-127">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="7807d-127">d3d9caps.h</span></span> |
| <span data-ttu-id="7807d-128">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="7807d-128">Minimum operating system</span></span> | <span data-ttu-id="7807d-129">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7807d-129">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7807d-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7807d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7807d-131">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="7807d-131">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



