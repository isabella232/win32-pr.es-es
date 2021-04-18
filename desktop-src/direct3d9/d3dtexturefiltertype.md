---
description: Define los modos de filtrado de textura para una fase de textura.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Enumeración D3DTEXTUREFILTERTYPE (D3D9Types. h)
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
ms.openlocfilehash: 212fd05755ebf554c3c57e7ac45dcf8947f2d753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717631"
---
# <a name="d3dtexturefiltertype-enumeration"></a><span data-ttu-id="e85c7-103">Enumeración D3DTEXTUREFILTERTYPE</span><span class="sxs-lookup"><span data-stu-id="e85c7-103">D3DTEXTUREFILTERTYPE enumeration</span></span>

<span data-ttu-id="e85c7-104">Define los modos de filtrado de textura para una fase de textura.</span><span class="sxs-lookup"><span data-stu-id="e85c7-104">Defines texture filtering modes for a texture stage.</span></span>

## <a name="syntax"></a><span data-ttu-id="e85c7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e85c7-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="e85c7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e85c7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e85c7-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="e85c7-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="e85c7-108">Cuando se usa con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md), deshabilita mipmapping.</span><span class="sxs-lookup"><span data-stu-id="e85c7-108">When used with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md), disables mipmapping.</span></span>

</dd> <dt>

<span data-ttu-id="e85c7-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**\_Punto D3DTEXF**</span><span class="sxs-lookup"><span data-stu-id="e85c7-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="e85c7-110">Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que el filtrado de puntos se va a usar como filtro de aumento de textura o minificación, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e85c7-110">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that point filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="e85c7-111">Cuando se usa con **D3DSAMP \_ MIPFILTER**, habilita mipmapping y especifica que el rasterizador elige el color del textura del nivel de MIP más próximo.</span><span class="sxs-lookup"><span data-stu-id="e85c7-111">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and specifies that the rasterizer chooses the color from the texel of the nearest mip level.</span></span>

</dd> <dt>

<span data-ttu-id="e85c7-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**\_Lineal D3DTEXF**</span><span class="sxs-lookup"><span data-stu-id="e85c7-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="e85c7-113">Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que el filtrado lineal se va a usar como filtro de aumento de textura o minificación, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e85c7-113">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that linear filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="e85c7-114">Cuando se usa con **D3DSAMP \_ MIPFILTER**, habilita el filtrado de mipmapping y trilineal; especifica que el rasterizador se interpola entre los dos niveles de MIP más cercanos.</span><span class="sxs-lookup"><span data-stu-id="e85c7-114">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and trilinear filtering; it specifies that the rasterizer interpolates between the two nearest mip levels.</span></span>

</dd> <dt>

<span data-ttu-id="e85c7-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ anisotrópico**</span><span class="sxs-lookup"><span data-stu-id="e85c7-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF\_ANISOTROPIC**</span></span>
</dt> <dd>

<span data-ttu-id="e85c7-116">Cuando se usa con [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) o [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), especifica que el filtrado de texturas anisotrópico se usa como filtro de aumento de textura o minificación, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e85c7-116">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that anisotropic texture filtering used as a texture magnification or minification filter respectively.</span></span> <span data-ttu-id="e85c7-117">Compensa la distorsión causada por la diferencia en el ángulo entre el polígono de textura y el plano de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="e85c7-117">Compensates for distortion caused by the difference in angle between the texture polygon and the plane of the screen.</span></span> <span data-ttu-id="e85c7-118">El uso con **D3DSAMP \_ MIPFILTER** es indefinido.</span><span class="sxs-lookup"><span data-stu-id="e85c7-118">Use with **D3DSAMP\_MIPFILTER** is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="e85c7-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**</span><span class="sxs-lookup"><span data-stu-id="e85c7-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF\_PYRAMIDALQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="e85c7-120">Un filtro de carpa de ejemplo 4 usado como filtro de aumento de textura o minificación.</span><span class="sxs-lookup"><span data-stu-id="e85c7-120">A 4-sample tent filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="e85c7-121">El uso con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) es indefinido.</span><span class="sxs-lookup"><span data-stu-id="e85c7-121">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="e85c7-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**</span><span class="sxs-lookup"><span data-stu-id="e85c7-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF\_GAUSSIANQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="e85c7-123">Un filtro gaussiano de 4 muestras usado como filtro de aumento de textura o minificación.</span><span class="sxs-lookup"><span data-stu-id="e85c7-123">A 4-sample Gaussian filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="e85c7-124">El uso con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) es indefinido.</span><span class="sxs-lookup"><span data-stu-id="e85c7-124">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="e85c7-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**</span><span class="sxs-lookup"><span data-stu-id="e85c7-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF\_CONVOLUTIONMONO**</span></span>
</dt> <dd>

