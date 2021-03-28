---
title: Switch (instrucción) (urlmon. h)
description: Transfiere el control a un bloque de instrucciones diferente en el cuerpo del modificador en función del valor de un selector.
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- Instrucción switch HLSL
topic_type:
- apiref
api_name:
- switch Statement
api_location:
- urlmon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c65049acce4265dd2abdf849119aad5902db9e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103820919"
---
# <a name="switch-statement"></a><span data-ttu-id="50cc6-104">switch (Instrucción)</span><span class="sxs-lookup"><span data-stu-id="50cc6-104">switch Statement</span></span>

<span data-ttu-id="50cc6-105">Transfiere el control a un bloque de instrucciones diferente en el cuerpo del modificador en función del valor de un selector.</span><span class="sxs-lookup"><span data-stu-id="50cc6-105">Transfer control to a different statement block within the switch body depending on the value of a selector.</span></span>



|                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50cc6-106">\[*Atributo* \] de Switch ( *selector* ) {Case 0: { *StatementBlock*;}   eliminar   caso 1: { *StatementBlock*;}   eliminar   Case n: { *StatementBlock*;}   eliminar   valor predeterminado: { *StatementBlock*;}   eliminar</span><span class="sxs-lookup"><span data-stu-id="50cc6-106">\[*Attribute*\] switch( *Selector* ) {   case 0 :     { *StatementBlock*; }   break;   case 1 :     { *StatementBlock*; }   break;   case n :     { *StatementBlock*; }   break;   default :     { *StatementBlock*; }   break;</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="50cc6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50cc6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50cc6-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atribui*</span><span class="sxs-lookup"><span data-stu-id="50cc6-108"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attribute*</span></span>
</dt> <dd>

<span data-ttu-id="50cc6-109">Parámetro opcional que controla cómo se compila la instrucción.</span><span class="sxs-lookup"><span data-stu-id="50cc6-109">An optional parameter that controls how the statement is compiled.</span></span> <span data-ttu-id="50cc6-110">Cuando no se especifica ningún atributo, el compilador puede usar un modificador de hardware o emitir una serie de instrucciones **If** .</span><span class="sxs-lookup"><span data-stu-id="50cc6-110">When no attribute is specified, the compiler may use a hardware switch or emit a series of **if** statements.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50cc6-111">Atributo</span><span class="sxs-lookup"><span data-stu-id="50cc6-111">Attribute</span></span></th>
<th><span data-ttu-id="50cc6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="50cc6-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="50cc6-113">quitar información de estructura jerárquica</span><span class="sxs-lookup"><span data-stu-id="50cc6-113">flatten</span></span></td>
<td><span data-ttu-id="50cc6-114">Compile la instrucción como una serie de instrucciones <strong>If</strong> , cada una con el atributo <strong>Flatten</strong> .</span><span class="sxs-lookup"><span data-stu-id="50cc6-114">Compile the statement as a series of <strong>if</strong> statements, each with the <strong>flatten</strong> attribute.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50cc6-115">branch</span><span class="sxs-lookup"><span data-stu-id="50cc6-115">branch</span></span></td>
<td><span data-ttu-id="50cc6-116">Compile la instrucción como una serie de instrucciones <strong>If</strong> cada una con el atributo <strong>Branch</strong> .</span><span class="sxs-lookup"><span data-stu-id="50cc6-116">Compile the statement as a series of <strong>if</strong> statements each with the <strong>branch</strong> attribute.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="50cc6-117">Al usar el modelo de <a href="dx-graphics-hlsl-sm2.md">sombreador 2. x</a> o el <a href="dx-graphics-hlsl-sm3.md">modelo de sombreador 3,0</a>, cada vez que se usa la bifurcación dinámica, se consumen recursos.</span><span class="sxs-lookup"><span data-stu-id="50cc6-117">When you use <a href="dx-graphics-hlsl-sm2.md">Shader Model 2.x</a> or <a href="dx-graphics-hlsl-sm3.md">Shader Model 3.0</a>, each time you use dynamic branching you consume resources.</span></span> <span data-ttu-id="50cc6-118">Por lo tanto, si utiliza la bifurcación dinámica de forma excesiva cuando tiene como destino estos perfiles, puede recibir errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="50cc6-118">So, if you use dynamic branching excessively when you target these profiles, you can receive compilation errors.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50cc6-119">forcecase</span><span class="sxs-lookup"><span data-stu-id="50cc6-119">forcecase</span></span></td>
<td><span data-ttu-id="50cc6-120">Fuerce una instrucción switch en el hardware.</span><span class="sxs-lookup"><span data-stu-id="50cc6-120">Force a switch statement in the hardware.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="50cc6-121">Requiere 10_0 de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">nivel de característica</a> o hardware posterior.</span><span class="sxs-lookup"><span data-stu-id="50cc6-121">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50cc6-122">llamada</span><span class="sxs-lookup"><span data-stu-id="50cc6-122">call</span></span></td>
<td><span data-ttu-id="50cc6-123">Los cuerpos de los casos individuales del conmutador se moverán a subrutinas de hardware y el modificador será una serie de llamadas subrutinas.</span><span class="sxs-lookup"><span data-stu-id="50cc6-123">The bodies of the individual cases in the switch will be moved into hardware subroutines and the switch will be a series of subroutine calls.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="50cc6-124">Requiere 10_0 de <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">nivel de característica</a> o hardware posterior.</span><span class="sxs-lookup"><span data-stu-id="50cc6-124">Requires <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a> 10_0 or later hardware.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="50cc6-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Situado*</span><span class="sxs-lookup"><span data-stu-id="50cc6-125"><span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Selector*</span></span>
</dt> <dd>

