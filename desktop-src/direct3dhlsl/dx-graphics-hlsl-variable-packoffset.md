---
title: packoffset
description: Palabra clave opcional de empaquetado constante de sombreador, que usa la sintaxis siguiente
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- packoffset HLSL
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c92a6375f0724a1910fc0f09b47e1593614f9f1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826084"
---
# <a name="packoffset"></a><span data-ttu-id="5293f-104">packoffset</span><span class="sxs-lookup"><span data-stu-id="5293f-104">packoffset</span></span>

<span data-ttu-id="5293f-105">Palabra clave opcional de empaquetado constante de sombreador, que usa la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="5293f-105">Optional shader constant packing keyword, which uses the following syntax:</span></span>

<span data-ttu-id="5293f-106">: packoffset( c \[ Subcomponent \] \[ .component \] )</span><span class="sxs-lookup"><span data-stu-id="5293f-106">: packoffset( c\[Subcomponent\]\[.component\] )</span></span>



 

## <a name="parameters"></a><span data-ttu-id="5293f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5293f-107">Parameters</span></span>



| <span data-ttu-id="5293f-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="5293f-108">Item</span></span>                                                                                                                                                                                 | <span data-ttu-id="5293f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5293f-109">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5293f-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span><span class="sxs-lookup"><span data-stu-id="5293f-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span></span><br/>                                                                                                  | <span data-ttu-id="5293f-111">Palabra clave required.</span><span class="sxs-lookup"><span data-stu-id="5293f-111">Required keyword.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="5293f-112"><span id="c"></span><span id="C"></span>**C**</span><span class="sxs-lookup"><span data-stu-id="5293f-112"><span id="c"></span><span id="C"></span>**c**</span></span><br/>                                                                                                                             | <span data-ttu-id="5293f-113">El empaquetado solo se aplica a los registros constantes (c).</span><span class="sxs-lookup"><span data-stu-id="5293f-113">Packing applies to constant registers (c) only.</span></span> <br/>                                                                                          |
| <span data-ttu-id="5293f-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent \] \[ .component\]**</span><span class="sxs-lookup"><span data-stu-id="5293f-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent\]\[.component\]**</span></span><br/> | <span data-ttu-id="5293f-115">Subcomponentes y componentes opcionales.</span><span class="sxs-lookup"><span data-stu-id="5293f-115">Optional subcomponents and components.</span></span> <span data-ttu-id="5293f-116">Un subcomponente es un número de registro, que es un entero.</span><span class="sxs-lookup"><span data-stu-id="5293f-116">A subcomponent is a register number, which is an integer.</span></span> <span data-ttu-id="5293f-117">Un componente tiene el formato \[ .xyzw \] .</span><span class="sxs-lookup"><span data-stu-id="5293f-117">A component is in the form of \[.xyzw\].</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5293f-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5293f-118">Remarks</span></span>

<span data-ttu-id="5293f-119">Use esta palabra clave para empaquetar manualmente una constante de sombreador [al declarar un tipo de variable](dx-graphics-hlsl-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="5293f-119">Use this keyword to manually pack a shader constant when [declaring a variable type](dx-graphics-hlsl-variable-syntax.md).</span></span>

<span data-ttu-id="5293f-120">Al empaquetar una constante, no se pueden mezclar tipos constantes.</span><span class="sxs-lookup"><span data-stu-id="5293f-120">When packing a constant, you cannot mix constant types.</span></span>

<span data-ttu-id="5293f-121">El compilador se comporta de forma ligeramente diferente para las constantes globales y las constantes uniformes:</span><span class="sxs-lookup"><span data-stu-id="5293f-121">The compiler behaves slightly differently for global constants and uniform constants:</span></span>

-   <span data-ttu-id="5293f-122">Constante global.</span><span class="sxs-lookup"><span data-stu-id="5293f-122">A global constant.</span></span> <span data-ttu-id="5293f-123">El compilador agrega una variable global como una constante global a *$Global* cbuffer.</span><span class="sxs-lookup"><span data-stu-id="5293f-123">A global variable is added as a global constant to a *$Global* cbuffer by the compiler.</span></span> <span data-ttu-id="5293f-124">Los elementos empaquetados automáticamente (los declarados sin packoffset) aparecerán después de la última variable empaquetada manualmente.</span><span class="sxs-lookup"><span data-stu-id="5293f-124">Automatically packed elements (those declared without packoffset) will appear after the last manually packed variable.</span></span> <span data-ttu-id="5293f-125">Puede mezclar tipos al empaquetar constantes globales.</span><span class="sxs-lookup"><span data-stu-id="5293f-125">You may mix types when packing global constants.</span></span>
-   <span data-ttu-id="5293f-126">Constante uniforme.</span><span class="sxs-lookup"><span data-stu-id="5293f-126">A uniform constant.</span></span> <span data-ttu-id="5293f-127">El compilador agregará un parámetro uniforme en la lista de parámetros de una función $Param un búfer constante de *$Param* cuando el sombreador se compile fuera del marco de efectos.</span><span class="sxs-lookup"><span data-stu-id="5293f-127">A uniform parameter in the parameter list of a function will be added to a *$Param* constant buffer by the compiler when the shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="5293f-128">Cuando se compila dentro del marco de efectos, una constante uniforme debe resolverse en una variable uniforme definida en el ámbito global.</span><span class="sxs-lookup"><span data-stu-id="5293f-128">When compiled inside the effect framework, a uniform constant must resolve to a uniform variable defined in global scope.</span></span> <span data-ttu-id="5293f-129">Una constante uniforme no se puede desplazar manualmente; Su uso recomendado es solo para la especialización de sombreadores en los que se les aplica el alias de vuelta a los globales, no como un medio de pasar datos de aplicación al sombreador.</span><span class="sxs-lookup"><span data-stu-id="5293f-129">A uniform constant cannot be manually offset; their recommend use is only for specialization of shaders where they alias back to globals, not as a means of passing application data into the shader.</span></span>

<span data-ttu-id="5293f-130">Estos son algunos ejemplos adicionales: [empaquetado de constantes mediante el modelo de sombreador 4](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="5293f-130">Here are some additional examples: [packing constants using shader model 4](dx-graphics-hlsl-packing-rules.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5293f-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5293f-131">Examples</span></span>

<span data-ttu-id="5293f-132">Estos son varios ejemplos de empaquetado manual de constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="5293f-132">Here are several examples of manually packing shader constants.</span></span>

<span data-ttu-id="5293f-133">Empaquetar subcomponentes de vectores y escalares cuyo tamaño es lo suficientemente grande como para evitar cruzar los límites del registro.</span><span class="sxs-lookup"><span data-stu-id="5293f-133">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundaries.</span></span> <span data-ttu-id="5293f-134">Por ejemplo, todos estos son válidos:</span><span class="sxs-lookup"><span data-stu-id="5293f-134">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a><span data-ttu-id="5293f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="5293f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5293f-136">Sintaxis de variables</span><span class="sxs-lookup"><span data-stu-id="5293f-136">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="5293f-137">Variables (HLSL de DirectX)</span><span class="sxs-lookup"><span data-stu-id="5293f-137">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





