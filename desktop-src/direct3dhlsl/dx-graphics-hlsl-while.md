---
title: while (Instrucción)
description: Ejecuta un bloque de instrucciones hasta que se produce un error en la expresión condicional.
ms.assetid: 0fe420db-3c09-40bd-b689-f85c02e2f817
keywords:
- while (Instrucción HLSL)
topic_type:
- apiref
api_name:
- while Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bf1f0049ac474e7840753a8cfe05c972aa346c1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826678"
---
# <a name="while-statement"></a><span data-ttu-id="de583-104">while (Instrucción)</span><span class="sxs-lookup"><span data-stu-id="de583-104">while Statement</span></span>

<span data-ttu-id="de583-105">Ejecuta un bloque de instrucciones hasta que se produce un error en la expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="de583-105">Executes a statement block until the conditional expression fails.</span></span>

<span data-ttu-id="de583-106">\[*Atributo* \] while ( *Conditional* ) { *Statement Block*; }</span><span class="sxs-lookup"><span data-stu-id="de583-106">\[*Attribute*\] while ( *Conditional* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="de583-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de583-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de583-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*</span><span class="sxs-lookup"><span data-stu-id="de583-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="de583-109">Parámetro opcional que controla cómo se compila la instrucción.</span><span class="sxs-lookup"><span data-stu-id="de583-109">An optional parameter that controls how the statement is compiled.</span></span>



| <span data-ttu-id="de583-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="de583-110">Attribute</span></span>             | <span data-ttu-id="de583-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="de583-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de583-112">unroll(x)</span><span class="sxs-lookup"><span data-stu-id="de583-112">unroll(x)</span></span>             | <span data-ttu-id="de583-113">Desenrolle el bucle hasta que deje de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="de583-113">Unroll the loop until it stops executing.</span></span> <span data-ttu-id="de583-114">Opcionalmente, puede especificar el número máximo de veces que se puede ejecutar el bucle.</span><span class="sxs-lookup"><span data-stu-id="de583-114">Optionally, you can specify the maximum number of times the loop can execute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="de583-115">bucle</span><span class="sxs-lookup"><span data-stu-id="de583-115">loop</span></span>                  | <span data-ttu-id="de583-116">Use instrucciones de control de flujo en el sombreador compilado; no desenrolle el bucle.</span><span class="sxs-lookup"><span data-stu-id="de583-116">Use flow-control statements in the compiled shader; do not unroll the loop.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="de583-117">fastopt</span><span class="sxs-lookup"><span data-stu-id="de583-117">fastopt</span></span>               | <span data-ttu-id="de583-118">Reduce el tiempo de compilación, pero genera optimizaciones menos agresivas.</span><span class="sxs-lookup"><span data-stu-id="de583-118">Reduces the compile time but produces less aggressive optimizations.</span></span> <span data-ttu-id="de583-119">Si usa este atributo, el compilador no desenrollará bucles.</span><span class="sxs-lookup"><span data-stu-id="de583-119">If you use this attribute, the compiler will not unroll loops.</span></span><br/> <span data-ttu-id="de583-120">Este atributo solo afecta a los destinos del modelo de sombreador que admiten [instrucciones de](dx-graphics-hlsl-break.md) interrupción.</span><span class="sxs-lookup"><span data-stu-id="de583-120">This attribute affects only shader model targets that support [break](dx-graphics-hlsl-break.md) instructions.</span></span> <span data-ttu-id="de583-121">Este atributo está disponible en el modelo de sombreador [frente \_ a 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md) y en el modelo [de sombreador 3](dx-graphics-hlsl-sm3.md) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="de583-121">This attribute is available in shader model [vs\_2\_x](dx9-graphics-reference-asm-vs-2-x.md) and [shader model 3](dx-graphics-hlsl-sm3.md) and later.</span></span> <span data-ttu-id="de583-122">Resulta especialmente útil en el modelo [de sombreador 4](dx-graphics-hlsl-sm4.md) y versiones posteriores cuando el compilador compila bucles.</span><span class="sxs-lookup"><span data-stu-id="de583-122">It is particularly useful in [shader model 4](dx-graphics-hlsl-sm4.md) and later when the compiler compiles loops.</span></span> <span data-ttu-id="de583-123">El compilador simula bucles de forma predeterminada para evaluar si puede deshacer su inscripción.</span><span class="sxs-lookup"><span data-stu-id="de583-123">The compiler simulates loops by default to evaluate whether it can unroll them.</span></span> <span data-ttu-id="de583-124">Si no desea que el compilador desenrolle bucles, use este atributo para reducir el tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="de583-124">If you do not want the compiler to unroll loops, use this attribute to reduce compile time.</span></span><br/> |
| <span data-ttu-id="de583-125">permitir \_ condición \_ uav</span><span class="sxs-lookup"><span data-stu-id="de583-125">allow\_uav\_condition</span></span> | <span data-ttu-id="de583-126">Permite que una condición de terminación de bucle de sombreador de proceso se base en una lectura UAV.</span><span class="sxs-lookup"><span data-stu-id="de583-126">Allows a compute shader loop termination condition to be based off of a UAV read.</span></span> <span data-ttu-id="de583-127">El bucle no debe contener intrínsecos de sincronización.</span><span class="sxs-lookup"><span data-stu-id="de583-127">The loop must not contain synchronization intrinsics.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="de583-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*</span><span class="sxs-lookup"><span data-stu-id="de583-128"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="de583-129">Expresión [condicional](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="de583-129">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="de583-130">Si la expresión se evalúa como true, se ejecuta el bloque de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="de583-130">If the expression evaluates to true, the statement block is executed.</span></span> <span data-ttu-id="de583-131">El bucle finaliza cuando la expresión se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="de583-131">The loop ends when the expression evaluates to false.</span></span>

</dd> <dt>

<span data-ttu-id="de583-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*</span><span class="sxs-lookup"><span data-stu-id="de583-132"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="de583-133">Una o varias [instrucciones](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="de583-133">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="de583-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="de583-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de583-135">Control de flujo</span><span class="sxs-lookup"><span data-stu-id="de583-135">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





