---
description: Define los modos de filtrado de textura para una fase de textura.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Enumeración D3DTEXTUREFILTERTYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bd6038e1b3d2b2f85e5766605583db9879427343
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343010"
---
# <a name="d3dtexturefiltertype-enumeration"></a><span data-ttu-id="bc554-103">D3DTEXTUREFILTERTYPE (enumeración)</span><span class="sxs-lookup"><span data-stu-id="bc554-103">D3DTEXTUREFILTERTYPE enumeration</span></span>

<span data-ttu-id="bc554-104">Define los modos de filtrado de textura para una fase de textura.</span><span class="sxs-lookup"><span data-stu-id="bc554-104">Defines texture filtering modes for a texture stage.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc554-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc554-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a><span data-ttu-id="bc554-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="bc554-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bc554-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ NONE**</span><span class="sxs-lookup"><span data-stu-id="bc554-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="bc554-108">Cuando se usa [**con \_ MIPFILTER de D3DSAMP,**](./d3dsamplerstatetype.md)deshabilita mipmapping.</span><span class="sxs-lookup"><span data-stu-id="bc554-108">When used with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md), disables mipmapping.</span></span>

</dd> <dt>

<span data-ttu-id="bc554-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF \_ POINT**</span><span class="sxs-lookup"><span data-stu-id="bc554-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="bc554-110">Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)especifica que el filtrado de puntos se usará como filtro de ampliación de textura o minificación, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bc554-110">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that point filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="bc554-111">Cuando se usa con **\_ MIPFILTER de D3DSAMP,** habilita mipmapping y especifica que el rasterizador elige el color del texel del nivel de mip más cercano.</span><span class="sxs-lookup"><span data-stu-id="bc554-111">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and specifies that the rasterizer chooses the color from the texel of the nearest mip level.</span></span>

</dd> <dt>

<span data-ttu-id="bc554-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ LINEAR**</span><span class="sxs-lookup"><span data-stu-id="bc554-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="bc554-113">Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)especifica que el filtrado lineal se usará como filtro de ampliación o minificación de textura, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bc554-113">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that linear filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="bc554-114">Cuando se usa con **\_ MIPFILTER de D3DSAMP,** habilita el filtrado de mipmapping y trilinear; especifica que el rasterizador se interpola entre los dos niveles de mip más cercanos.</span><span class="sxs-lookup"><span data-stu-id="bc554-114">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and trilinear filtering; it specifies that the rasterizer interpolates between the two nearest mip levels.</span></span>

</dd> <dt>

<span data-ttu-id="bc554-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ ANISOTROPIC**</span><span class="sxs-lookup"><span data-stu-id="bc554-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF\_ANISOTROPIC**</span></span>
</dt> <dd>

<span data-ttu-id="bc554-116">Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER,**](./d3dsamplerstatetype.md)especifica que el filtrado de textura anisotropica se usa como filtro de ampliación o minificación de textura, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bc554-116">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that anisotropic texture filtering used as a texture magnification or minification filter respectively.</span></span> <span data-ttu-id="bc554-117">Compensa la distorsión causada por la diferencia de ángulo entre el polígono de textura y el plano de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="bc554-117">Compensates for distortion caused by the difference in angle between the texture polygon and the plane of the screen.</span></span> <span data-ttu-id="bc554-118">El uso **con \_ MIPFILTER de D3DSAMP** no está definido.</span><span class="sxs-lookup"><span data-stu-id="bc554-118">Use with **D3DSAMP\_MIPFILTER** is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="bc554-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**</span><span class="sxs-lookup"><span data-stu-id="bc554-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF\_PYRAMIDALQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="bc554-120">Filtro de tienda de 4 muestras que se usa como filtro de ampliación o minificación de textura.</span><span class="sxs-lookup"><span data-stu-id="bc554-120">A 4-sample tent filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="bc554-121">El uso [**con \_ MIPFILTER de D3DSAMP**](./d3dsamplerstatetype.md) no está definido.</span><span class="sxs-lookup"><span data-stu-id="bc554-121">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="bc554-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**</span><span class="sxs-lookup"><span data-stu-id="bc554-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF\_GAUSSIANQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="bc554-123">Filtro gaussiano de 4 muestras que se usa como filtro de ampliación o minificación de textura.</span><span class="sxs-lookup"><span data-stu-id="bc554-123">A 4-sample Gaussian filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="bc554-124">El uso [**con \_ MIPFILTER de D3DSAMP**](./d3dsamplerstatetype.md) no está definido.</span><span class="sxs-lookup"><span data-stu-id="bc554-124">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="bc554-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**</span><span class="sxs-lookup"><span data-stu-id="bc554-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF\_CONVOLUTIONMONO**</span></span>
</dt> <dd>

<span data-ttu-id="bc554-126">Filtro de convolución para texturas monocromáticas.</span><span class="sxs-lookup"><span data-stu-id="bc554-126">Convolution filter for monochrome textures.</span></span> <span data-ttu-id="bc554-127">Vea [D3DFMT \_ A1.](d3dformat.md)</span><span class="sxs-lookup"><span data-stu-id="bc554-127">See [D3DFMT\_A1](d3dformat.md).</span></span>

<span data-ttu-id="bc554-128">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="bc554-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="bc554-129">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="bc554-129">This flag is available in Direct3D 9Ex only.</span></span>



 

