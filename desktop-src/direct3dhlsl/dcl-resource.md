---
title: dcl_resource (SM4-ASM)
description: '\_recurso DCL (SM4-ASM)'
ms.assetid: 045610f0-f7db-4bf2-bfea-501bbee94601
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb65a8ea83feaf2fec80403fc9ac6c2ab38c1936
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785008"
---
# <a name="dcl_resource-sm4---asm"></a><span data-ttu-id="9def0-103">\_recurso DCL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9def0-103">dcl\_resource (sm4 - asm)</span></span>

<span data-ttu-id="9def0-104">Declara un recurso de entrada de sombreador no multimuestreado.</span><span class="sxs-lookup"><span data-stu-id="9def0-104">Declares a non-multisampled shader-input resource.</span></span>



| <span data-ttu-id="9def0-105">DCL \_ Resource *tN*, *resourceType*, *ReturnType (s)*</span><span class="sxs-lookup"><span data-stu-id="9def0-105">dcl\_resource *tN*, *resourceType*, *returnType(s)*</span></span> |
|-----------------------------------------------------|



 

<span data-ttu-id="9def0-106">Declara un recurso de entrada de sombreador de muestreo múltiple.</span><span class="sxs-lookup"><span data-stu-id="9def0-106">Declares a multisampled shader-input resource.</span></span>



| <span data-ttu-id="9def0-107">DCL \_ Resource *tN*, *resourceType \[ tamaño \] nn*, *ReturnType (s)*</span><span class="sxs-lookup"><span data-stu-id="9def0-107">dcl\_resource *tN*, *resourceType\[size\]NN*, *returnType(s)*</span></span> |
|---------------------------------------------------------------|



 



| <span data-ttu-id="9def0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="9def0-108">Item</span></span>                                                                                                                                                     | <span data-ttu-id="9def0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9def0-109">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9def0-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span><span class="sxs-lookup"><span data-stu-id="9def0-110"><span id="tN"></span><span id="tn"></span><span id="TN"></span>t *N*</span></span><br/>                                                                           | <span data-ttu-id="9def0-111">\[en \] el registro de textura, donde *N* es un entero que denota el número de registro.</span><span class="sxs-lookup"><span data-stu-id="9def0-111">\[in\] The texture register, where *N* is an integer that denotes the register number.</span></span><br/>                                                                                                                                                                        |
| <span data-ttu-id="9def0-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span><span class="sxs-lookup"><span data-stu-id="9def0-112"><span id="resourceType"></span><span id="resourcetype"></span><span id="RESOURCETYPE"></span>*resourceType*</span></span><br/>                                   | <span data-ttu-id="9def0-113">\[en \] cualquier tipo de objeto que se muestra en la página [Texture-Object](dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="9def0-113">\[in\] Any object type listed in the [texture-object](dx-graphics-hlsl-to-type.md) page.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="9def0-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType \[ tamaño \] NN*</span><span class="sxs-lookup"><span data-stu-id="9def0-114"><span id="resourceType_size_NN"></span><span id="resourcetype_size_nn"></span><span id="RESOURCETYPE_SIZE_NN"></span>*resourceType\[size\]NN*</span></span><br/> | <span data-ttu-id="9def0-115">\[en \] un tipo de objeto Texture2D o Texture2DArray (vea la página [Texture-Object](dx-graphics-hlsl-to-type.md) ); *size* es un entero opcional que denota el número de elementos de la matriz; *Nn* es un entero que denota el número de muestras de varios.</span><span class="sxs-lookup"><span data-stu-id="9def0-115">\[in\] A Texture2D or a Texture2DArray object type (see the [texture-object](dx-graphics-hlsl-to-type.md) page); *size* is an optional integer that denotes the number of elements in the array; *NN* is an integer that denotes the number of multisamples.</span></span><br/> |
| <span data-ttu-id="9def0-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType (s)*</span><span class="sxs-lookup"><span data-stu-id="9def0-116"><span id="returnType_s_"></span><span id="returntype_s_"></span><span id="RETURNTYPE_S_"></span>*returnType(s)*</span></span><br/>                               | <span data-ttu-id="9def0-117">\[en \] el tipo de valor devuelto por componente, que es uno de los siguientes: UNORM, SNORM, Sint, uint o float.</span><span class="sxs-lookup"><span data-stu-id="9def0-117">\[in\] Per-component return type which is one of the following: UNORM, SNORM, SINT, UINT, or FLOAT.</span></span> <span data-ttu-id="9def0-118">El número de tipos de valor devuelto puede ser tan pocos como 1 (si todos los componentes son del mismo tipo), pero puede ser de hasta cuatro.</span><span class="sxs-lookup"><span data-stu-id="9def0-118">The number of return types can be as few as 1 (if all components are the same type), but can be as many as four.</span></span><br/>                                          |



 

