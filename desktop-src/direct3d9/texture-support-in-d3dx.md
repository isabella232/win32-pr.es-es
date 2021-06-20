---
description: Obtenga información sobre la compatibilidad con texturas en D3DX. D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Compatibilidad con texturas en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f31a597ddcab317477d31e0d833c9da96f71ed4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404608"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="21da6-105">Compatibilidad con texturas en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="21da6-105">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="21da6-106">D3DX es una biblioteca de utilidades que proporciona servicios auxiliares.</span><span class="sxs-lookup"><span data-stu-id="21da6-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="21da6-107">Es una capa por encima del componente Direct3D.</span><span class="sxs-lookup"><span data-stu-id="21da6-107">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="21da6-108">Texturas</span><span class="sxs-lookup"><span data-stu-id="21da6-108">Textures</span></span>

<span data-ttu-id="21da6-109">En los temas siguientes se admiten muchas texturas diferentes.</span><span class="sxs-lookup"><span data-stu-id="21da6-109">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="21da6-110">Compatibilidad con texturas mipmapped estándar.</span><span class="sxs-lookup"><span data-stu-id="21da6-110">Standard mipmapped texture support.</span></span> <span data-ttu-id="21da6-111">Vea [Generación automática de mapas Mip (Direct3D 9).](automatic-generation-of-mipmaps.md)</span><span class="sxs-lookup"><span data-stu-id="21da6-111">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="21da6-112">Compatibilidad con mapas de cubos.</span><span class="sxs-lookup"><span data-stu-id="21da6-112">Cube map support.</span></span> <span data-ttu-id="21da6-113">Vea [Asignación de entorno cúbica (Direct3D 9).](cubic-environment-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="21da6-113">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="21da6-114">Compatibilidad con texturas de volumen.</span><span class="sxs-lookup"><span data-stu-id="21da6-114">Volume texture support.</span></span> <span data-ttu-id="21da6-115">Vea [Recursos de textura de volumen (Direct3D 9).](volume-texture-resources.md)</span><span class="sxs-lookup"><span data-stu-id="21da6-115">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="21da6-116">Compatibilidad con la asignación de entornos.</span><span class="sxs-lookup"><span data-stu-id="21da6-116">Environment mapping support.</span></span> <span data-ttu-id="21da6-117">Vea [Asignación de entorno (Direct3D 9).](environment-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="21da6-117">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="21da6-118">Compatibilidad con la asignación de protuberancias.</span><span class="sxs-lookup"><span data-stu-id="21da6-118">Bump mapping support.</span></span> <span data-ttu-id="21da6-119">Vea [Asignación de protuberancias (Direct3D 9).](bump-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="21da6-119">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="21da6-120">Conversión de color de textura</span><span class="sxs-lookup"><span data-stu-id="21da6-120">Texture Color Conversion</span></span>

<span data-ttu-id="21da6-121">Al usar cualquiera de las funciones D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx o D3DXCreateVolumeTexturexxx, es posible que sea necesario realizar la conversión de color.</span><span class="sxs-lookup"><span data-stu-id="21da6-121">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="21da6-122">Por ejemplo, una superficie podría ser de tipo RGBA y la otra podría ser UVWQ.</span><span class="sxs-lookup"><span data-stu-id="21da6-122">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="21da6-123">Para los casos de formatos diferentes, la secuencia de conversión es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="21da6-123">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="21da6-124">Asignación de RGBA a UVWQ</span><span class="sxs-lookup"><span data-stu-id="21da6-124">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="21da6-125">R <-> U, el canal R se asigna al canal U o viceversa.</span><span class="sxs-lookup"><span data-stu-id="21da6-125">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="21da6-126">G <-> V, el canal G se asigna al canal V o viceversa.</span><span class="sxs-lookup"><span data-stu-id="21da6-126">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="21da6-127">B <-> W, el canal B se asigna al canal W o viceversa.</span><span class="sxs-lookup"><span data-stu-id="21da6-127">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="21da6-128">Un <-> Q/L, un canal se asigna al canal Q o L (dependiendo de cuál esté disponible en el formato de destino) o viceversa.</span><span class="sxs-lookup"><span data-stu-id="21da6-128">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="21da6-129">Asignación de UV a RGBA</span><span class="sxs-lookup"><span data-stu-id="21da6-129">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="21da6-130">U <-> R, el canal U se asigna al canal de R o viceversa.</span><span class="sxs-lookup"><span data-stu-id="21da6-130">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="21da6-131">V <-> G, el canal V se asigna al canal G, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="21da6-131">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="21da6-132">1 <-> B, 1 se asigna al canal B o viceversa.</span><span class="sxs-lookup"><span data-stu-id="21da6-132">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="21da6-133">1 <-> A, 1 se asigna al canal A o viceversa.</span><span class="sxs-lookup"><span data-stu-id="21da6-133">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="21da6-134">Si un canal no existe en el origen, se supone que es 1 (a excepción de A8, donde se supone que R,G,B es 0).</span><span class="sxs-lookup"><span data-stu-id="21da6-134">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="21da6-135">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="21da6-135">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="21da6-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="21da6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21da6-137">D3DX</span><span class="sxs-lookup"><span data-stu-id="21da6-137">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



