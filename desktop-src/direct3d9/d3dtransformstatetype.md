---
description: Define constantes que describen los valores de estado de transformación.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumeración D3DTRANSFORMSTATETYPE (D3D9Types.h)
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
ms.openlocfilehash: 022aa20fab0739b32aa75eb5f4bc575c0a8ad853
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343000"
---
# <a name="d3dtransformstatetype-enumeration"></a><span data-ttu-id="6b802-103">D3DTRANSFORMSTATETYPE (enumeración)</span><span class="sxs-lookup"><span data-stu-id="6b802-103">D3DTRANSFORMSTATETYPE enumeration</span></span>

<span data-ttu-id="6b802-104">Define constantes que describen los valores de estado de transformación.</span><span class="sxs-lookup"><span data-stu-id="6b802-104">Defines constants that describe transformation state values.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b802-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b802-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="6b802-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="6b802-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6b802-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**VISTA \_ D3DTS**</span><span class="sxs-lookup"><span data-stu-id="6b802-107"><span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**D3DTS\_VIEW**</span></span>
</dt> <dd>

<span data-ttu-id="6b802-108">Identifica la matriz de transformación que se establece como la matriz de transformación de vista.</span><span class="sxs-lookup"><span data-stu-id="6b802-108">Identifies the transformation matrix being set as the view transformation matrix.</span></span> <span data-ttu-id="6b802-109">El valor predeterminado es **NULL** (la matriz de identidad).</span><span class="sxs-lookup"><span data-stu-id="6b802-109">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="6b802-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**PROYECCIÓN DE \_ D3DTS**</span><span class="sxs-lookup"><span data-stu-id="6b802-110"><span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**D3DTS\_PROJECTION**</span></span>
</dt> <dd>

<span data-ttu-id="6b802-111">Identifica la matriz de transformación que se establece como matriz de transformación de proyección.</span><span class="sxs-lookup"><span data-stu-id="6b802-111">Identifies the transformation matrix being set as the projection transformation matrix.</span></span> <span data-ttu-id="6b802-112">El valor predeterminado es **NULL** (la matriz de identidad).</span><span class="sxs-lookup"><span data-stu-id="6b802-112">The default value is **NULL** (the identity matrix).</span></span>

</dd> <dt>

<span data-ttu-id="6b802-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**TEXTURA DE \_ D3DTS0**</span><span class="sxs-lookup"><span data-stu-id="6b802-113"><span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS\_TEXTURE0**</span></span>
</dt> <dd>

<span data-ttu-id="6b802-114">Identifica la matriz de transformación que se establece para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="6b802-114">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6b802-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**TEXTURA D3DTS1 \_**</span><span class="sxs-lookup"><span data-stu-id="6b802-115"><span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS\_TEXTURE1**</span></span>
</dt> <dd>

<span data-ttu-id="6b802-116">Identifica la matriz de transformación que se establece para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="6b802-116">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6b802-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**TEXTURA DE \_ D3DTS2**</span><span class="sxs-lookup"><span data-stu-id="6b802-117"><span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS\_TEXTURE2**</span></span>
</dt> <dd>

<span data-ttu-id="6b802-118">Identifica la matriz de transformación que se establece para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="6b802-118">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6b802-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**TEXTURA DE \_ D3DTS3**</span><span class="sxs-lookup"><span data-stu-id="6b802-119"><span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS\_TEXTURE3**</span></span>
</dt> <dd>

<span data-ttu-id="6b802-120">Identifica la matriz de transformación que se establece para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="6b802-120">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6b802-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**TEXTURA D3DTS4 \_**</span><span class="sxs-lookup"><span data-stu-id="6b802-121"><span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS\_TEXTURE4**</span></span>
</dt> <dd>

<span data-ttu-id="6b802-122">Identifica la matriz de transformación que se establece para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="6b802-122">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6b802-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**TEXTURA DE \_ D3DTS5**</span><span class="sxs-lookup"><span data-stu-id="6b802-123"><span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS\_TEXTURE5**</span></span>
</dt> <dd>

<span data-ttu-id="6b802-124">Identifica la matriz de transformación que se establece para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="6b802-124">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6b802-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**TEXTURA DE \_ D3DTS6**</span><span class="sxs-lookup"><span data-stu-id="6b802-125"><span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS\_TEXTURE6**</span></span>
</dt> <dd>

