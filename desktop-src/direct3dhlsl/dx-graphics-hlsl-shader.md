---
title: Tipo de sombreador
description: La sintaxis para declarar una variable de sombreador en un efecto cambió de Direct3D 9 a Direct3D 10.
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- Tipo de sombreador HLSL
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ca3332c441279d7f9221efe8cfa7638908ddc44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984055"
---
# <a name="shader-type"></a><span data-ttu-id="33c03-104">Tipo de sombreador</span><span class="sxs-lookup"><span data-stu-id="33c03-104">Shader Type</span></span>

<span data-ttu-id="33c03-105">La sintaxis para declarar una variable de sombreador en un efecto cambió de Direct3D 9 a Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="33c03-105">The syntax for declaring a shader variable in an effect changed from Direct3D 9 to Direct3D 10.</span></span>

## <a name="shader-type-for-direct3d-10"></a><span data-ttu-id="33c03-106">Tipo de sombreador para Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="33c03-106">Shader Type for Direct3D 10</span></span>

<span data-ttu-id="33c03-107">Declare una variable de sombreador dentro de un paso de efecto (en Direct3D 10) con la sintaxis de tipo de sombreador:</span><span class="sxs-lookup"><span data-stu-id="33c03-107">Declare a shader variable within an effect pass (in Direct3D 10) using the shader type syntax:</span></span>



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c03-108">**SetPixelShader** Compilar ( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compilar ( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compilar ( **ShaderTarget, ShaderFunction** );</span><span class="sxs-lookup"><span data-stu-id="33c03-108">**SetPixelShader** Compile( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile( **ShaderTarget, ShaderFunction** );</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="33c03-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33c03-109">Parameters</span></span>



| <span data-ttu-id="33c03-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="33c03-110">Item</span></span>                                                                                                                             | <span data-ttu-id="33c03-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="33c03-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c03-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span><span class="sxs-lookup"><span data-stu-id="33c03-112"><span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**</span></span><br/>         | <span data-ttu-id="33c03-113">La llamada a la API de Direct3D que crea el objeto de sombreador.</span><span class="sxs-lookup"><span data-stu-id="33c03-113">The Direct3D API call that creates the shader object.</span></span> <span data-ttu-id="33c03-114">Puede ser: **SetPixelShader** o **SetGeometryShader** o **SetVertexShader**.</span><span class="sxs-lookup"><span data-stu-id="33c03-114">Can be either: **SetPixelShader** or **SetGeometryShader** or **SetVertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="33c03-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span><span class="sxs-lookup"><span data-stu-id="33c03-115"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>         | <span data-ttu-id="33c03-116">Modelo de sombreador con el que se va a realizar la compilación.</span><span class="sxs-lookup"><span data-stu-id="33c03-116">The shader model to compile against.</span></span> <span data-ttu-id="33c03-117">Esto es válido para cualquier destino, incluidos todos los destinos de Direct3D 9 más los destinos del [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) : vs \_ 4 \_ 0, GS \_ 4 \_ 0 y PS \_ 4 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="33c03-117">This is valid for any target including all Direct3D 9 targets plus the [shader model 4](dx-graphics-hlsl-sm4.md) targets: vs\_4\_0, gs\_4\_0, and ps\_4\_0.</span></span><br/>                                                                                                                                                                                                                                          |
| <span data-ttu-id="33c03-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="33c03-118"><span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**</span></span><br/> | <span data-ttu-id="33c03-119">Cadena ASCII que contiene el nombre de la función de punto de entrada del sombreador; Esta es la función que comienza la ejecución cuando se invoca el sombreador.</span><span class="sxs-lookup"><span data-stu-id="33c03-119">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="33c03-120">(...) Representa los argumentos del sombreador; Estos son los mismos argumentos que se pasan a las API de creación de sombreador: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) o [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) o [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span><span class="sxs-lookup"><span data-stu-id="33c03-120">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) or [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) or [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="33c03-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="33c03-121">Example</span></span>

