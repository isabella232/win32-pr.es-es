---
title: for (Instrucción)
description: Ejecuta de forma iterativa una serie de instrucciones, en función de la evaluación de la expresión condicional.
ms.assetid: d795c89e-7088-4bf3-93a8-798ed9c1a353
keywords:
- for Statement HLSL
topic_type:
- apiref
api_name:
- for Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cbcf06f28a327e18aa9f31b417dc1911411d0c9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119081"
---
# <a name="for-statement"></a><span data-ttu-id="b7ef8-104">for (Instrucción)</span><span class="sxs-lookup"><span data-stu-id="b7ef8-104">for Statement</span></span>

<span data-ttu-id="b7ef8-105">Ejecuta de forma iterativa una serie de instrucciones, en función de la evaluación de la expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-105">Iteratively executes a series of statements, based on the evaluation of the conditional expression.</span></span>

<span data-ttu-id="b7ef8-106">\[*Atributo* \] for ( *Initializer; Condicional; Iterator* ) { *Bloque de instrucciones*; }</span><span class="sxs-lookup"><span data-stu-id="b7ef8-106">\[*Attribute*\] for ( *Initializer; Conditional; Iterator* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="b7ef8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7ef8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7ef8-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*</span><span class="sxs-lookup"><span data-stu-id="b7ef8-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="b7ef8-109">Parámetro opcional que controla cómo se compila la instrucción.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="b7ef8-110">Cuando no se especifica ningún atributo, el compilador intentará primero emitir una versión revertida del bucle y, si se produce un error, o si algunas operaciones serían más fáciles si el bucle se anuló, revertirá a una versión no inscrita del bucle.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-110">When no attribute is specified the compiler will first attempt to emit a rolled version of the loop, and if that fails, or if some operations would be easier if the loop was unrolled, will fall back to an unrolled version of the loop.</span></span>



| <span data-ttu-id="b7ef8-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="b7ef8-111">Attribute</span></span>             | <span data-ttu-id="b7ef8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b7ef8-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ef8-113">unroll(x)</span><span class="sxs-lookup"><span data-stu-id="b7ef8-113">unroll(x)</span></span>             | <span data-ttu-id="b7ef8-114">Desenrolle el bucle hasta que deje de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-114">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="b7ef8-115">Opcionalmente, puede especificar el número máximo de veces que se va a ejecutar el bucle.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-115">Can optionally specify the maximum number of times the loop is to execute.</span></span> <span data-ttu-id="b7ef8-116">No es compatible con el **\[ atributo de \]** bucle.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-116">Not compatible with the **\[loop\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b7ef8-117">bucle</span><span class="sxs-lookup"><span data-stu-id="b7ef8-117">loop</span></span>                  | <span data-ttu-id="b7ef8-118">Genere código que use el control de flujo para ejecutar cada iteración del bucle.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-118">Generate code that uses flow control to execute each iteration of the loop.</span></span> <span data-ttu-id="b7ef8-119">No es compatible con el **\[ atributo unroll. \]**</span><span class="sxs-lookup"><span data-stu-id="b7ef8-119">Not compatible with the **\[unroll\]** attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b7ef8-120">fastopt</span><span class="sxs-lookup"><span data-stu-id="b7ef8-120">fastopt</span></span>               | <span data-ttu-id="b7ef8-121">Reduce el tiempo de compilación, pero genera optimizaciones menos agresivas.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-121">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="b7ef8-122">Si usa este atributo, el compilador no desenrollará bucles.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-122">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="b7ef8-123">Este atributo solo afecta a los destinos del modelo de sombreador que admiten [instrucciones de](dx-graphics-hlsl-break.md) interrupción.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-123">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="b7ef8-124">Este atributo está disponible en el modelo de sombreador [frente \_ a 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) y en el modelo [de sombreador 3](dx-graphics-hlsl-sm3.md) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-124">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="b7ef8-125">Es especialmente útil en el modelo [de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores cuando el compilador compila bucles.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-125">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="b7ef8-126">El compilador simula bucles de forma predeterminada para evaluar si puede deshacer su inscripción.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-126">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="b7ef8-127">Si no desea que el compilador desrolle bucles, use este atributo para reducir el tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-127">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span> <br/> |
| <span data-ttu-id="b7ef8-128">permitir \_ condición \_ uav</span><span class="sxs-lookup"><span data-stu-id="b7ef8-128">allow\_uav\_condition</span></span> | <span data-ttu-id="b7ef8-129">Permite que una condición de terminación del bucle de sombreador de proceso se base en una lectura UAV.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-129">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="b7ef8-130">El bucle no debe contener intrínsecos de sincronización.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-130">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="b7ef8-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Inicializador*</span><span class="sxs-lookup"><span data-stu-id="b7ef8-131"><span id="Initializer"></span><span id="initializer"></span><span id="INITIALIZER"></span>*Initializer*</span></span>
</dt> <dd>

<span data-ttu-id="b7ef8-132">Valor inicial del contador de bucles.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-132">The initial value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef8-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*</span><span class="sxs-lookup"><span data-stu-id="b7ef8-133"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="b7ef8-134">Expresión [condicional](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="b7ef8-134">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="b7ef8-135">Si la expresión condicional se evalúa como true, se ejecuta el bloque de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-135">If the conditional expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="b7ef8-136">El bucle finaliza cuando la expresión se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-136">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef8-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterador*</span><span class="sxs-lookup"><span data-stu-id="b7ef8-137"><span id="Iterator"></span><span id="iterator"></span><span id="ITERATOR"></span>*Iterator*</span></span>
</dt> <dd>

<span data-ttu-id="b7ef8-138">Actualice el valor del contador de bucles.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-138">Update the value of the loop counter.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef8-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*</span><span class="sxs-lookup"><span data-stu-id="b7ef8-139"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="b7ef8-140">Una o varias [instrucciones HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="b7ef8-140">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b7ef8-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7ef8-141">Remarks</span></span>

<span data-ttu-id="b7ef8-142">Los **\[ atributos \] de la inscripción** y del **\[ bucle \]** son mutuamente excluyentes y generarán errores del compilador cuando se especifiquen ambos.</span><span class="sxs-lookup"><span data-stu-id="b7ef8-142">The **\[unroll\]** and **\[loop\]** attributes are mutually exclusive and will generate compiler errors when both are specified.</span></span>

<span data-ttu-id="b7ef8-143">Los **\[ atributos \] de condición fastopt** y **\[ allow \_ uav \_ \]** se omiten si **\[ se especifica unroll. \]**</span><span class="sxs-lookup"><span data-stu-id="b7ef8-143">The **\[fastopt\]** and **\[allow\_uav\_condition\]** attributes are ignored if **\[unroll\]** is specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7ef8-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b7ef8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ef8-145">Control de flujo</span><span class="sxs-lookup"><span data-stu-id="b7ef8-145">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





