---
description: Describe los datos incluidos en la enumeración.
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: Enumeración D3DXPARAMETER_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 16ff89feb694bb6aae550422b6f9546c2268fc07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362430"
---
# <a name="d3dxparameter_type-enumeration"></a><span data-ttu-id="231b7-103">\_Enumeración de tipo D3DXPARAMETER</span><span class="sxs-lookup"><span data-stu-id="231b7-103">D3DXPARAMETER\_TYPE enumeration</span></span>

<span data-ttu-id="231b7-104">Describe los datos incluidos en la enumeración.</span><span class="sxs-lookup"><span data-stu-id="231b7-104">Describes the data contained by the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="231b7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="231b7-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="231b7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="231b7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="231b7-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ void**</span><span class="sxs-lookup"><span data-stu-id="231b7-107"><span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT\_VOID**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-108">El parámetro es un puntero void.</span><span class="sxs-lookup"><span data-stu-id="231b7-108">Parameter is a void pointer.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="231b7-109"><span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-110">El parámetro es un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="231b7-110">Parameter is a Boolean.</span></span> <span data-ttu-id="231b7-111">Cualquier valor distinto de cero que se pase a [**ID3DXConstantTable:: SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable:: SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: SetVector**](id3dxconstanttable--setvector.md)o [**ID3DXConstantTable:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) se asignará a 1 (true) antes de escribirse en la tabla de constantes. de lo contrario, el valor se establecerá en 0 en la tabla Constant.</span><span class="sxs-lookup"><span data-stu-id="231b7-111">Any non-zero value passed into [**ID3DXConstantTable::SetBool**](id3dxconstanttable--setbool.md), [**ID3DXConstantTable::SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be mapped to 1 (TRUE) before being written into the constant table; otherwise, the value will be set to 0 in the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ int**</span><span class="sxs-lookup"><span data-stu-id="231b7-112"><span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT\_INT**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-113">El parámetro es un entero.</span><span class="sxs-lookup"><span data-stu-id="231b7-113">Parameter is an integer.</span></span> <span data-ttu-id="231b7-114">Los valores de punto flotante pasados en [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: SetVector**](id3dxconstanttable--setvector.md)o [**ID3DXConstantTable:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) se redondearán (a cero posiciones decimales) antes de escribirse en la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="231b7-114">Any floating-point values passed into [**ID3DXConstantTable::SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md), or [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) will be rounded off (to zero decimal places) before being written into the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ float**</span><span class="sxs-lookup"><span data-stu-id="231b7-115"><span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT\_FLOAT**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-116">El parámetro es un número de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="231b7-116">Parameter is a floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**\_Cadena D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="231b7-117"><span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**D3DXPT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-118">El parámetro es una cadena.</span><span class="sxs-lookup"><span data-stu-id="231b7-118">Parameter is a string.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**\_Textura D3DXPT**</span><span class="sxs-lookup"><span data-stu-id="231b7-119"><span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**D3DXPT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-120">El parámetro es una textura.</span><span class="sxs-lookup"><span data-stu-id="231b7-120">Parameter is a texture.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**</span><span class="sxs-lookup"><span data-stu-id="231b7-121"><span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT\_TEXTURE1D**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-122">El parámetro es una textura 1D.</span><span class="sxs-lookup"><span data-stu-id="231b7-122">Parameter is a 1D texture.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**</span><span class="sxs-lookup"><span data-stu-id="231b7-123"><span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT\_TEXTURE2D**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-124">El parámetro es una textura 2D.</span><span class="sxs-lookup"><span data-stu-id="231b7-124">Parameter is a 2D texture.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT \_ TEXTURE3D**</span><span class="sxs-lookup"><span data-stu-id="231b7-125"><span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**D3DXPT\_TEXTURE3D**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-126">El parámetro es una textura 3D.</span><span class="sxs-lookup"><span data-stu-id="231b7-126">Parameter is a 3D texture.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ TEXTURECUBE**</span><span class="sxs-lookup"><span data-stu-id="231b7-127"><span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT\_TEXTURECUBE**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-128">El parámetro es una textura del cubo.</span><span class="sxs-lookup"><span data-stu-id="231b7-128">Parameter is a cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**Muestra de D3DXPT \_**</span><span class="sxs-lookup"><span data-stu-id="231b7-129"><span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-130">El parámetro es una muestra.</span><span class="sxs-lookup"><span data-stu-id="231b7-130">Parameter is a sampler.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**</span><span class="sxs-lookup"><span data-stu-id="231b7-131"><span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT\_SAMPLER1D**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-132">El parámetro es una muestra 1D.</span><span class="sxs-lookup"><span data-stu-id="231b7-132">Parameter is a 1D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**</span><span class="sxs-lookup"><span data-stu-id="231b7-133"><span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT\_SAMPLER2D**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-134">El parámetro es una muestra 2D.</span><span class="sxs-lookup"><span data-stu-id="231b7-134">Parameter is a 2D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**</span><span class="sxs-lookup"><span data-stu-id="231b7-135"><span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT\_SAMPLER3D**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-136">El parámetro es una muestra 3D.</span><span class="sxs-lookup"><span data-stu-id="231b7-136">Parameter is a 3D sampler.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ SAMPLERCUBE**</span><span class="sxs-lookup"><span data-stu-id="231b7-137"><span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT\_SAMPLERCUBE**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-138">El parámetro es una muestra de cubo.</span><span class="sxs-lookup"><span data-stu-id="231b7-138">Parameter is a cube sampler.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ u**</span><span class="sxs-lookup"><span data-stu-id="231b7-139"><span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT\_PIXELSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-140">El parámetro es un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="231b7-140">Parameter is a pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ VERTEXSHADER**</span><span class="sxs-lookup"><span data-stu-id="231b7-141"><span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT\_VERTEXSHADER**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-142">El parámetro es un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="231b7-142">Parameter is a vertex shader.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ PIXELFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="231b7-143"><span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT\_PIXELFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-144">El parámetro es un fragmento de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="231b7-144">Parameter is a pixel shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ VERTEXFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="231b7-145"><span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT\_VERTEXFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-146">El parámetro es un fragmento de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="231b7-146">Parameter is a vertex shader fragment.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT \_ no compatible**</span><span class="sxs-lookup"><span data-stu-id="231b7-147"><span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT\_UNSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-148">No se admite el parámetro.</span><span class="sxs-lookup"><span data-stu-id="231b7-148">Parameter is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="231b7-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="231b7-149"><span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="231b7-150">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="231b7-150">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="231b7-151">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="231b7-151">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="231b7-152">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="231b7-152">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="231b7-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="231b7-153">Requirements</span></span>



| <span data-ttu-id="231b7-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="231b7-154">Requirement</span></span> | <span data-ttu-id="231b7-155">Value</span><span class="sxs-lookup"><span data-stu-id="231b7-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="231b7-156">Encabezado</span><span class="sxs-lookup"><span data-stu-id="231b7-156">Header</span></span><br/> | <dl> <span data-ttu-id="231b7-157"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="231b7-157"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="231b7-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="231b7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="231b7-159">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="231b7-159">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="231b7-160">**D3DXSHADER \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="231b7-160">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="231b7-161">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="231b7-161">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