<span data-ttu-id="33c03-122">Este es un ejemplo que crea un sombreador de vértices y un objeto de sombreador de píxeles, compilados para un modelo de sombreador determinado.</span><span class="sxs-lookup"><span data-stu-id="33c03-122">Here is an example that creates a vertex shader and pixel shader object, compiled for a particular shader model.</span></span> <span data-ttu-id="33c03-123">En el ejemplo de Direct3D 10, no hay sombreador de geometría, por lo que el puntero se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="33c03-123">In the Direct3D 10 example, there is no geometry shader, so the pointer is set to **NULL**.</span></span>


```
// Direct3D 10
technique10 Render
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, VS() ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PS() ) );
    }
}
```



## <a name="shader-type-for-direct3d-9"></a><span data-ttu-id="33c03-124">Tipo de sombreador para Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="33c03-124">Shader Type for Direct3D 9</span></span>

<span data-ttu-id="33c03-125">Declare una variable de sombreador dentro de un paso de efecto (para Direct3D 9) con la sintaxis de tipo de sombreador:</span><span class="sxs-lookup"><span data-stu-id="33c03-125">Declare a shader variable within an effect pass (for Direct3D 9) using the shader type syntax:</span></span>



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c03-126">**U** = compilar **ShaderTarget ShaderFunction (...); VertexShader** = compilar **ShaderTarget ShaderFunction (...);**</span><span class="sxs-lookup"><span data-stu-id="33c03-126">**PixelShader** = compile **ShaderTarget ShaderFunction(...);VertexShader** = compile **ShaderTarget ShaderFunction(...);**</span></span> |



 

### <a name="parameters"></a><span data-ttu-id="33c03-127">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33c03-127">Parameters</span></span>



| <span data-ttu-id="33c03-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="33c03-128">Item</span></span>                                                                                                                                                 | <span data-ttu-id="33c03-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="33c03-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c03-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span><span class="sxs-lookup"><span data-stu-id="33c03-130"><span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**</span></span><br/>                                         | <span data-ttu-id="33c03-131">Una variable de sombreador, que representa el sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="33c03-131">A shader variable, which represents the compiled shader.</span></span> <span data-ttu-id="33c03-132">Puede ser: **u** o **VertexShader**.</span><span class="sxs-lookup"><span data-stu-id="33c03-132">Can be either: **PixelShader** or **VertexShader**.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="33c03-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span><span class="sxs-lookup"><span data-stu-id="33c03-133"><span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**</span></span><br/>                             | <span data-ttu-id="33c03-134">[Modelo de sombreador](dx-graphics-hlsl-models.md) con el que se va a realizar la compilación; depende del tipo de variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="33c03-134">The [shader model](dx-graphics-hlsl-models.md) to compile against; depends on the type of shader variable.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="33c03-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**</span><span class="sxs-lookup"><span data-stu-id="33c03-135"><span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**</span></span><br/> | <span data-ttu-id="33c03-136">Cadena ASCII que contiene el nombre de la función de punto de entrada del sombreador; Esta es la función que comienza la ejecución cuando se invoca el sombreador.</span><span class="sxs-lookup"><span data-stu-id="33c03-136">An ASCII string that contains the name of the shader entry point function; this is the function that begins execution when the shader is invoked.</span></span> <span data-ttu-id="33c03-137">(...) Representa los argumentos del sombreador; Estos son los mismos argumentos que se pasan a las API de creación de sombreador: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) o [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span><span class="sxs-lookup"><span data-stu-id="33c03-137">The (...) represents the shader arguments; these are the same arguments passed to the shader creation API's: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) or [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).</span></span><br/> |



 

### <a name="example"></a><span data-ttu-id="33c03-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="33c03-138">Example</span></span>

<span data-ttu-id="33c03-139">Este es un ejemplo de un sombreador de vértices y un objeto de sombreador de píxeles, compilado para un modelo de sombreador determinado.</span><span class="sxs-lookup"><span data-stu-id="33c03-139">Here is an example of a vertex shader and pixel shader object, compiled for a particular shader model.</span></span>


```
// Direct3D 9
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_2_0 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_2_0 RenderScenePS( true );
    }
}
```



## <a name="see-also"></a><span data-ttu-id="33c03-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="33c03-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c03-141">Tipos de datos (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="33c03-141">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