<span data-ttu-id="50cc6-126">Una variable.</span><span class="sxs-lookup"><span data-stu-id="50cc6-126">A variable.</span></span> <span data-ttu-id="50cc6-127">Las instrucciones Case dentro de los corchetes comprueban esta variable para ver si el SwitchValue coincide con su CaseValue determinado.</span><span class="sxs-lookup"><span data-stu-id="50cc6-127">The case statements inside the curly brackets will each check this variable to see if the SwitchValue matches their particular CaseValue.</span></span>

</dd> <dt>

<span data-ttu-id="50cc6-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="50cc6-128"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="50cc6-129">Una o más [instrucciones](dx-graphics-hlsl-statement-blocks.md).</span><span class="sxs-lookup"><span data-stu-id="50cc6-129">One or more [statements](dx-graphics-hlsl-statement-blocks.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50cc6-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50cc6-130">Remarks</span></span>


```
[branch] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



<span data-ttu-id="50cc6-131">Es equivalente a:</span><span class="sxs-lookup"><span data-stu-id="50cc6-131">Is equivalent to:</span></span>


```
[branch] if( a == 2 )
    return 3;
else if( a == 1 )
    return 1;
else if( a == 0 )
    return 0;
else
    return 6;
```



<span data-ttu-id="50cc6-132">Estos son los usos de ejemplo de forcecase y los atributos de control de flujo de llamadas:</span><span class="sxs-lookup"><span data-stu-id="50cc6-132">Here are example usages of forcecase and call flow control attributes:</span></span>


```
[forcecase] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}

[call] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



## <a name="requirements"></a><span data-ttu-id="50cc6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50cc6-133">Requirements</span></span>



| <span data-ttu-id="50cc6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="50cc6-134">Requirement</span></span> | <span data-ttu-id="50cc6-135">Value</span><span class="sxs-lookup"><span data-stu-id="50cc6-135">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="50cc6-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50cc6-136">Header</span></span><br/> | <dl> <span data-ttu-id="50cc6-137"><dt>Urlmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="50cc6-137"><dt>Urlmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50cc6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="50cc6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50cc6-139">Control de flujo</span><span class="sxs-lookup"><span data-stu-id="50cc6-139">Flow Control</span></span>](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

