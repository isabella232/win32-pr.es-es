---
description: Define constantes que describen los valores de estado de la transformación.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumeración D3DTRANSFORMSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c618e0e19bf7dd01dec73d35436f23189f9e78a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717693"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="28c32-103">Enumeración D3DTRANSFORMSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="28c32-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="28c32-104">Define constantes que describen los valores de estado de la transformación.</span><span class="sxs-lookup"><span data-stu-id="28c32-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c32-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28c32-105">Syntax</span></span>


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="28c32-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="28c32-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="28c32-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**\_Vista D3DTS**</span><span class="sxs-lookup"><span data-stu-id="28c32-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="28c32-108">Identifica la matriz de transformación que se establece como la matriz de transformación de la vista.</span><span class="sxs-lookup"><span data-stu-id="28c32-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="28c32-109">El valor predeterminado es **null** (la matriz de identidad).</span><span class="sxs-lookup"><span data-stu-id="28c32-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="28c32-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_Proyección D3DTS**</span><span class="sxs-lookup"><span data-stu-id="28c32-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="28c32-111">Identifica la matriz de transformación que se establece como la matriz de transformación de proyección.</span><span class="sxs-lookup"><span data-stu-id="28c32-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="28c32-112">El valor predeterminado es **null** (la matriz de identidad).</span><span class="sxs-lookup"><span data-stu-id="28c32-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="28c32-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**</span><span class="sxs-lookup"><span data-stu-id="28c32-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="28c32-114">Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="28c32-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="28c32-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ textura1**</span><span class="sxs-lookup"><span data-stu-id="28c32-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="28c32-116">Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="28c32-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="28c32-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ textura2**</span><span class="sxs-lookup"><span data-stu-id="28c32-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="28c32-118">Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="28c32-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="28c32-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**</span><span class="sxs-lookup"><span data-stu-id="28c32-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="28c32-120">Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="28c32-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="28c32-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**</span><span class="sxs-lookup"><span data-stu-id="28c32-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="28c32-122">Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="28c32-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="28c32-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**</span><span class="sxs-lookup"><span data-stu-id="28c32-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="28c32-124">Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="28c32-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="28c32-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**</span><span class="sxs-lookup"><span data-stu-id="28c32-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="28c32-126">Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="28c32-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="28c32-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**</span><span class="sxs-lookup"><span data-stu-id="28c32-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="28c32-128">Identifica la matriz de transformación que se va a establecer para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="28c32-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="28c32-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="28c32-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="28c32-130">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="28c32-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="28c32-131">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="28c32-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="28c32-132">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="28c32-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28c32-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="28c32-133">Remarks</span></span>

<span data-ttu-id="28c32-134">Los Estados de transformación en el intervalo de 256 a 511 se reservan para almacenar hasta 256 matrices del mundo que se pueden indexar mediante las \_ macros D3DTS WORLDMATRIX y D3DTS \_ World.</span><span class="sxs-lookup"><span data-stu-id="28c32-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="28c32-135">Macros</span><span class="sxs-lookup"><span data-stu-id="28c32-135">Macros</span></span>                                                  |                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="28c32-136">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="28c32-136">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="28c32-137">Equivalente a D3DTS \_ WORLDMATRIX (0).</span><span class="sxs-lookup"><span data-stu-id="28c32-137">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="28c32-138">[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (índice)</span><span class="sxs-lookup"><span data-stu-id="28c32-138">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="28c32-139">Identifica la matriz de transformación que se va a establecer para la matriz universal en el índice.</span><span class="sxs-lookup"><span data-stu-id="28c32-139">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="28c32-140">Las matrices de varios mundo solo se usan para la combinación de vértices.</span><span class="sxs-lookup"><span data-stu-id="28c32-140">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="28c32-141">De lo contrario, solo \_ se usa D3DTS World.</span><span class="sxs-lookup"><span data-stu-id="28c32-141">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="28c32-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28c32-142">Requirements</span></span>



| <span data-ttu-id="28c32-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c32-143">Requirement</span></span> | <span data-ttu-id="28c32-144">Value</span><span class="sxs-lookup"><span data-stu-id="28c32-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28c32-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28c32-145">Header</span></span><br/> | <dl> <span data-ttu-id="28c32-146"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c32-146"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c32-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="28c32-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c32-148">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="28c32-148">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="28c32-149">**IDirect3DDevice9::GetTransform**</span><span class="sxs-lookup"><span data-stu-id="28c32-149">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="28c32-150">**IDirect3DDevice9::MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="28c32-150">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="28c32-151">**IDirect3DDevice9::SetTransform**</span><span class="sxs-lookup"><span data-stu-id="28c32-151">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="28c32-152">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="28c32-152">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="28c32-153">**D3DTS \_ worlda**</span><span class="sxs-lookup"><span data-stu-id="28c32-153">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="28c32-154">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="28c32-154">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
