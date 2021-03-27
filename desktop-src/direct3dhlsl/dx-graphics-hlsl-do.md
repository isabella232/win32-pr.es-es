---
title: Instrucción do (Ocidl. h)
description: Ejecute una serie de instrucciones de forma continua hasta que se produzca un error en la expresión condicional.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- Instrucción do HLSL
topic_type:
- apiref
api_name:
- do Statement
api_location:
- ocidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46c0ced3c9747f0bfbdf01847b21350a45b68aa6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280309"
---
# <a name="do-statement"></a><span data-ttu-id="ee1df-104">Instrucción do</span><span class="sxs-lookup"><span data-stu-id="ee1df-104">do Statement</span></span>

<span data-ttu-id="ee1df-105">Ejecute una serie de instrucciones de forma continua hasta que se produzca un error en la expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="ee1df-105">Execute a series of statements continuously until the conditional expression fails.</span></span>



|                                                                     |
|---------------------------------------------------------------------|
| <span data-ttu-id="ee1df-106">\[*Atributo* \] de do { *bloque de instrucciones*;} while ( *condicional* );</span><span class="sxs-lookup"><span data-stu-id="ee1df-106">\[*Attribute*\] do {   *Statement Block*; } while( *Conditional* );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="ee1df-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee1df-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee1df-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atribui*</span><span class="sxs-lookup"><span data-stu-id="ee1df-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="ee1df-109">Parámetro opcional que controla cómo se compila la instrucción.</span><span class="sxs-lookup"><span data-stu-id="ee1df-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="ee1df-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="ee1df-110">Attribute</span></span> | <span data-ttu-id="ee1df-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee1df-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1df-112">fastopt</span><span class="sxs-lookup"><span data-stu-id="ee1df-112">fastopt</span></span>   | <span data-ttu-id="ee1df-113">Reduce el tiempo de compilación, pero produce optimizaciones menos agresivas.</span><span class="sxs-lookup"><span data-stu-id="ee1df-113">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="ee1df-114">Si utiliza este atributo, el compilador no deshará los bucles.</span><span class="sxs-lookup"><span data-stu-id="ee1df-114">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="ee1df-115">Este atributo solo afecta a los destinos del modelo de sombreador que admiten instrucciones de [interrupción](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="ee1df-115">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="ee1df-116">Este atributo está disponible en el modelo de sombreador [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) y en el [modelo de sombreador 3](dx-graphics-hlsl-sm3.md) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ee1df-116">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="ee1df-117">Es especialmente útil en el [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores cuando el compilador compila bucles.</span><span class="sxs-lookup"><span data-stu-id="ee1df-117">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="ee1df-118">El compilador simula los bucles de forma predeterminada para evaluar si puede deshacerlos.</span><span class="sxs-lookup"><span data-stu-id="ee1df-118">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="ee1df-119">Si no desea que el compilador deshaga los bucles, utilice este atributo para reducir el tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="ee1df-119">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ee1df-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*</span><span class="sxs-lookup"><span data-stu-id="ee1df-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="ee1df-121">Una o más [instrucciones](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="ee1df-121">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> <dt>

<span data-ttu-id="ee1df-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Instrucción*</span><span class="sxs-lookup"><span data-stu-id="ee1df-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="ee1df-123">[Expresión](dx-graphics-hlsl-expressions.md)condicional.</span><span class="sxs-lookup"><span data-stu-id="ee1df-123">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="ee1df-124">El bloque de instrucciones se ejecuta antes de que se evalúe la expresión.</span><span class="sxs-lookup"><span data-stu-id="ee1df-124">The statement block is executed before the expression is evaluated.</span></span> <span data-ttu-id="ee1df-125">El bucle se cierra cuando la expresión se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="ee1df-125">The loop is exited when the expression evaluates to false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee1df-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee1df-126">Requirements</span></span>



| <span data-ttu-id="ee1df-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee1df-127">Requirement</span></span> | <span data-ttu-id="ee1df-128">Value</span><span class="sxs-lookup"><span data-stu-id="ee1df-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ee1df-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee1df-129">Header</span></span><br/> | <dl> <span data-ttu-id="ee1df-130"><dt>Ocidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee1df-130"><dt>Ocidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee1df-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee1df-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee1df-132">Control de flujo</span><span class="sxs-lookup"><span data-stu-id="ee1df-132">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





