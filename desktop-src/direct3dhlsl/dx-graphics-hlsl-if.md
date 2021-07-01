---
title: if (Instrucción)
description: Ejecute condicionalmente una serie de instrucciones, en función de la evaluación de la expresión condicional.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- if (Instrucción HLSL)
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4a1f049526422f39c3529395481548943c7e84
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118960"
---
# <a name="if-statement"></a><span data-ttu-id="6b784-104">if (Instrucción)</span><span class="sxs-lookup"><span data-stu-id="6b784-104">if Statement</span></span>

<span data-ttu-id="6b784-105">Ejecute condicionalmente una serie de instrucciones, en función de la evaluación de la expresión condicional.</span><span class="sxs-lookup"><span data-stu-id="6b784-105">Conditionally execute a series of statements, based on the evaluation of the conditional expression.</span></span>

<span data-ttu-id="6b784-106">\[*Atributo* \] if ( *Conditional* ) { *Statement Block*; }</span><span class="sxs-lookup"><span data-stu-id="6b784-106">\[*Attribute*\] if ( *Conditional* ) {   *Statement Block*; }</span></span>



 

## <a name="parameters"></a><span data-ttu-id="6b784-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b784-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b784-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*</span><span class="sxs-lookup"><span data-stu-id="6b784-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="6b784-109">Parámetro opcional que controla cómo se compila la instrucción.</span><span class="sxs-lookup"><span data-stu-id="6b784-109">An optional parameter that controls how the statement is compiled.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b784-110">Atributo</span><span class="sxs-lookup"><span data-stu-id="6b784-110">Attribute</span></span></th>
<th><span data-ttu-id="6b784-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b784-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b784-112">branch</span><span class="sxs-lookup"><span data-stu-id="6b784-112">branch</span></span></td>
<td><span data-ttu-id="6b784-113">Evalúe solo un lado de la instrucción if en función de la condición dada.</span><span class="sxs-lookup"><span data-stu-id="6b784-113">Evaluate only one side of the if statement depending on the given condition.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="6b784-114">Cuando se usa <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> o <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0,</a>cada vez que se usa la bifurcación dinámica se consumen recursos.</span><span class="sxs-lookup"><span data-stu-id="6b784-114">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="6b784-115">Por lo tanto, si usa la bifurcación dinámica excesivamente cuando tiene como destino estos perfiles, puede recibir errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="6b784-115">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b784-116">quitar información de estructura jerárquica</span><span class="sxs-lookup"><span data-stu-id="6b784-116">flatten</span></span></td>
<td><span data-ttu-id="6b784-117">Evalúe ambos lados de la instrucción if y elija entre los dos valores resultantes.</span><span class="sxs-lookup"><span data-stu-id="6b784-117">Evaluate both sides of the if statement and choose between the two resulting values.</span></span></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="6b784-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condicional*</span><span class="sxs-lookup"><span data-stu-id="6b784-118"><span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Conditional*</span></span>
</dt> <dd>