<span data-ttu-id="6b802-126">Identifica la matriz de transformación que se establece para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="6b802-126">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6b802-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**TEXTURA D3DTS7 \_**</span><span class="sxs-lookup"><span data-stu-id="6b802-127"><span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS\_TEXTURE7**</span></span>
</dt> <dd>

<span data-ttu-id="6b802-128">Identifica la matriz de transformación que se establece para la fase de textura especificada.</span><span class="sxs-lookup"><span data-stu-id="6b802-128">Identifies the transformation matrix being set for the specified texture stage.</span></span>

</dd> <dt>

<span data-ttu-id="6b802-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6b802-129"><span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="6b802-130">Fuerza esta enumeración a compilar hasta 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="6b802-130">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="6b802-131">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="6b802-131">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="6b802-132">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6b802-132">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b802-133">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b802-133">Remarks</span></span>

<span data-ttu-id="6b802-134">Los estados de transformación del intervalo de 256 a 511 están reservados para almacenar hasta 256 matrices globales que se pueden indexar mediante las \_ macros WORLDMATRIX y D3DTS WORLD de D3DTS. \_</span><span class="sxs-lookup"><span data-stu-id="6b802-134">The transform states in the range 256 through 511 are reserved to store up to 256 world matrices that can be indexed using the D3DTS\_WORLDMATRIX and D3DTS\_WORLD macros.</span></span>



| <span data-ttu-id="6b802-135">Macros</span><span class="sxs-lookup"><span data-stu-id="6b802-135">Macros</span></span>                                                  | <span data-ttu-id="6b802-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="6b802-136">Description</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b802-137">**D3DTS \_ WORLD**</span><span class="sxs-lookup"><span data-stu-id="6b802-137">**D3DTS\_WORLD**</span></span>](d3dts-world.md)                     | <span data-ttu-id="6b802-138">Equivalente a D3DTS \_ WORLDMATRIX(0).</span><span class="sxs-lookup"><span data-stu-id="6b802-138">Equivalent to D3DTS\_WORLDMATRIX(0).</span></span>                                                                                                                                  |
| <span data-ttu-id="6b802-139">[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (índice)</span><span class="sxs-lookup"><span data-stu-id="6b802-139">[**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) (index)</span></span> | <span data-ttu-id="6b802-140">Identifica la matriz de transformación que se establecerá para la matriz mundial en el índice.</span><span class="sxs-lookup"><span data-stu-id="6b802-140">Identifies the transform matrix to set for the world matrix at index.</span></span> <span data-ttu-id="6b802-141">Solo se usan varias matrices de mundo para la mezcla de vértices.</span><span class="sxs-lookup"><span data-stu-id="6b802-141">Multiple world matrices are used only for vertex blending.</span></span> <span data-ttu-id="6b802-142">De lo contrario, solo se usa D3DTS \_ WORLD.</span><span class="sxs-lookup"><span data-stu-id="6b802-142">Otherwise only D3DTS\_WORLD is used.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6b802-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b802-143">Requirements</span></span>



| <span data-ttu-id="6b802-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b802-144">Requirement</span></span> | <span data-ttu-id="6b802-145">Value</span><span class="sxs-lookup"><span data-stu-id="6b802-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b802-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b802-146">Header</span></span><br/> | <dl> <span data-ttu-id="6b802-147"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="6b802-147"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b802-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b802-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b802-149">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="6b802-149">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="6b802-150">**IDirect3DDevice9::GetTransform**</span><span class="sxs-lookup"><span data-stu-id="6b802-150">**IDirect3DDevice9::GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="6b802-151">**IDirect3DDevice9::MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="6b802-151">**IDirect3DDevice9::MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="6b802-152">**IDirect3DDevice9::SetTransform**</span><span class="sxs-lookup"><span data-stu-id="6b802-152">**IDirect3DDevice9::SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[<span data-ttu-id="6b802-153">**D3DTS \_ WORLD**</span><span class="sxs-lookup"><span data-stu-id="6b802-153">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="6b802-154">**D3DTS \_ WORLDn**</span><span class="sxs-lookup"><span data-stu-id="6b802-154">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="6b802-155">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="6b802-155">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
