---
title: do (Instrucción, Ocidl.h)
description: Ejecute una serie de instrucciones continuamente hasta que se produce un error en la expresión condicional.
ms.assetid: 07fd37b0-59c2-404b-a755-7178e4a058e4
keywords:
- do (Instrucción HLSL)
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
ms.openlocfilehash: a1f019af77ef0021ad0574bf703ff2a2a52ac0f6
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118790"
---
# <a name="do-statement"></a><span data-ttu-id="bcf45-104">do (Instrucción)</span><span class="sxs-lookup"><span data-stu-id="bcf45-104">do Statement</span></span>

<span data-ttu-id="bcf45-105">Ejecute una serie de instrucciones continuamente hasta que se produce un error en la expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="bcf45-105">Execute a series of statements continuously until the conditional expression fails.</span></span>

<span data-ttu-id="bcf45-106">\[*Atributo* \] do { *Statement Block*; } while( *Conditional* );</span><span class="sxs-lookup"><span data-stu-id="bcf45-106">\[*Attribute*\] do {   *Statement Block*; } while( *Conditional* );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="bcf45-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcf45-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf45-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*</span><span class="sxs-lookup"><span data-stu-id="bcf45-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="bcf45-109">Parámetro opcional que controla cómo se compila la instrucción.</span><span class="sxs-lookup"><span data-stu-id="bcf45-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="bcf45-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="bcf45-110">Attribute</span></span> | <span data-ttu-id="bcf45-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcf45-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf45-112">fastopt</span><span class="sxs-lookup"><span data-stu-id="bcf45-112">fastopt</span></span>   | <span data-ttu-id="bcf45-113">Reduce el tiempo de compilación, pero genera optimizaciones menos agresivas.</span><span class="sxs-lookup"><span data-stu-id="bcf45-113">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="bcf45-114">Si usa este atributo, el compilador no desenrollará bucles.</span><span class="sxs-lookup"><span data-stu-id="bcf45-114">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="bcf45-115">Este atributo solo afecta a los destinos del modelo de sombreador que admiten [instrucciones de](dx-graphics-hlsl-break.md) interrupción.</span><span class="sxs-lookup"><span data-stu-id="bcf45-115">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="bcf45-116">Este atributo está disponible en el modelo de sombreador [frente \_ a 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) y en el modelo [de sombreador 3](dx-graphics-hlsl-sm3.md) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bcf45-116">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="bcf45-117">Es especialmente útil en el modelo [de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores cuando el compilador compila bucles.</span><span class="sxs-lookup"><span data-stu-id="bcf45-117">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="bcf45-118">El compilador simula bucles de forma predeterminada para evaluar si puede deshacer su inscripción.</span><span class="sxs-lookup"><span data-stu-id="bcf45-118">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="bcf45-119">Si no desea que el compilador desrolle bucles, use este atributo para reducir el tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="bcf45-119">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bcf45-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*</span><span class="sxs-lookup"><span data-stu-id="bcf45-120"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="bcf45-121">Una o varias [instrucciones](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="bcf45-121">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> <dt>

<span data-ttu-id="bcf45-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*</span><span class="sxs-lookup"><span data-stu-id="bcf45-122"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="bcf45-123">Expresión [condicional](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="bcf45-123">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="bcf45-124">El bloque de instrucciones se ejecuta antes de evaluar la expresión.</span><span class="sxs-lookup"><span data-stu-id="bcf45-124">The statement block is executed before the expression is evaluated.</span></span> <span data-ttu-id="bcf45-125">El bucle se cierra cuando la expresión se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="bcf45-125">The loop is exited when the expression evaluates to false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcf45-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcf45-126">Requirements</span></span>



| <span data-ttu-id="bcf45-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcf45-127">Requirement</span></span> | <span data-ttu-id="bcf45-128">Value</span><span class="sxs-lookup"><span data-stu-id="bcf45-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf45-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcf45-129">Header</span></span><br/> | <dl> <span data-ttu-id="bcf45-130"><dt>Ocidl.h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf45-130"><dt>Ocidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf45-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bcf45-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf45-132">Control de flujo</span><span class="sxs-lookup"><span data-stu-id="bcf45-132">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