<span data-ttu-id="6b784-119">Expresión [condicional](dx-graphics-hlsl-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="6b784-119">A conditional [expression](dx-graphics-hlsl-expressions.md).</span></span> <span data-ttu-id="6b784-120">Se evalúa la expresión y, si es true, se ejecuta el bloque de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="6b784-120">The expression is evaluated, and if true, the statement block is executed.</span></span>

</dd> <dt>

<span data-ttu-id="6b784-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Bloque de instrucciones*</span><span class="sxs-lookup"><span data-stu-id="6b784-121"><span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Statement Block*</span></span>
</dt> <dd>

<span data-ttu-id="6b784-122">Una o varias [instrucciones HLSL](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="6b784-122">One or more [HLSL statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b784-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b784-123">Remarks</span></span>

<span data-ttu-id="6b784-124">Cuando el compilador usa el método de rama para compilar una instrucción if, generará código que evaluará solo un lado de la instrucción if en función de la condición dada.</span><span class="sxs-lookup"><span data-stu-id="6b784-124">When the compiler uses the branch method for compiling an if statement it will generate code that will evaluate only one side of the if statement depending on the given condition.</span></span> <span data-ttu-id="6b784-125">Por ejemplo, en la instrucción if:</span><span class="sxs-lookup"><span data-stu-id="6b784-125">For example, in the if statement:</span></span>


```
[branch] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="6b784-126">La **instrucción if** tiene un bloque else implícito, que es equivalente a x = x.</span><span class="sxs-lookup"><span data-stu-id="6b784-126">The **if** statement has an implicit else block, which is equivalent to x = x.</span></span> <span data-ttu-id="6b784-127">Dado que hemos indicado al compilador que use el método de rama con el atributo de rama anterior, el código compilado evaluará x y ejecutará solo el lado que se debe ejecutar; si x es cero, ejecutará  el otro lado y, si es distinto de cero, ejecutará el **lado** siguiente.</span><span class="sxs-lookup"><span data-stu-id="6b784-127">Because we have told the compiler to use the branch method with the preceding branch attribute, the compiled code will evaluate x and execute only the side that should be executed; if x is zero, then it will execute the **else** side, and if it is non-zero it will execute the **then** side.</span></span>

<span data-ttu-id="6b784-128">Por el contrario, si se usa el atributo **flatten,** el código compilado evaluará ambos lados de la **instrucción if** y elegirá entre los dos valores resultantes con el valor original de x.</span><span class="sxs-lookup"><span data-stu-id="6b784-128">Conversely, if the **flatten** attribute is used, then the compiled code will evaluate both sides of the **if** statement and choose between the two resulting values using the original value of x.</span></span> <span data-ttu-id="6b784-129">Este es un ejemplo de un uso del atributo flatten:</span><span class="sxs-lookup"><span data-stu-id="6b784-129">Here is an example of a usage of the flatten attribute:</span></span>


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



<span data-ttu-id="6b784-130">Hay ciertos casos en los que el uso de la rama o los atributos planos puede generar un error de compilación.</span><span class="sxs-lookup"><span data-stu-id="6b784-130">There are certain cases where using the branch or flatten attributes may generate a compile error.</span></span> <span data-ttu-id="6b784-131">El atributo de rama puede producir un error si cualquiera de los lados de la instrucción if contiene una función de degradado, como [**texas2D.**](dx-graphics-hlsl-tex2d.md)</span><span class="sxs-lookup"><span data-stu-id="6b784-131">The branch attribute may fail if either side of the if statement contains a gradient function, such as [**tex2D**](dx-graphics-hlsl-tex2d.md).</span></span> <span data-ttu-id="6b784-132">El atributo flatten puede producir un error si cualquiera de los lados de la instrucción if contiene una instrucción stream append o cualquier otra instrucción que tenga efectos secundarios.</span><span class="sxs-lookup"><span data-stu-id="6b784-132">The flatten attribute may fail if either side of the if statement contains a stream append statement or any other statement that has side-effects.</span></span>

<span data-ttu-id="6b784-133">Una **instrucción if** también puede usar un bloque else opcional.</span><span class="sxs-lookup"><span data-stu-id="6b784-133">An **if** statement can also use an optional else block.</span></span> <span data-ttu-id="6b784-134">Si la **expresión if** es true, se procesa el código del bloque de instrucciones asociado a la instrucción if.</span><span class="sxs-lookup"><span data-stu-id="6b784-134">If the **if** expression is true, the code in the statement block associated with the if statement is processed.</span></span> <span data-ttu-id="6b784-135">De lo contrario, se procesa el bloque de instrucciones asociado al bloque else opcional.</span><span class="sxs-lookup"><span data-stu-id="6b784-135">Otherwise, the statement block associated with the optional else block is processed.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b784-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6b784-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b784-137">Control de flujo</span><span class="sxs-lookup"><span data-stu-id="6b784-137">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 





