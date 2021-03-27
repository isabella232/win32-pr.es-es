---
title: packoffset
description: Palabra clave de empaquetado constante de sombreador opcional, que usa la sintaxis siguiente
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- HLSL de packoffset
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6feeaa586abe30fa8a36c28d0298dc408cdfb099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358080"
---
# <a name="packoffset"></a><span data-ttu-id="a9648-104">packoffset</span><span class="sxs-lookup"><span data-stu-id="a9648-104">packoffset</span></span>

<span data-ttu-id="a9648-105">Palabra clave de empaquetado constante de sombreador opcional, que usa la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="a9648-105">Optional shader constant packing keyword, which uses the following syntax:</span></span>



|                                                 |
|-------------------------------------------------|
| <span data-ttu-id="a9648-106">: packoffset ( \[ subcomponente de c \] \[ . Component \] )</span><span class="sxs-lookup"><span data-stu-id="a9648-106">: packoffset( c\[Subcomponent\]\[.component\] )</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="a9648-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9648-107">Parameters</span></span>



| <span data-ttu-id="a9648-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a9648-108">Item</span></span>                                                                                                                                                                                 | <span data-ttu-id="a9648-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9648-109">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9648-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span><span class="sxs-lookup"><span data-stu-id="a9648-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span></span><br/>                                                                                                  | <span data-ttu-id="a9648-111">Palabra clave required.</span><span class="sxs-lookup"><span data-stu-id="a9648-111">Required keyword.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="a9648-112"><span id="c"></span><span id="C"></span>**unidad**</span><span class="sxs-lookup"><span data-stu-id="a9648-112"><span id="c"></span><span id="C"></span>**c**</span></span><br/>                                                                                                                             | <span data-ttu-id="a9648-113">El empaquetado se aplica solo a los registros constantes (c).</span><span class="sxs-lookup"><span data-stu-id="a9648-113">Packing applies to constant registers (c) only.</span></span> <br/>                                                                                          |
| <span data-ttu-id="a9648-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[SubComponent \] \[ . Component\]**</span><span class="sxs-lookup"><span data-stu-id="a9648-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent\]\[.component\]**</span></span><br/> | <span data-ttu-id="a9648-115">Subcomponentes y componentes opcionales.</span><span class="sxs-lookup"><span data-stu-id="a9648-115">Optional subcomponents and components.</span></span> <span data-ttu-id="a9648-116">Un subcomponente es un número de registro, que es un entero.</span><span class="sxs-lookup"><span data-stu-id="a9648-116">A subcomponent is a register number, which is an integer.</span></span> <span data-ttu-id="a9648-117">Un componente tiene el formato \[ . xyzw \] .</span><span class="sxs-lookup"><span data-stu-id="a9648-117">A component is in the form of \[.xyzw\].</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a9648-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a9648-118">Remarks</span></span>

<span data-ttu-id="a9648-119">Use esta palabra clave para empaquetar manualmente una constante de sombreador al [declarar un tipo de variable](dx-graphics-hlsl-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="a9648-119">Use this keyword to manually pack a shader constant when [declaring a variable type](dx-graphics-hlsl-variable-syntax.md).</span></span>

<span data-ttu-id="a9648-120">Cuando se empaqueta una constante, no se pueden mezclar tipos constantes.</span><span class="sxs-lookup"><span data-stu-id="a9648-120">When packing a constant, you cannot mix constant types.</span></span>

<span data-ttu-id="a9648-121">El compilador se comporta de forma ligeramente diferente para las constantes globales y las constantes uniformes:</span><span class="sxs-lookup"><span data-stu-id="a9648-121">The compiler behaves slightly differently for global constants and uniform constants:</span></span>

-   <span data-ttu-id="a9648-122">Constante global.</span><span class="sxs-lookup"><span data-stu-id="a9648-122">A global constant.</span></span> <span data-ttu-id="a9648-123">Una variable global se agrega como una constante global a un *$global* CBuffer por el compilador.</span><span class="sxs-lookup"><span data-stu-id="a9648-123">A global variable is added as a global constant to a *$Global* cbuffer by the compiler.</span></span> <span data-ttu-id="a9648-124">Los elementos empaquetados automáticamente (los declarados sin packoffset) aparecerán después de la última variable empaquetada manualmente.</span><span class="sxs-lookup"><span data-stu-id="a9648-124">Automatically packed elements (those declared without packoffset) will appear after the last manually packed variable.</span></span> <span data-ttu-id="a9648-125">Puede mezclar tipos al empaquetar constantes globales.</span><span class="sxs-lookup"><span data-stu-id="a9648-125">You may mix types when packing global constants.</span></span>
-   <span data-ttu-id="a9648-126">Constante uniforme.</span><span class="sxs-lookup"><span data-stu-id="a9648-126">A uniform constant.</span></span> <span data-ttu-id="a9648-127">El compilador *$param* agregará un parámetro uniforme en la lista de parámetros de una función cuando el sombreador se compile fuera del marco de trabajo de efectos.</span><span class="sxs-lookup"><span data-stu-id="a9648-127">A uniform parameter in the parameter list of a function will be added to a *$Param* constant buffer by the compiler when the shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="a9648-128">Cuando se compila dentro del marco de trabajo de efecto, una constante uniforme debe resolverse en una variable uniforme definida en el ámbito global.</span><span class="sxs-lookup"><span data-stu-id="a9648-128">When compiled inside the effect framework, a uniform constant must resolve to a uniform variable defined in global scope.</span></span> <span data-ttu-id="a9648-129">Una constante uniforme no puede desplazarse manualmente; su uso recomendado es solo para la especialización de los sombreadores en los que el alias se vuelve a globales, no como un medio para pasar datos de aplicación al sombreador.</span><span class="sxs-lookup"><span data-stu-id="a9648-129">A uniform constant cannot be manually offset; their recommend use is only for specialization of shaders where they alias back to globals, not as a means of passing application data into the shader.</span></span>

<span data-ttu-id="a9648-130">Estos son algunos ejemplos adicionales: [empaquetar constantes con el modelo de sombreador 4](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="a9648-130">Here are some additional examples: [packing constants using shader model 4](dx-graphics-hlsl-packing-rules.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a9648-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a9648-131">Examples</span></span>

<span data-ttu-id="a9648-132">Estos son algunos ejemplos de cómo empaquetar manualmente las constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a9648-132">Here are several examples of manually packing shader constants.</span></span>

<span data-ttu-id="a9648-133">Empaquete subcomponentes de vectores y escalares cuyo tamaño sea lo suficientemente grande como para evitar cruzar los límites del registro.</span><span class="sxs-lookup"><span data-stu-id="a9648-133">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundaries.</span></span> <span data-ttu-id="a9648-134">Por ejemplo, todos son válidos:</span><span class="sxs-lookup"><span data-stu-id="a9648-134">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a><span data-ttu-id="a9648-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9648-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9648-136">Sintaxis de variables</span><span class="sxs-lookup"><span data-stu-id="a9648-136">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="a9648-137">Variables (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a9648-137">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





