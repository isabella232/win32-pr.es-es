---
title: Modelo de sombreador 4
description: El modelo de sombreador 4 es un supraconjunto de las funcionalidades del modelo de sombreador 3, con la excepción de que el modelo de sombreador 4 no es compatible con las características del modelo de sombreador 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f1964eaf84e9b0a2669f59357f54d16b1b4cbd3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420175"
---
# <a name="shader-model-4"></a><span data-ttu-id="8e7c3-103">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8e7c3-103">Shader Model 4</span></span>

<span data-ttu-id="8e7c3-104">El modelo de sombreador 4 es un supraconjunto de las funcionalidades del [modelo de sombreador 3](dx-graphics-hlsl-sm3.md), con la excepción de que el modelo de sombreador 4 no es compatible con las características del modelo de sombreador 1.</span><span class="sxs-lookup"><span data-stu-id="8e7c3-104">Shader Model 4 is a superset of the capabilities in [Shader Model 3](dx-graphics-hlsl-sm3.md), except that Shader Model 4 doesn't support the features in Shader Model 1.</span></span> <span data-ttu-id="8e7c3-105">Se ha diseñado con un núcleo de sombreador común que proporciona un conjunto común de características a todos los sombreadores programables, que solo se pueden programar mediante HLSL.</span><span class="sxs-lookup"><span data-stu-id="8e7c3-105">It has been designed using a common-shader core that gives a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e7c3-106">Característica</span><span class="sxs-lookup"><span data-stu-id="8e7c3-106">Feature</span></span></th>
<th><span data-ttu-id="8e7c3-107">Funcionalidad</span><span class="sxs-lookup"><span data-stu-id="8e7c3-107">Capability</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e7c3-108">Conjunto de instrucciones</span><span class="sxs-lookup"><span data-stu-id="8e7c3-108">Instruction Set</span></span></td>
<td><span data-ttu-id="8e7c3-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funciones de HLSL</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e7c3-109"><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>HLSL functions</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e7c3-110">Conjunto de registros</span><span class="sxs-lookup"><span data-stu-id="8e7c3-110">Register Set</span></span></td>
<td><span data-ttu-id="8e7c3-111">Se puede tener acceso al conjunto de registros a través de los miembros de búferes de constantes y texturas mediante la semántica de HLSL para elementos como el empaquetado de componentes.</span><span class="sxs-lookup"><span data-stu-id="8e7c3-111">The register set is accessible through members in constant and texture buffers using HLSL semantics for things like component packing.</span></span>
<ul>
<li><span data-ttu-id="8e7c3-112">Registros del sombreador de píxeles (consulte <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">registros-ps_4_0</a> y <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">registros-ps_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="8e7c3-112">Pixel shader registers (see <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registers - ps_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">Registers - ps_4_1</a>)</span></span></li>
<li><span data-ttu-id="8e7c3-113">Registros del sombreador de vértices (consulte <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">registros-vs_4_0</a> y <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">registros-vs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="8e7c3-113">Vertex shader registers (see <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registers - vs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">Registers - vs_4_1</a>)</span></span></li>
<li><span data-ttu-id="8e7c3-114">Registros del sombreador de geometría (consulte <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">registros-gs_4_0</a> y <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">registros-gs_4_1</a>)</span><span class="sxs-lookup"><span data-stu-id="8e7c3-114">Geometry shader registers (see <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registers - gs_4_0</a> and <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">Registers - gs_4_1</a>)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e7c3-115">Sombreador de vértices máximo</span><span class="sxs-lookup"><span data-stu-id="8e7c3-115">Vertex Shader Max</span></span></td>
<td><span data-ttu-id="8e7c3-116">Sin restricción</span><span class="sxs-lookup"><span data-stu-id="8e7c3-116">No restriction</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e7c3-117">Sombreador de píxeles máximo</span><span class="sxs-lookup"><span data-stu-id="8e7c3-117">Pixel Shader Max</span></span></td>
<td><span data-ttu-id="8e7c3-118">Sin restricción</span><span class="sxs-lookup"><span data-stu-id="8e7c3-118">No restriction</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e7c3-119">Nuevos perfiles de sombreador agregados</span><span class="sxs-lookup"><span data-stu-id="8e7c3-119">New Shader Profiles Added</span></span></td>
<td><span data-ttu-id="8e7c3-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="8e7c3-120">gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1\*</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e7c3-121">Nuevo perfil de Effect-Framework agregado</span><span class="sxs-lookup"><span data-stu-id="8e7c3-121">New Effect-Framework Profile Added</span></span></td>
<td><span data-ttu-id="8e7c3-122">fx_4_0, fx_4_1 \*</span><span class="sxs-lookup"><span data-stu-id="8e7c3-122">fx_4_0, fx_4_1\*</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8e7c3-123">\* -GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1 y FX \_ 4 \_ 1 se admiten en Direct3D 10,1 o superior.</span><span class="sxs-lookup"><span data-stu-id="8e7c3-123">\* - gs\_4\_1, ps\_4\_1, vs\_4\_1 and fx\_4\_1 are supported on Direct3D 10.1 or higher.</span></span>

<span data-ttu-id="8e7c3-124">El modelo de sombreador 4 admite una nueva fase de canalización, la fase de sombreador de geometría, que se puede usar para crear o modificar la geometría existente.</span><span class="sxs-lookup"><span data-stu-id="8e7c3-124">Shader Model 4 supports a new pipeline stage—the geometry-shader stage—which can be used to create or modify existing geometry.</span></span> <span data-ttu-id="8e7c3-125">También incluye dos nuevos tipos de objeto: un objeto de salida de flujo diseñado para la transmisión de datos fuera de la fase de geometría y un objeto de textura con plantilla que implementa funciones de muestreo de textura.</span><span class="sxs-lookup"><span data-stu-id="8e7c3-125">It also includes two new object types: a stream-output object designed for streaming data out of the geometry stage, and a templated texture object that implements texture sampling functions.</span></span>

-   [<span data-ttu-id="8e7c3-126">Common-Shader Core</span><span class="sxs-lookup"><span data-stu-id="8e7c3-126">Common-Shader Core</span></span>](dx-graphics-hlsl-common-core.md)
-   [<span data-ttu-id="8e7c3-127">Constantes</span><span class="sxs-lookup"><span data-stu-id="8e7c3-127">Constants</span></span>](dx-graphics-hlsl-constants.md)
-   [<span data-ttu-id="8e7c3-128">Geometry: objeto de sombreador</span><span class="sxs-lookup"><span data-stu-id="8e7c3-128">Geometry-Shader Object</span></span>](dx-graphics-hlsl-geometry-shader.md)
-   [<span data-ttu-id="8e7c3-129">Stream: salida de objeto</span><span class="sxs-lookup"><span data-stu-id="8e7c3-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
-   [<span data-ttu-id="8e7c3-130">Objeto Texture</span><span class="sxs-lookup"><span data-stu-id="8e7c3-130">Texture Object</span></span>](dx-graphics-hlsl-to-type.md)

<span data-ttu-id="8e7c3-131">El modelo de sombreador 4 admite reglas de empaquetado que determinan la forma en que los datos se pueden organizar cuando se almacenan.</span><span class="sxs-lookup"><span data-stu-id="8e7c3-131">Shader Model 4 supports packing rules that dictate how tightly data can be arranged when it is stored.</span></span> <span data-ttu-id="8e7c3-132">Estas reglas se describen en [reglas de empaquetado para variables constantes](dx-graphics-hlsl-packing-rules.md)</span><span class="sxs-lookup"><span data-stu-id="8e7c3-132">These rules are described in [Packing Rules for Constant Variables](dx-graphics-hlsl-packing-rules.md)</span></span>

<span data-ttu-id="8e7c3-133">En la sección del [ensamblado modelo 4 del sombreador](dx-graphics-hlsl-sm4-asm.md) se describen las instrucciones de ensamblado que admiten el modelo de sombreador 4 y el modelo de sombreador 4,1.</span><span class="sxs-lookup"><span data-stu-id="8e7c3-133">The [Shader Model 4 Assembly](dx-graphics-hlsl-sm4-asm.md) section describes the assembly instructions that the Shader Model 4 and Shader Model 4.1 support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e7c3-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e7c3-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e7c3-135">Modelos de sombreador frente a perfiles de sombreador</span><span class="sxs-lookup"><span data-stu-id="8e7c3-135">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