<span data-ttu-id="e85c7-126">Filtro de circunvolución para texturas monocromas.</span><span class="sxs-lookup"><span data-stu-id="e85c7-126">Convolution filter for monochrome textures.</span></span> <span data-ttu-id="e85c7-127">Consulte [D3DFMT \_ a1](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="e85c7-127">See [D3DFMT\_A1](d3dformat.md).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e85c7-128">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="e85c7-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="e85c7-129">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="e85c7-129">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

<span data-ttu-id="e85c7-130">El uso con [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) es indefinido.</span><span class="sxs-lookup"><span data-stu-id="e85c7-130">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="e85c7-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e85c7-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="e85c7-132">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="e85c7-132">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="e85c7-133">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e85c7-133">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="e85c7-134">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e85c7-134">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e85c7-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e85c7-135">Remarks</span></span>

<span data-ttu-id="e85c7-136">[**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) usa D3DTEXTUREFILTERTYPE junto con [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) para definir los modos de filtrado de textura para una fase de textura.</span><span class="sxs-lookup"><span data-stu-id="e85c7-136">D3DTEXTUREFILTERTYPE is used by [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) along with [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) to define texture filtering modes for a texture stage.</span></span>

<span data-ttu-id="e85c7-137">Para comprobar si un formato admite tipos de filtro de textura distintos \_ del punto D3DTEXF (que siempre se admite), llame a [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) con el \_ filtro de consulta D3DUSAGE \_ .</span><span class="sxs-lookup"><span data-stu-id="e85c7-137">To check if a format supports texture filter types other than D3DTEXF\_POINT (which is always supported), call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_FILTER.</span></span>

<span data-ttu-id="e85c7-138">Establezca el filtro de ampliación de una fase de textura mediante una llamada a [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el \_ valor MAGFILTER de D3DSAMP como segundo parámetro y un miembro de esta enumeración como el tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="e85c7-138">Set a texture stage's magnification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MAGFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="e85c7-139">Establezca el filtro minificación de una fase de textura mediante una llamada a [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el \_ valor D3DSAMP MINFILTER como segundo parámetro y un miembro de esta enumeración como el tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="e85c7-139">Set a texture stage's minification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MINFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="e85c7-140">Establezca el filtro de textura para que use los niveles entre-MIP mediante una llamada a [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) con el \_ valor MIPFILTER de D3DSAMP como el segundo parámetro y un miembro de esta enumeración como el tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="e85c7-140">Set the texture filter to use between-mipmap levels by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MIPFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="e85c7-141">No todos los modos de filtrado válidos para un dispositivo se aplicarán a las asignaciones de volumen.</span><span class="sxs-lookup"><span data-stu-id="e85c7-141">Not all valid filtering modes for a device will apply to volume maps.</span></span> <span data-ttu-id="e85c7-142">En general, se \_ \_ admitirán los filtros de ampliación lineal D3DTEXF Point y D3DTEXF para los mapas de volumen.</span><span class="sxs-lookup"><span data-stu-id="e85c7-142">In general, D3DTEXF\_POINT and D3DTEXF\_LINEAR magnification filters will be supported for volume maps.</span></span> <span data-ttu-id="e85c7-143">Si \_ se establece D3DPTEXTURECAPS MIPVOLUMEMAP, se \_ admitirán los filtros de mapa MIP del punto D3DTEXF y \_ de D3DTEXF y D3DTEXF \_ lineal minificación para los mapas de volumen.</span><span class="sxs-lookup"><span data-stu-id="e85c7-143">If D3DPTEXTURECAPS\_MIPVOLUMEMAP is set, then the D3DTEXF\_POINT mipmap filter and D3DTEXF\_POINT and D3DTEXF\_LINEAR minification filters will be supported for volume maps.</span></span> <span data-ttu-id="e85c7-144">El dispositivo puede o no admitir el \_ filtro de mipmap lineal D3DTEXF para mapas de volumen.</span><span class="sxs-lookup"><span data-stu-id="e85c7-144">The device may or may not support the D3DTEXF\_LINEAR mipmap filter for volume maps.</span></span> <span data-ttu-id="e85c7-145">Los dispositivos que admiten el filtrado anisotrópico para asignaciones 2D no admiten necesariamente el filtrado anisotrópico para mapas de volumen.</span><span class="sxs-lookup"><span data-stu-id="e85c7-145">Devices that support anisotropic filtering for 2D maps do not necessarily support anisotropic filtering for volume maps.</span></span> <span data-ttu-id="e85c7-146">Sin embargo, las aplicaciones que permiten el filtrado anisotrópico recibirán el mejor filtrado disponible (probablemente lineal) si no se admite el filtrado anisotrópico.</span><span class="sxs-lookup"><span data-stu-id="e85c7-146">However, applications that enable anisotropic filtering will receive the best available filtering (probably linear) if anisotropic filtering is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="e85c7-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e85c7-147">Requirements</span></span>



| <span data-ttu-id="e85c7-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="e85c7-148">Requirement</span></span> | <span data-ttu-id="e85c7-149">Value</span><span class="sxs-lookup"><span data-stu-id="e85c7-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e85c7-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e85c7-150">Header</span></span><br/> | <dl> <span data-ttu-id="e85c7-151"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e85c7-151"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e85c7-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="e85c7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e85c7-153">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="e85c7-153">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="e85c7-154">**ID3DXPatchMesh::GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="e85c7-154">**ID3DXPatchMesh::GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="e85c7-155">**ID3DXPatchMesh::SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="e85c7-155">**ID3DXPatchMesh::SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="e85c7-156">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="e85c7-156">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> <dt>

[<span data-ttu-id="e85c7-157">**IDirect3DDevice9::SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="e85c7-157">**IDirect3DDevice9::SetSamplerState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
