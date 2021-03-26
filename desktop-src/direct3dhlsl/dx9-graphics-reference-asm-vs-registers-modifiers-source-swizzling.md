---
title: Registro de origen permutación (HLSL VS Reference)
description: Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal. Permutación hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal. Permutación no afecta a los datos de registro de origen.
ms.assetid: 6271d846-c68d-467c-a110-be3279e0c11a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c075d8ff47b1f76adf378b6a583cd4d675651a87
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104420013"
---
# <a name="source-register-swizzling-hlsl-vs-reference"></a><span data-ttu-id="4f6ec-105">Registro de origen permutación (HLSL VS Reference)</span><span class="sxs-lookup"><span data-stu-id="4f6ec-105">Source Register Swizzling (HLSL VS reference)</span></span>

<span data-ttu-id="4f6ec-106">Antes de que se ejecute una instrucción, los datos de un registro de origen se copian en un registro temporal.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-106">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span> <span data-ttu-id="4f6ec-107">Permutación hace referencia a la capacidad de copiar cualquier componente de registro de origen en cualquier componente de registro temporal.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-107">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="4f6ec-108">Permutación no afecta a los datos de registro de origen.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-108">Swizzling does not affect the source register data.</span></span>

## <a name="component-swizzling"></a><span data-ttu-id="4f6ec-109">Componente permutación</span><span class="sxs-lookup"><span data-stu-id="4f6ec-109">Component Swizzling</span></span>

<span data-ttu-id="4f6ec-110">Como se muestra en la tabla siguiente, permutación se puede aplicar a los componentes individuales de los datos del registro de origen (donde es uno de los registros de entrada del sombreador de vértices válidos [, vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span><span class="sxs-lookup"><span data-stu-id="4f6ec-110">As shown in the following table, swizzling can be applied to the individual components of the source register data (where r is one of the valid vertex shader input [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md)).</span></span>



| <span data-ttu-id="4f6ec-111">Modificador de componente</span><span class="sxs-lookup"><span data-stu-id="4f6ec-111">Component modifier</span></span>                 | <span data-ttu-id="4f6ec-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f6ec-112">Description</span></span>    |
|------------------------------------|----------------|
| <span data-ttu-id="4f6ec-113">r. \[ xyzw \] \[ xyzw \] \[ xyzw \] \[ xyzw\]</span><span class="sxs-lookup"><span data-stu-id="4f6ec-113">r.\[xyzw\]\[xyzw\]\[xyzw\]\[xyzw\]</span></span> | <span data-ttu-id="4f6ec-114">Swizzle de origen</span><span class="sxs-lookup"><span data-stu-id="4f6ec-114">Source swizzle</span></span> |



 

-   <span data-ttu-id="4f6ec-115">Siempre se copian los cuatro componentes.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-115">All four components are always copied.</span></span> <span data-ttu-id="4f6ec-116">Si se especifican menos de cuatro componentes, el último componente se repite (XY Means. xyyy).</span><span class="sxs-lookup"><span data-stu-id="4f6ec-116">If fewer than four components are specified, the last component is repeated (xy means .xyyy).</span></span> <span data-ttu-id="4f6ec-117">Si no se especifica ningún componente, x se repite (. xxxx).</span><span class="sxs-lookup"><span data-stu-id="4f6ec-117">If no components are specified, x is repeated (.xxxx).</span></span>
-   <span data-ttu-id="4f6ec-118">Los componentes pueden aparecer en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-118">The components can appear in any order.</span></span> <span data-ttu-id="4f6ec-119">v0. YWX da como resultado v0. ywxx.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-119">v0.ywx results in v0.ywxx.</span></span>
-   <span data-ttu-id="4f6ec-120">Los componentes RGBA se pueden usar respectivamente para xyzw (r para x, g para b, etc.).</span><span class="sxs-lookup"><span data-stu-id="4f6ec-120">The rgba components can be used respectively for xyzw (r for x, g for b, etc.).</span></span>
-   <span data-ttu-id="4f6ec-121">Estas instrucciones implementan un componente de registro de origen único swizzles: EXP, EXPP, log, logP, pow, RCP, RSQ.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-121">These instructions implement source-register single component swizzles: exp, expp, log, logp, pow, rcp, rsq.</span></span> <span data-ttu-id="4f6ec-122">El resultado de estas instrucciones se copia en los cuatro componentes de registro de destino.</span><span class="sxs-lookup"><span data-stu-id="4f6ec-122">The result of these instructions is copied to all four destination register components.</span></span>

<span data-ttu-id="4f6ec-123">Permutación no se puede usar en las instrucciones [m3x2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [m4x3-vs](m4x3---vs.md)y [M4x4-vs](m4x4---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="4f6ec-123">Swizzling cannot be used on the [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m4x3 - vs](m4x3---vs.md), and [m4x4 - vs](m4x4---vs.md) instructions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f6ec-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f6ec-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f6ec-125">Modificadores de registro del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="4f6ec-125">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




