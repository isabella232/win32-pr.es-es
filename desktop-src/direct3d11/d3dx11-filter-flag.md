---
title: Enumeración D3DX11_FILTER_FLAG (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Marcas de filtrado de texturas.
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- Enumeración de D3DX11_FILTER_FLAG Direct3D 11
- LPD3DX11_FILTER_FLAG puntero de enumeración Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_FILTER_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2105970efb7f2ec07464d8a902df49d8f75bc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987222"
---
# <a name="d3dx11_filter_flag-enumeration"></a><span data-ttu-id="dfb67-106">\_Enumeración de marcas de filtro de D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="dfb67-106">D3DX11\_FILTER\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="dfb67-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="dfb67-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="dfb67-108">Marcas de filtrado de texturas.</span><span class="sxs-lookup"><span data-stu-id="dfb67-108">Texture filtering flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb67-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfb67-109">Syntax</span></span>


```C++
typedef enum D3DX11_FILTER_FLAG { 
  D3DX11_FILTER_NONE              = (1 << 0),
  D3DX11_FILTER_POINT             = (2 << 0),
  D3DX11_FILTER_LINEAR            = (3 << 0),
  D3DX11_FILTER_TRIANGLE          = (4 << 0),
  D3DX11_FILTER_BOX               = (5 << 0),
  D3DX11_FILTER_MIRROR_U          = (1 << 16),
  D3DX11_FILTER_MIRROR_V          = (2 << 16),
  D3DX11_FILTER_MIRROR_W          = (4 << 16),
  D3DX11_FILTER_MIRROR            = (7 << 16),
  D3DX11_FILTER_DITHER            = (1 << 19),
  D3DX11_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX11_FILTER_SRGB_IN           = (1 << 21),
  D3DX11_FILTER_SRGB_OUT          = (2 << 21),
  D3DX11_FILTER_SRGB              = (3 << 21)
} D3DX11_FILTER_FLAG, *LPD3DX11_FILTER_FLAG;
```



## <a name="constants"></a><span data-ttu-id="dfb67-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="dfb67-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dfb67-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11 \_ filtro \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="dfb67-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11\_FILTER\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-112">No se llevará a cabo ningún ajuste de escala o filtro.</span><span class="sxs-lookup"><span data-stu-id="dfb67-112">No scaling or filtering will take place.</span></span> <span data-ttu-id="dfb67-113">Se supone que los píxeles que están fuera de los límites de la imagen de origen son negros transparentes.</span><span class="sxs-lookup"><span data-stu-id="dfb67-113">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**D3DX11 \_ punto de filtro \_**</span><span class="sxs-lookup"><span data-stu-id="dfb67-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**D3DX11\_FILTER\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-115">Cada píxel de destino se calcula mediante el muestreo del píxel más cercano de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="dfb67-115">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**\_Filtro \_ lineal de D3DX11**</span><span class="sxs-lookup"><span data-stu-id="dfb67-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11\_FILTER\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-117">Cada píxel de destino se calcula mediante el muestreo de los cuatro píxeles más cercanos de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="dfb67-117">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="dfb67-118">Este filtro funciona mejor cuando la escala en ambos ejes es menor que dos.</span><span class="sxs-lookup"><span data-stu-id="dfb67-118">This filter works best when the scale on both axes is less than two.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**\_Triángulo de filtro de D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="dfb67-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**D3DX11\_FILTER\_TRIANGLE**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-120">Cada píxel de la imagen de origen contribuye igualmente a la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="dfb67-120">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="dfb67-121">Este es el más lento de los filtros.</span><span class="sxs-lookup"><span data-stu-id="dfb67-121">This is the slowest of the filters.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**\_Cuadro de filtro de D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="dfb67-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**D3DX11\_FILTER\_BOX**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-123">Cada píxel se calcula calculando el promedio de un cuadro 2x2 (x2) de píxeles de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="dfb67-123">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="dfb67-124">Este filtro solo funciona cuando las dimensiones del destino son la mitad de las del origen, como sucede con los mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="dfb67-124">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11 \_ filtro de \_ reflejo \_ U**</span><span class="sxs-lookup"><span data-stu-id="dfb67-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11\_FILTER\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-126">Los píxeles que están fuera del borde de la textura en el eje u deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="dfb67-126">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11 \_ filtro de \_ reflejo \_ V**</span><span class="sxs-lookup"><span data-stu-id="dfb67-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11\_FILTER\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-128">Los píxeles que están fuera del borde de la textura en el eje v deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="dfb67-128">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**D3DX11 \_ filtro \_ reflejo \_ W**</span><span class="sxs-lookup"><span data-stu-id="dfb67-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**D3DX11\_FILTER\_MIRROR\_W**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-130">Los píxeles que están fuera del borde de la textura en el eje w deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="dfb67-130">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**D3DX11 \_ filtro \_ reflejado**</span><span class="sxs-lookup"><span data-stu-id="dfb67-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**D3DX11\_FILTER\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-132">La especificación de esta marca es la misma que la especificación de las marcas de la imagen reflejada del filtro de D3DX U, de la versión reflejada del filtro de d3dx \_ \_ \_ \_ \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dfb67-132">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**\_Trama de filtro de D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="dfb67-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**D3DX11\_FILTER\_DITHER**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-134">La imagen resultante debe ser interpolada mediante un algoritmo de tramado ordenado de 4x4.</span><span class="sxs-lookup"><span data-stu-id="dfb67-134">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span> <span data-ttu-id="dfb67-135">Esto sucede cuando se realiza la conversión de un formato a otro.</span><span class="sxs-lookup"><span data-stu-id="dfb67-135">This happens when converting from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**\_Difusión de \_ interpolación de filtro de D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="dfb67-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**D3DX11\_FILTER\_DITHER\_DIFFUSION**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-137">Se difumina la interpolación en la imagen al cambiar de un formato a otro.</span><span class="sxs-lookup"><span data-stu-id="dfb67-137">Do diffuse dithering on the image when changing from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11 \_ filtro \_ sRGB \_ en**</span><span class="sxs-lookup"><span data-stu-id="dfb67-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11\_FILTER\_SRGB\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-139">Los datos de entrada están en el espacio de colores RGB estándar (sRGB).</span><span class="sxs-lookup"><span data-stu-id="dfb67-139">Input data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="dfb67-140">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="dfb67-140">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ filtro \_ sRGB \_ out**</span><span class="sxs-lookup"><span data-stu-id="dfb67-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11\_FILTER\_SRGB\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-142">Los datos de salida están en el espacio de colores RGB estándar (sRGB).</span><span class="sxs-lookup"><span data-stu-id="dfb67-142">Output data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="dfb67-143">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="dfb67-143">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="dfb67-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11 \_ filtro \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="dfb67-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11\_FILTER\_SRGB**</span></span>
</dt> <dd>

<span data-ttu-id="dfb67-145">Igual que al especificar el \_ filtro de d3dx \_ sRGB \_ en el \| filtro de d3dx \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dfb67-145">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span> <span data-ttu-id="dfb67-146">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="dfb67-146">See remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfb67-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfb67-147">Remarks</span></span>

<span data-ttu-id="dfb67-148">D3DX11 realiza automáticamente la corrección gamma (para convertir los datos de color del espacio RGB al espacio RGB estándar) al cargar datos de textura.</span><span class="sxs-lookup"><span data-stu-id="dfb67-148">D3DX11 automatically performs gamma correction (to convert color data from RGB space to standard RGB space) when loading texture data.</span></span> <span data-ttu-id="dfb67-149">Esto se hace automáticamente por ejemplo cuando los datos RGB se cargan desde un archivo. png en una textura sRGB.</span><span class="sxs-lookup"><span data-stu-id="dfb67-149">This is automatically done for instance when RGB data is loaded from a .png file into an sRGB texture.</span></span> <span data-ttu-id="dfb67-150">Use las marcas de filtro SRGB para indicar si no es necesario convertir los datos en el espacio sRGB.</span><span class="sxs-lookup"><span data-stu-id="dfb67-150">Use the SRGB filter flags to indicate if the data does not need to be converted into sRGB space.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb67-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfb67-151">Requirements</span></span>



| <span data-ttu-id="dfb67-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfb67-152">Requirement</span></span> | <span data-ttu-id="dfb67-153">Value</span><span class="sxs-lookup"><span data-stu-id="dfb67-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb67-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dfb67-154">Header</span></span><br/> | <dl> <span data-ttu-id="dfb67-155"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfb67-155"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfb67-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfb67-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb67-157">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="dfb67-157">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