<span data-ttu-id="9def0-119">Se tiene acceso a un recurso en HLSL mediante la [carga](dx-graphics-hlsl-to-load.md); también se puede tener acceso a una textura no multimuestreada mediante cualquiera de los métodos de ejemplo de [objeto de textura](dx-graphics-hlsl-to-type.md) HLSL.</span><span class="sxs-lookup"><span data-stu-id="9def0-119">A resource is accessed in HLSL using [load](dx-graphics-hlsl-to-load.md); a non-multisampled texture can also be accessed using any of the HLSL [texture object](dx-graphics-hlsl-to-type.md) sample methods.</span></span>

<span data-ttu-id="9def0-120">Si un recurso se enlaza a una fase del sombreador, el formato de los recursos se validará con el tipo de valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="9def0-120">If a resource is bound to a shader stage, the resource format will be validated against the return type.</span></span>

<span data-ttu-id="9def0-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="9def0-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9def0-122">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="9def0-122">Vertex Shader</span></span> | <span data-ttu-id="9def0-123">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="9def0-123">Geometry Shader</span></span> | <span data-ttu-id="9def0-124">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="9def0-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9def0-125">x</span><span class="sxs-lookup"><span data-stu-id="9def0-125">x</span></span>             | <span data-ttu-id="9def0-126">x</span><span class="sxs-lookup"><span data-stu-id="9def0-126">x</span></span>               | <span data-ttu-id="9def0-127">x</span><span class="sxs-lookup"><span data-stu-id="9def0-127">x</span></span>            |



 

<span data-ttu-id="9def0-128">Esta instrucción se incluye para ayudar en la depuración de un sombreador en el ensamblado. no se puede crear un sombreador en lenguaje de ensamblado con el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="9def0-128">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="9def0-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9def0-129">Example</span></span>

<span data-ttu-id="9def0-130">A continuación se muestra un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="9def0-130">Here is an example.</span></span>


```
dcl_resource t3, buffer, UNORM
```



## <a name="minimum-shader-model"></a><span data-ttu-id="9def0-131">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="9def0-131">Minimum Shader Model</span></span>

<span data-ttu-id="9def0-132">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9def0-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9def0-133">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="9def0-133">Shader Model</span></span>                                              | <span data-ttu-id="9def0-134">Compatible</span><span class="sxs-lookup"><span data-stu-id="9def0-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9def0-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9def0-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9def0-136">sí</span><span class="sxs-lookup"><span data-stu-id="9def0-136">yes</span></span>       |
| [<span data-ttu-id="9def0-137">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="9def0-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9def0-138">sí</span><span class="sxs-lookup"><span data-stu-id="9def0-138">yes</span></span>       |
| [<span data-ttu-id="9def0-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9def0-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9def0-140">sí</span><span class="sxs-lookup"><span data-stu-id="9def0-140">yes</span></span>       |
| [<span data-ttu-id="9def0-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9def0-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9def0-142">no</span><span class="sxs-lookup"><span data-stu-id="9def0-142">no</span></span>        |
| [<span data-ttu-id="9def0-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9def0-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9def0-144">no</span><span class="sxs-lookup"><span data-stu-id="9def0-144">no</span></span>        |
| [<span data-ttu-id="9def0-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9def0-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9def0-146">no</span><span class="sxs-lookup"><span data-stu-id="9def0-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9def0-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9def0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9def0-148">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9def0-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





