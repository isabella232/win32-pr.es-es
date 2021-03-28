---
title: for (Instrucción)
description: Ejecuta una serie de instrucciones de forma iterativa, en función de la evaluación de la expresión condicional.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- for (instrucción HLSL)
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50f8c18ebc23455563b4b3e6bfee72bfa9d3ec4c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148897"
---
# <a name="for-statement"></a><span data-ttu-id="11109-104">for (Instrucción)</span><span class="sxs-lookup"><span data-stu-id="11109-104">for Statement</span></span>

<span data-ttu-id="11109-105">Ejecuta una serie de instrucciones de forma iterativa, en función de la evaluación de la expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="11109-105">Iteratively executes a series of statements, based on the evaluation of the conditional expression.</span></span>



|                                                                                       |
|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11109-106">\[*Atributo* \] de para ( *inicializador; Instrucción Iterator* ) { *bloque de instrucciones*;}</span><span class="sxs-lookup"><span data-stu-id="11109-106">\[*Attribute*\] for ( *Initializer; Conditional; Iterator* ) {   *Statement Block*; }</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="11109-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11109-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11109-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atribui*</span><span class="sxs-lookup"><span data-stu-id="11109-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="11109-109">Parámetro opcional que controla cómo se compila la instrucción.</span><span class="sxs-lookup"><span data-stu-id="11109-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="11109-110">Cuando no se especifica ningún atributo, el compilador intentará primero emitir una versión revertida del bucle y, en caso de que se produzca un error, o si algunas operaciones serían más fáciles si el bucle se hubiera inscrito, revertiría a una versión no repuesta del bucle.</span><span class="sxs-lookup"><span data-stu-id="11109-110">When no attribute is specified the compiler will first attempt to emit a rolled version of the loop, and if that fails, or if some operations would be easier if the loop was unrolled, will fall back to an unrolled version of the loop.</span></span>



| <span data-ttu-id="11109-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="11109-111">Attribute</span></span>             | <span data-ttu-id="11109-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="11109-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11109-113">deshacer (x)</span><span class="sxs-lookup"><span data-stu-id="11109-113">unroll(x)</span></span>             | <span data-ttu-id="11109-114">Desponga el bucle hasta que deje de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="11109-114">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="11109-115">Opcionalmente, puede especificar el número máximo de veces que se va a ejecutar el bucle.</span><span class="sxs-lookup"><span data-stu-id="11109-115">Can optionally specify the maximum number of times the loop is to execute.</span></span> <span data-ttu-id="11109-116">No es compatible con el atributo de **\[ bucle \]** .</span><span class="sxs-lookup"><span data-stu-id="11109-116">Not compatible with the **\[loop\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="11109-117">bucle</span><span class="sxs-lookup"><span data-stu-id="11109-117">loop</span></span>                  | <span data-ttu-id="11109-118">Generar código que usa el control de flujo para ejecutar cada iteración del bucle.</span><span class="sxs-lookup"><span data-stu-id="11109-118">Generate code that uses flow control to execute each iteration of the loop.</span></span> <span data-ttu-id="11109-119">No es compatible con el atributo **\[ unroll \]** .</span><span class="sxs-lookup"><span data-stu-id="11109-119">Not compatible with the **\[unroll\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="11109-120">fastopt</span><span class="sxs-lookup"><span data-stu-id="11109-120">fastopt</span></span>               | <span data-ttu-id="11109-121">Reduce el tiempo de compilación, pero produce optimizaciones menos agresivas.</span><span class="sxs-lookup"><span data-stu-id="11109-121">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="11109-122">Si utiliza este atributo, el compilador no deshará los bucles.</span><span class="sxs-lookup"><span data-stu-id="11109-122">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="11109-123">Este atributo solo afecta a los destinos del modelo de sombreador que admiten instrucciones de [interrupción](dx-graphics-hlsl-break.md) .</span><span class="sxs-lookup"><span data-stu-id="11109-123">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="11109-124">Este atributo está disponible en el modelo de sombreador [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) y en el [modelo de sombreador 3](dx-graphics-hlsl-sm3.md) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="11109-124">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="11109-125">Es especialmente útil en el [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores cuando el compilador compila bucles.</span><span class="sxs-lookup"><span data-stu-id="11109-125">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="11109-126">El compilador simula los bucles de forma predeterminada para evaluar si puede deshacerlos.</span><span class="sxs-lookup"><span data-stu-id="11109-126">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="11109-127">Si no desea que el compilador deshaga los bucles, utilice este atributo para reducir el tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="11109-127">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span> <br/> |
| <span data-ttu-id="11109-128">permitir \_ \_ condición UAV</span><span class="sxs-lookup"><span data-stu-id="11109-128">allow\_uav\_condition</span></span> | <span data-ttu-id="11109-129">Permite que una condición de finalización del bucle del sombreador de cálculo se base en una lectura UAV.</span><span class="sxs-lookup"><span data-stu-id="11109-129">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="11109-130">El bucle no debe contener intrínsecos de sincronización.</span><span class="sxs-lookup"><span data-stu-id="11109-130">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="11109-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inicializador*</span><span class="sxs-lookup"><span data-stu-id="11109-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span></span>
</dt> <dd>

<span data-ttu-id="11109-132">Valor inicial del contador de bucles.</span><span class="sxs-lookup"><span data-stu-id="11109-132">The initial value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="11109-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Instrucción*</span><span class="sxs-lookup"><span data-stu-id="11109-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="11109-134">[Expresión](dx-graphics-hlsl-expressions.md)condicional.</span><span class="sxs-lookup"><span data-stu-id="11109-134">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="11109-135">Si la expresión condicional se evalúa como true, se ejecuta el bloque de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="11109-135">If the conditional expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="11109-136">El bucle finaliza cuando la expresión se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="11109-136">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="11109-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Apunta*</span><span class="sxs-lookup"><span data-stu-id="11109-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span></span>
</dt> <dd>

<span data-ttu-id="11109-138">Actualice el valor del contador de bucle.</span><span class="sxs-lookup"><span data-stu-id="11109-138">Update the value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="11109-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*</span><span class="sxs-lookup"><span data-stu-id="11109-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="11109-140">Una o varias [instrucciones de HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="11109-140">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11109-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11109-141">Remarks</span></span>

<span data-ttu-id="11109-142">Los atributos **\[ unroll \]** y **\[ Loop \]** se excluyen mutuamente y generarán errores del compilador cuando se especifiquen ambos.</span><span class="sxs-lookup"><span data-stu-id="11109-142">The **\[unroll\]** and **\[loop\]** attributes are mutually exclusive and will generate compiler errors when both are specified.</span></span>

<span data-ttu-id="11109-143">Los atributos **\[ fastopt \]** y **\[ Allow \_ UAV \_ Condition \]** se omiten si se especifica **\[ unroll \]** .</span><span class="sxs-lookup"><span data-stu-id="11109-143">The **\[fastopt\]** and **\[allow\_uav\_condition\]** attributes are ignored if **\[unroll\]** is specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="11109-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="11109-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11109-145">Control de flujo</span><span class="sxs-lookup"><span data-stu-id="11109-145">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