<span data-ttu-id="bc554-130">El uso [**con \_ MIPFILTER de D3DSAMP**](./d3dsamplerstatetype.md) no está definido.</span><span class="sxs-lookup"><span data-stu-id="bc554-130">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="bc554-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bc554-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="bc554-132">Fuerza esta enumeración a compilar hasta 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="bc554-132">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="bc554-133">Sin este valor, algunos compiladores permitirían que esta enumeración se compilase a un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bc554-133">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="bc554-134">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="bc554-134">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bc554-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bc554-135">Remarks</span></span>

<span data-ttu-id="bc554-136">[**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) usa D3DTEXTUREFILTERTYPE junto con [**D3DSAMPLERSTATETYPE para**](./d3dsamplerstatetype.md) definir modos de filtrado de textura para una fase de textura.</span><span class="sxs-lookup"><span data-stu-id="bc554-136">D3DTEXTUREFILTERTYPE is used by [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) along with [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) to define texture filtering modes for a texture stage.</span></span>

<span data-ttu-id="bc554-137">Para comprobar si un formato admite tipos de filtro de textura distintos de D3DTEXF POINT (que siempre se admite), llame a \_ [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con D3DUSAGE \_ QUERY \_ FILTER.</span><span class="sxs-lookup"><span data-stu-id="bc554-137">To check if a format supports texture filter types other than D3DTEXF\_POINT (which is always supported), call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_FILTER.</span></span>

<span data-ttu-id="bc554-138">Establezca el filtro de ampliación de una fase de textura llamando a [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el valor MAGFILTER de D3DSAMP como segundo parámetro y un miembro de esta enumeración como tercer \_ parámetro.</span><span class="sxs-lookup"><span data-stu-id="bc554-138">Set a texture stage's magnification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MAGFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="bc554-139">Establezca el filtro de minificación de una fase de textura llamando a [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el valor MINFILTER de D3DSAMP como segundo parámetro y un miembro de esta enumeración como tercer \_ parámetro.</span><span class="sxs-lookup"><span data-stu-id="bc554-139">Set a texture stage's minification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MINFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="bc554-140">Establezca el filtro de textura para usar entre niveles mipmap mediante una llamada a [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el valor MIPFILTER de D3DSAMP como segundo parámetro y un miembro de esta enumeración como tercer \_ parámetro.</span><span class="sxs-lookup"><span data-stu-id="bc554-140">Set the texture filter to use between-mipmap levels by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MIPFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="bc554-141">No todos los modos de filtrado válidos para un dispositivo se aplicarán a los mapas de volumen.</span><span class="sxs-lookup"><span data-stu-id="bc554-141">Not all valid filtering modes for a device will apply to volume maps.</span></span> <span data-ttu-id="bc554-142">En general, se admiten los filtros de ampliación LINEAR D3DTEXF POINT y \_ D3DTEXF \_ para mapas de volúmenes.</span><span class="sxs-lookup"><span data-stu-id="bc554-142">In general, D3DTEXF\_POINT and D3DTEXF\_LINEAR magnification filters will be supported for volume maps.</span></span> <span data-ttu-id="bc554-143">Si se establece D3DPTEXTURECAPS MIPVOLUMEMAP, se admiten los filtros \_ mipmap D3DTEXF \_ POINT y D3DTEXF POINT y \_ D3DTEXF LINEAR para mapas de \_ volumen.</span><span class="sxs-lookup"><span data-stu-id="bc554-143">If D3DPTEXTURECAPS\_MIPVOLUMEMAP is set, then the D3DTEXF\_POINT mipmap filter and D3DTEXF\_POINT and D3DTEXF\_LINEAR minification filters will be supported for volume maps.</span></span> <span data-ttu-id="bc554-144">El dispositivo puede admitir o no el filtro mipmap LINEAR de D3DTEXF para \_ mapas de volumen.</span><span class="sxs-lookup"><span data-stu-id="bc554-144">The device may or may not support the D3DTEXF\_LINEAR mipmap filter for volume maps.</span></span> <span data-ttu-id="bc554-145">Los dispositivos que admiten el filtrado anisotropico para mapas 2D no admiten necesariamente el filtrado anisotropo para mapas de volumen.</span><span class="sxs-lookup"><span data-stu-id="bc554-145">Devices that support anisotropic filtering for 2D maps do not necessarily support anisotropic filtering for volume maps.</span></span> <span data-ttu-id="bc554-146">Sin embargo, las aplicaciones que habilitan el filtrado anisotropico recibirán el mejor filtrado disponible (probablemente lineal) si no se admite el filtrado anisotropico.</span><span class="sxs-lookup"><span data-stu-id="bc554-146">However, applications that enable anisotropic filtering will receive the best available filtering (probably linear) if anisotropic filtering is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc554-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc554-147">Requirements</span></span>



| <span data-ttu-id="bc554-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc554-148">Requirement</span></span> | <span data-ttu-id="bc554-149">Value</span><span class="sxs-lookup"><span data-stu-id="bc554-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc554-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc554-150">Header</span></span><br/> | <dl> <span data-ttu-id="bc554-151"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="bc554-151"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc554-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc554-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc554-153">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="bc554-153">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="bc554-154">**ID3DXPatchMesh::GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="bc554-154">**ID3DXPatchMesh::GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="bc554-155">**ID3DXPatchMesh::SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="bc554-155">**ID3DXPatchMesh::SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="bc554-156">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="bc554-156">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> <dt>

[<span data-ttu-id="bc554-157">**IDirect3DDevice9::SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="bc554-157">**IDirect3DDevice9::SetSamplerState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
