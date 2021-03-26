---
title: DEF-PS
description: Define las constantes de punto flotante del sombreador de píxeles.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b4f035df97de2645983862dd68aa7ec80fc22d4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078310"
---
# <a name="def---ps"></a><span data-ttu-id="78fa2-103">DEF-PS</span><span class="sxs-lookup"><span data-stu-id="78fa2-103">def - ps</span></span>

<span data-ttu-id="78fa2-104">Define las constantes de punto flotante del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="78fa2-104">Defines pixel shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="78fa2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78fa2-105">Syntax</span></span>



| <span data-ttu-id="78fa2-106">DEF DST, fVvalue1, fValue2, fValue3, fValue4</span><span class="sxs-lookup"><span data-stu-id="78fa2-106">def dst, fVvalue1, fValue2, fValue3, fValue4</span></span> |
|----------------------------------------------|



 

<span data-ttu-id="78fa2-107">Donde:</span><span class="sxs-lookup"><span data-stu-id="78fa2-107">Where:</span></span>

-   <span data-ttu-id="78fa2-108">DST es el registro de destino.</span><span class="sxs-lookup"><span data-stu-id="78fa2-108">dst is the destination register.</span></span>
-   <span data-ttu-id="78fa2-109">fValue1 to fValue4 son valores de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="78fa2-109">fValue1 to fValue4 are floating-point values..</span></span>

## <a name="remarks"></a><span data-ttu-id="78fa2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78fa2-110">Remarks</span></span>



| <span data-ttu-id="78fa2-111">Versiones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="78fa2-111">Pixel shader versions</span></span> | <span data-ttu-id="78fa2-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="78fa2-112">1\_1</span></span> | <span data-ttu-id="78fa2-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="78fa2-113">1\_2</span></span> | <span data-ttu-id="78fa2-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="78fa2-114">1\_3</span></span> | <span data-ttu-id="78fa2-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="78fa2-115">1\_4</span></span> | <span data-ttu-id="78fa2-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="78fa2-116">2\_0</span></span> | <span data-ttu-id="78fa2-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="78fa2-117">2\_x</span></span> | <span data-ttu-id="78fa2-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="78fa2-118">2\_sw</span></span> | <span data-ttu-id="78fa2-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="78fa2-119">3\_0</span></span> | <span data-ttu-id="78fa2-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="78fa2-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="78fa2-121">def</span><span class="sxs-lookup"><span data-stu-id="78fa2-121">def</span></span>                   | <span data-ttu-id="78fa2-122">x</span><span class="sxs-lookup"><span data-stu-id="78fa2-122">x</span></span>    | <span data-ttu-id="78fa2-123">x</span><span class="sxs-lookup"><span data-stu-id="78fa2-123">x</span></span>    | <span data-ttu-id="78fa2-124">x</span><span class="sxs-lookup"><span data-stu-id="78fa2-124">x</span></span>    | <span data-ttu-id="78fa2-125">x</span><span class="sxs-lookup"><span data-stu-id="78fa2-125">x</span></span>    | <span data-ttu-id="78fa2-126">x</span><span class="sxs-lookup"><span data-stu-id="78fa2-126">x</span></span>    | <span data-ttu-id="78fa2-127">x</span><span class="sxs-lookup"><span data-stu-id="78fa2-127">x</span></span>    | <span data-ttu-id="78fa2-128">x</span><span class="sxs-lookup"><span data-stu-id="78fa2-128">x</span></span>     | <span data-ttu-id="78fa2-129">x</span><span class="sxs-lookup"><span data-stu-id="78fa2-129">x</span></span>    | <span data-ttu-id="78fa2-130">x</span><span class="sxs-lookup"><span data-stu-id="78fa2-130">x</span></span>     |



 

<span data-ttu-id="78fa2-131">Hay dos maneras de establecer una constante de punto flotante en un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="78fa2-131">There are two ways to set a floating-point constant in a pixel shader.</span></span>

1.  <span data-ttu-id="78fa2-132">Use Def para definir la constante directamente dentro de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="78fa2-132">Use def to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="78fa2-133">Use la API para establecer una constante con [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span><span class="sxs-lookup"><span data-stu-id="78fa2-133">Use the API to set a constant with [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="78fa2-134">DEF define una constante de sombreador cuyo valor se carga cada vez que se establece un sombreador en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="78fa2-134">def defines a shader constant whose value is loaded any time a shader is set to a device.</span></span> <span data-ttu-id="78fa2-135">Se denominan constantes inmediatas.</span><span class="sxs-lookup"><span data-stu-id="78fa2-135">These are called immediate constants.</span></span> <span data-ttu-id="78fa2-136">Las constantes inmediatas tienen prioridad sobre las constantes establecidas por el método de la API.</span><span class="sxs-lookup"><span data-stu-id="78fa2-136">Immediate constants take precedence over constants set by the API method.</span></span>

-   <span data-ttu-id="78fa2-137">Debe aparecer antes de la primera instrucción aritmética o de direccionamiento en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="78fa2-137">Must appear before the first arithmetic or addressing instruction in shader.</span></span>
-   <span data-ttu-id="78fa2-138">Se puede combinar con las instrucciones [DCL-(SM2, SM3-PS ASM)](dcl---ps.md) (que son el otro tipo de instrucción que reside al principio de un sombreador).</span><span class="sxs-lookup"><span data-stu-id="78fa2-138">Can be intermixed with [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) instructions (which are the other type of instruction that resides at the beginning of a shader).</span></span>
-   <span data-ttu-id="78fa2-139">el registro de DST debe ser un [registro constante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="78fa2-139">dst register must be a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>
-   <span data-ttu-id="78fa2-140">La máscara de escritura debe estar llena (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="78fa2-140">Write mask must be full (default).</span></span>
-   <span data-ttu-id="78fa2-141">Si un [registro constante](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) se define varias veces en un sombreador, el último persiste.</span><span class="sxs-lookup"><span data-stu-id="78fa2-141">If a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) is defined multiple times in a shader, the last one persists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78fa2-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78fa2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78fa2-143">Instrucciones del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="78fa2-143">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 