---
description: Los estados de efecto son pares nombre-valor en forma de expresión.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Grupos de estado del efecto (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335579"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="706f2-103">Grupos de estado del efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="706f2-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="706f2-104">Los estados de efecto son pares nombre-valor en forma de expresión.</span><span class="sxs-lookup"><span data-stu-id="706f2-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="706f2-105">Estado de blend</span><span class="sxs-lookup"><span data-stu-id="706f2-105">Blend state</span></span>

| <span data-ttu-id="706f2-106">Estado del efecto</span><span class="sxs-lookup"><span data-stu-id="706f2-106">Effect state</span></span> | <span data-ttu-id="706f2-107">Grupo</span><span class="sxs-lookup"><span data-stu-id="706f2-107">Group</span></span> |
|-|-|
| <span data-ttu-id="706f2-108">**ALPHATOCOVERAGEENABLE,** **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP,** **SRCBLEPHA,** **DESTBLEPHA,** **BLENDOPALPHA,** **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="706f2-108">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="706f2-109">Miembros de [ **D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="706f2-109">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="706f2-110">Profundidad y estado de galería de símbolos</span><span class="sxs-lookup"><span data-stu-id="706f2-110">Depth and stencil state</span></span>

| <span data-ttu-id="706f2-111">Estado del efecto</span><span class="sxs-lookup"><span data-stu-id="706f2-111">Effect state</span></span>| <span data-ttu-id="706f2-112">Grupo</span><span class="sxs-lookup"><span data-stu-id="706f2-112">Group</span></span> |
|-|-|
| <span data-ttu-id="706f2-113">**DEPTHENABLE**, **DEPTHWRITEMASK,** **DEPTHFUNC,** **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="706f2-113">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="706f2-114">Miembros de [ **D3D10 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="706f2-114">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="706f2-115">**FRONTFACESTENCICOHERENCIAIL,** **FRONTFACESTENCILZFAIL,** **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC,** **BACKFACESTENCINCIIL,** **BACKFACESTENCILZFAIL,** **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="706f2-115">**FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="706f2-116">Miembro de [ **D3D10 \_ DEPTH \_ STENCISTONE \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="706f2-116">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="706f2-117">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="706f2-117">Rasterizer state</span></span>

| <span data-ttu-id="706f2-118">Estado del efecto</span><span class="sxs-lookup"><span data-stu-id="706f2-118">Effect state</span></span>| <span data-ttu-id="706f2-119">Grupo</span><span class="sxs-lookup"><span data-stu-id="706f2-119">Group</span></span> |
|-|-|
| <span data-ttu-id="706f2-120">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="706f2-120">FILLMODE</span></span> | [<span data-ttu-id="706f2-121">**MODO DE RELLENO D3D10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="706f2-121">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="706f2-122">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="706f2-122">CULLMODE</span></span> | [<span data-ttu-id="706f2-123">**MODO CULL D3D10 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="706f2-123">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="706f2-124">**FRONTCOUNTERCLOCKWISE,** **DEPTHBIAS**, DEPTHBIASCLAMP,SAMPLEEDDEPTHBIAS, **ZCLIPENABLE,SAMPLEENABLE,**  **MULTISAMPLEENABLE,** **ANTIALIASEDLINEENABLE**  </span><span class="sxs-lookup"><span data-stu-id="706f2-124">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="706f2-125">Miembros de [ **D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="706f2-125">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="706f2-126">Estado del muestreador</span><span class="sxs-lookup"><span data-stu-id="706f2-126">Sampler state</span></span>

| <span data-ttu-id="706f2-127">Estado del efecto</span><span class="sxs-lookup"><span data-stu-id="706f2-127">Effect state</span></span> | <span data-ttu-id="706f2-128">Grupo</span><span class="sxs-lookup"><span data-stu-id="706f2-128">Group</span></span> |
|-|-|
| <span data-ttu-id="706f2-129">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc,** **BorderColor**, **MinLOD**, **MaxLOD**</span><span class="sxs-lookup"><span data-stu-id="706f2-129">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="706f2-130">Miembros de [ **D3D10 \_ SAMPLER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="706f2-130">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="706f2-131">Vea [Sampler type (DirectX HLSL) (Tipo de sampler [HLSL de DirectX])](../direct3dhlsl/dx-graphics-hlsl-sampler.md) para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="706f2-131">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="706f2-132">Estado del objeto de efecto</span><span class="sxs-lookup"><span data-stu-id="706f2-132">Effect object state</span></span>

| <span data-ttu-id="706f2-133">Este objeto de efecto</span><span class="sxs-lookup"><span data-stu-id="706f2-133">This effect object</span></span> | <span data-ttu-id="706f2-134">Se asigna a</span><span class="sxs-lookup"><span data-stu-id="706f2-134">Maps to</span></span> |
|-|-|
| <span data-ttu-id="706f2-135">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="706f2-135">RASTERIZERSTATE</span></span> | <span data-ttu-id="706f2-136">Objeto [de estado de rasterizador.](#rasterizer-state)</span><span class="sxs-lookup"><span data-stu-id="706f2-136">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="706f2-137">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="706f2-137">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="706f2-138">Objeto [de estado Depth y Stencil State.](#depth-and-stencil-state)</span><span class="sxs-lookup"><span data-stu-id="706f2-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="706f2-139">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="706f2-139">BLENDSTATE</span></span> | <span data-ttu-id="706f2-140">Objeto [de estado de blend.](#blend-state)</span><span class="sxs-lookup"><span data-stu-id="706f2-140">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="706f2-141">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="706f2-141">VERTEXSHADER</span></span> | <span data-ttu-id="706f2-142">Objeto de sombreador de vértices compilado.</span><span class="sxs-lookup"><span data-stu-id="706f2-142">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="706f2-143">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="706f2-143">PIXELSHADER</span></span> | <span data-ttu-id="706f2-144">Objeto de sombreador de píxeles compilado.</span><span class="sxs-lookup"><span data-stu-id="706f2-144">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="706f2-145">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="706f2-145">GEOMETRYSHADER</span></span> | <span data-ttu-id="706f2-146">Objeto de sombreador de geometría compilado.</span><span class="sxs-lookup"><span data-stu-id="706f2-146">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="706f2-147">DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="706f2-147">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="706f2-148">Miembros de [**D3D10 \_ PASS \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span><span class="sxs-lookup"><span data-stu-id="706f2-148">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="706f2-149">Definición y uso de objetos de estado</span><span class="sxs-lookup"><span data-stu-id="706f2-149">Defining and using state objects</span></span>

<span data-ttu-id="706f2-150">Los objetos de estado se declaran en archivos FX en el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="706f2-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="706f2-151">*StateObjectType es* uno de los estados enumerados anteriormente y *MemberName* es el nombre de cualquier miembro que tenga un valor no predeterminado.</span><span class="sxs-lookup"><span data-stu-id="706f2-151">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="706f2-152">Por ejemplo, para configurar un objeto de estado de mezcla con AlphaToCoverageEnable y BlendEnable 0 establecidos en FALSE, se usaría \[ \] el código siguiente. </span><span class="sxs-lookup"><span data-stu-id="706f2-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="706f2-153">El objeto de estado se aplica a un paso de técnica mediante una de las funciones SetStateGroup descritas en Sintaxis de técnica de [efecto (Direct3D 10).](d3d10-effect-technique-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="706f2-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="706f2-154">Por ejemplo, para aplicar el objeto BlendState descrito anteriormente, se usaría el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="706f2-154">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="706f2-155">Para ver un tutorial en el que se describe el uso de estados, vea [Administración de estado.](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="706f2-155">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="706f2-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="706f2-156">Related topics</span></span>

* [<span data-ttu-id="706f2-157">Sintaxis de la técnica de efecto</span><span class="sxs-lookup"><span data-stu-id="706f2-157">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="706f2-158">Formato de efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="706f2-158">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
