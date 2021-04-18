---
description: Los Estados de efecto son pares nombre-valor en forma de expresión.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Grupos de estado del efecto (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361947"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="c40a9-103">Grupos de estado del efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="c40a9-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="c40a9-104">Los Estados de efecto son pares nombre-valor en forma de expresión.</span><span class="sxs-lookup"><span data-stu-id="c40a9-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="c40a9-105">Estado de Blend</span><span class="sxs-lookup"><span data-stu-id="c40a9-105">Blend state</span></span>

| | |
|-|-|
| <span data-ttu-id="c40a9-106">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="c40a9-106">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="c40a9-107">Miembros de [ **D3D10 \_ Blend \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="c40a9-107">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="c40a9-108">Profundidad y estado de estarcido</span><span class="sxs-lookup"><span data-stu-id="c40a9-108">Depth and stencil state</span></span>

| | |
|-|-|
| <span data-ttu-id="c40a9-109">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="c40a9-109">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="c40a9-110">Miembros de la [ **Galería de símbolos de \_ profundidad D3D10 \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="c40a9-110">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="c40a9-111">FRONTFACESTENCILFAIL \* \*, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="c40a9-111">FRONTFACESTENCILFAIL\*\*, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="c40a9-112">Miembro de [ **D3D10 \_ Depth \_ STENCILOP \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="c40a9-112">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="c40a9-113">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="c40a9-113">Rasterizer state</span></span>

| | |
|-|-|
| <span data-ttu-id="c40a9-114">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="c40a9-114">FILLMODE</span></span> | [<span data-ttu-id="c40a9-115">**\_Modo de relleno de D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="c40a9-115">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="c40a9-116">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="c40a9-116">CULLMODE</span></span> | [<span data-ttu-id="c40a9-117">**\_Modo de selección de D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="c40a9-117">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="c40a9-118">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="c40a9-118">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="c40a9-119">Miembros de [ **D3D10 \_ rasterizador \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="c40a9-119">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="c40a9-120">Estado de muestra</span><span class="sxs-lookup"><span data-stu-id="c40a9-120">Sampler state</span></span>

| | |
|-|-|
| <span data-ttu-id="c40a9-121">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span><span class="sxs-lookup"><span data-stu-id="c40a9-121">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="c40a9-122">Miembros de la [ **\_ muestra D3D10 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="c40a9-122">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="c40a9-123">Consulte [tipo de muestra (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) para obtener ejemplos.</span><span class="sxs-lookup"><span data-stu-id="c40a9-123">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="c40a9-124">Estado del objeto de efecto</span><span class="sxs-lookup"><span data-stu-id="c40a9-124">Effect object state</span></span>

| <span data-ttu-id="c40a9-125">Este objeto de efecto</span><span class="sxs-lookup"><span data-stu-id="c40a9-125">This effect object</span></span> | <span data-ttu-id="c40a9-126">Se asigna a</span><span class="sxs-lookup"><span data-stu-id="c40a9-126">Maps to</span></span> |
|-|-|
| <span data-ttu-id="c40a9-127">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="c40a9-127">RASTERIZERSTATE</span></span> | <span data-ttu-id="c40a9-128">Objeto de estado de [Estado de rasterizador](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="c40a9-128">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="c40a9-129">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="c40a9-129">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="c40a9-130">Objeto de estado de [Estado de estarcido y de profundidad](#depth-and-stencil-state) .</span><span class="sxs-lookup"><span data-stu-id="c40a9-130">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="c40a9-131">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="c40a9-131">BLENDSTATE</span></span> | <span data-ttu-id="c40a9-132">Objeto de estado de [Estado de Blend](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="c40a9-132">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="c40a9-133">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="c40a9-133">VERTEXSHADER</span></span> | <span data-ttu-id="c40a9-134">Objeto de sombreador de vértices compilado.</span><span class="sxs-lookup"><span data-stu-id="c40a9-134">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="c40a9-135">U</span><span class="sxs-lookup"><span data-stu-id="c40a9-135">PIXELSHADER</span></span> | <span data-ttu-id="c40a9-136">Objeto de sombreador de píxeles compilado.</span><span class="sxs-lookup"><span data-stu-id="c40a9-136">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="c40a9-137">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="c40a9-137">GEOMETRYSHADER</span></span> | <span data-ttu-id="c40a9-138">Objeto de sombreador de geometría compilado.</span><span class="sxs-lookup"><span data-stu-id="c40a9-138">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="c40a9-139">DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="c40a9-139">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="c40a9-140">Miembros de [**D3D10 \_ Pass \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span><span class="sxs-lookup"><span data-stu-id="c40a9-140">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="c40a9-141">Definir y usar objetos de estado</span><span class="sxs-lookup"><span data-stu-id="c40a9-141">Defining and using state objects</span></span>

<span data-ttu-id="c40a9-142">Los objetos de estado se declaran en archivos FX con el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="c40a9-142">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="c40a9-143">*StateObjectType* es uno de los Estados enumerados anteriormente y *memberName* es el nombre de cualquier miembro que tenga un valor no predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c40a9-143">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="c40a9-144">Por ejemplo, para configurar un objeto de estado de Blend con AlphaToCoverageEnable y BlendEnable \[ 0 \] establecido en **false**, se utilizaría el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="c40a9-144">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="c40a9-145">El objeto de estado se aplica a un paso de técnica mediante una de las funciones de SetStateGroup descritas en sintaxis de la [técnica de efectos (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="c40a9-145">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="c40a9-146">Por ejemplo, para aplicar el objeto BlendState descrito anteriormente, se utilizaría el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="c40a9-146">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="c40a9-147">Para ver un tutorial en el que se describe el uso de Estados, consulte [Administración](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)de Estados.</span><span class="sxs-lookup"><span data-stu-id="c40a9-147">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c40a9-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c40a9-148">Related topics</span></span>

* [<span data-ttu-id="c40a9-149">Sintaxis de la técnica de efectos</span><span class="sxs-lookup"><span data-stu-id="c40a9-149">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="c40a9-150">Formato de efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="c40a9-150">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
