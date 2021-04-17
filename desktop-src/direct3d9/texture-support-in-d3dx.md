---
description: D3DX es una biblioteca de utilidades que proporciona servicios auxiliares. Es una capa por encima del componente Direct3D.
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: Compatibilidad con texturas en D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9c8d6da498a47d14fe57ca770ba96a6852ae41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705189"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="cbfea-104">Compatibilidad con texturas en D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cbfea-104">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="cbfea-105">D3DX es una biblioteca de utilidades que proporciona servicios auxiliares.</span><span class="sxs-lookup"><span data-stu-id="cbfea-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="cbfea-106">Es una capa por encima del componente Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cbfea-106">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="cbfea-107">Texturas</span><span class="sxs-lookup"><span data-stu-id="cbfea-107">Textures</span></span>

<span data-ttu-id="cbfea-108">En los temas siguientes se admiten muchas texturas diferentes.</span><span class="sxs-lookup"><span data-stu-id="cbfea-108">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="cbfea-109">Compatibilidad con la textura de mipmapped estándar.</span><span class="sxs-lookup"><span data-stu-id="cbfea-109">Standard mipmapped texture support.</span></span> <span data-ttu-id="cbfea-110">Vea [generación automática de mapas MIP (Direct3D 9)](automatic-generation-of-mipmaps.md).</span><span class="sxs-lookup"><span data-stu-id="cbfea-110">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="cbfea-111">Compatibilidad con mapas de cubos.</span><span class="sxs-lookup"><span data-stu-id="cbfea-111">Cube map support.</span></span> <span data-ttu-id="cbfea-112">Vea [asignación de entorno cúbica (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="cbfea-112">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="cbfea-113">Compatibilidad con texturas de volumen.</span><span class="sxs-lookup"><span data-stu-id="cbfea-113">Volume texture support.</span></span> <span data-ttu-id="cbfea-114">Vea [recursos de textura de volumen (Direct3D 9)](volume-texture-resources.md).</span><span class="sxs-lookup"><span data-stu-id="cbfea-114">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="cbfea-115">Compatibilidad con la asignación de entorno.</span><span class="sxs-lookup"><span data-stu-id="cbfea-115">Environment mapping support.</span></span> <span data-ttu-id="cbfea-116">Consulte [asignación de entorno (Direct3D 9)](environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="cbfea-116">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="cbfea-117">Compatibilidad con la asignación de rugosidad.</span><span class="sxs-lookup"><span data-stu-id="cbfea-117">Bump mapping support.</span></span> <span data-ttu-id="cbfea-118">Vea [asignación de rugosidad (Direct3D 9)](bump-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="cbfea-118">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="cbfea-119">Conversión de color de textura</span><span class="sxs-lookup"><span data-stu-id="cbfea-119">Texture Color Conversion</span></span>

<span data-ttu-id="cbfea-120">Al usar cualquiera de las funciones D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx o D3DXCreateVolumeTexturexxx, es posible que sea necesario realizar la conversión de colores.</span><span class="sxs-lookup"><span data-stu-id="cbfea-120">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="cbfea-121">Por ejemplo, una superficie podría ser de tipo RGBA y la otra podría ser UVWQ.</span><span class="sxs-lookup"><span data-stu-id="cbfea-121">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="cbfea-122">En los casos de formatos distintos, la secuencia de conversión es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="cbfea-122">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="cbfea-123">Asignación de RGBA a UVWQ</span><span class="sxs-lookup"><span data-stu-id="cbfea-123">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="cbfea-124">R <-> U, el canal R está asignado al canal U, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="cbfea-124">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="cbfea-125">G <-> V, el canal G está asignado al canal V, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="cbfea-125">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="cbfea-126">B <-> W, el canal B está asignado al canal W, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="cbfea-126">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="cbfea-127">Una < > Q/L, se asigna un canal al canal Q o L (en función de cuál esté disponible en el formato de destino), o viceversa.</span><span class="sxs-lookup"><span data-stu-id="cbfea-127">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="cbfea-128">Asignación de UV a RGBA</span><span class="sxs-lookup"><span data-stu-id="cbfea-128">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="cbfea-129">U <-> R, el canal U está asignado al canal R, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="cbfea-129">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="cbfea-130">V <-> G, el canal V está asignado al canal G, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="cbfea-130">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="cbfea-131">1 <-> B, 1 se asigna al canal B, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="cbfea-131">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="cbfea-132">1 <-> a, 1 se asigna a un canal, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="cbfea-132">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="cbfea-133">Si un canal no existe en el origen, se supone que es 1 (con la excepción de A8, donde R, G, B se supone que es 0).</span><span class="sxs-lookup"><span data-stu-id="cbfea-133">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="cbfea-134">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cbfea-134">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="cbfea-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cbfea-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbfea-136">D3DX</span><span class="sxs-lookup"><span data-stu-id="cbfea-136">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



