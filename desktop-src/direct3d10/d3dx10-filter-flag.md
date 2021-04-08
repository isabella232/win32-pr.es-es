---
description: Marcas de filtrado de texturas.
ms.assetid: bc73d916-fe18-4b15-b507-7954e157ab9a
title: Enumeración D3DX10_FILTER_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FILTER_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f12842cd07c55c33509ecfbb56fc804a6fc3b7c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003942"
---
# <a name="d3dx10_filter_flag-enumeration"></a><span data-ttu-id="a028b-103">\_Enumeración de marcas de filtro de D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="a028b-103">D3DX10\_FILTER\_FLAG enumeration</span></span>

<span data-ttu-id="a028b-104">Marcas de filtrado de texturas.</span><span class="sxs-lookup"><span data-stu-id="a028b-104">Texture filtering flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="a028b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a028b-105">Syntax</span></span>


```C++
typedef enum D3DX10_FILTER_FLAG { 
  D3DX10_FILTER_NONE              = (1 << 0),
  D3DX10_FILTER_POINT             = (2 << 0),
  D3DX10_FILTER_LINEAR            = (3 << 0),
  D3DX10_FILTER_TRIANGLE          = (4 << 0),
  D3DX10_FILTER_BOX               = (5 << 0),
  D3DX10_FILTER_MIRROR_U          = (1 << 16),
  D3DX10_FILTER_MIRROR_V          = (2 << 16),
  D3DX10_FILTER_MIRROR_W          = (4 << 16),
  D3DX10_FILTER_MIRROR            = (7 << 16),
  D3DX10_FILTER_DITHER            = (1 << 19),
  D3DX10_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX10_FILTER_SRGB_IN           = (1 << 21),
  D3DX10_FILTER_SRGB_OUT          = (2 << 21),
  D3DX10_FILTER_SRGB              = (3 << 21)
} D3DX10_FILTER_FLAG, *LPD3DX10_FILTER_FLAG;
```



## <a name="constants"></a><span data-ttu-id="a028b-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="a028b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a028b-107"><span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3DX10 \_ filtro \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="a028b-107"><span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3DX10\_FILTER\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-108">No se llevará a cabo ningún ajuste de escala o filtro.</span><span class="sxs-lookup"><span data-stu-id="a028b-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="a028b-109">Se supone que los píxeles que están fuera de los límites de la imagen de origen son negros transparentes.</span><span class="sxs-lookup"><span data-stu-id="a028b-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-110"><span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**D3DX10 \_ punto de filtro \_**</span><span class="sxs-lookup"><span data-stu-id="a028b-110"><span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**D3DX10\_FILTER\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-111">Cada píxel de destino se calcula mediante el muestreo del píxel más cercano de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="a028b-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-112"><span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**\_Filtro \_ lineal de D3DX10**</span><span class="sxs-lookup"><span data-stu-id="a028b-112"><span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**D3DX10\_FILTER\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-113">Cada píxel de destino se calcula mediante el muestreo de los cuatro píxeles más cercanos de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="a028b-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="a028b-114">Este filtro funciona mejor cuando la escala en ambos ejes es menor que dos.</span><span class="sxs-lookup"><span data-stu-id="a028b-114">This filter works best when the scale on both axes is less than two.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-115"><span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**\_Triángulo de filtro de D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="a028b-115"><span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**D3DX10\_FILTER\_TRIANGLE**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-116">Cada píxel de la imagen de origen contribuye igualmente a la imagen de destino.</span><span class="sxs-lookup"><span data-stu-id="a028b-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="a028b-117">Este es el más lento de los filtros.</span><span class="sxs-lookup"><span data-stu-id="a028b-117">This is the slowest of the filters.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-118"><span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**\_Cuadro de filtro de D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="a028b-118"><span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**D3DX10\_FILTER\_BOX**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-119">Cada píxel se calcula calculando el promedio de un cuadro 2x2 (x2) de píxeles de la imagen de origen.</span><span class="sxs-lookup"><span data-stu-id="a028b-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="a028b-120">Este filtro solo funciona cuando las dimensiones del destino son la mitad de las del origen, como sucede con los mapas MIP.</span><span class="sxs-lookup"><span data-stu-id="a028b-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-121"><span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**D3DX10 \_ filtro de \_ reflejo \_ U**</span><span class="sxs-lookup"><span data-stu-id="a028b-121"><span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**D3DX10\_FILTER\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-122">Los píxeles que están fuera del borde de la textura en el eje u deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="a028b-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-123"><span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3DX10 \_ filtro de \_ reflejo \_ V**</span><span class="sxs-lookup"><span data-stu-id="a028b-123"><span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3DX10\_FILTER\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-124">Los píxeles que están fuera del borde de la textura en el eje v deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="a028b-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-125"><span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3DX10 \_ filtro \_ reflejo \_ W**</span><span class="sxs-lookup"><span data-stu-id="a028b-125"><span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3DX10\_FILTER\_MIRROR\_W**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-126">Los píxeles que están fuera del borde de la textura en el eje w deben reflejarse, no ajustarse.</span><span class="sxs-lookup"><span data-stu-id="a028b-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-127"><span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**D3DX10 \_ filtro \_ reflejado**</span><span class="sxs-lookup"><span data-stu-id="a028b-127"><span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**D3DX10\_FILTER\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-128">La especificación de esta marca es la misma que la especificación de las marcas de la imagen reflejada del filtro de D3DX U, de la versión reflejada del filtro de d3dx \_ \_ \_ \_ \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a028b-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-129"><span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**\_Trama de filtro de D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="a028b-129"><span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**D3DX10\_FILTER\_DITHER**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-130">La imagen resultante debe ser interpolada mediante un algoritmo de tramado ordenado de 4x4.</span><span class="sxs-lookup"><span data-stu-id="a028b-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span> <span data-ttu-id="a028b-131">Esto sucede cuando se realiza la conversión de un formato a otro.</span><span class="sxs-lookup"><span data-stu-id="a028b-131">This happens when converting from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-132"><span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**\_Difusión de \_ interpolación de filtro de D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="a028b-132"><span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**D3DX10\_FILTER\_DITHER\_DIFFUSION**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-133">Se difumina la interpolación en la imagen al cambiar de un formato a otro.</span><span class="sxs-lookup"><span data-stu-id="a028b-133">Do diffuse dithering on the image when changing from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-134"><span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10 \_ filtro \_ sRGB \_ en**</span><span class="sxs-lookup"><span data-stu-id="a028b-134"><span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10\_FILTER\_SRGB\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-135">Los datos de entrada están en el espacio de colores RGB estándar (sRGB).</span><span class="sxs-lookup"><span data-stu-id="a028b-135">Input data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="a028b-136">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="a028b-136">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-137"><span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10 \_ filtro \_ sRGB \_ out**</span><span class="sxs-lookup"><span data-stu-id="a028b-137"><span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10\_FILTER\_SRGB\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-138">Los datos de salida están en el espacio de colores RGB estándar (sRGB).</span><span class="sxs-lookup"><span data-stu-id="a028b-138">Output data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="a028b-139">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="a028b-139">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a028b-140"><span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10 \_ filtro \_ sRGB**</span><span class="sxs-lookup"><span data-stu-id="a028b-140"><span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10\_FILTER\_SRGB**</span></span>
</dt> <dd>

<span data-ttu-id="a028b-141">Igual que al especificar el \_ filtro de d3dx \_ sRGB \_ en el \| filtro de d3dx \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a028b-141">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span> <span data-ttu-id="a028b-142">Vea Notas.</span><span class="sxs-lookup"><span data-stu-id="a028b-142">See remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a028b-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a028b-143">Remarks</span></span>

<span data-ttu-id="a028b-144">D3DX10 realiza automáticamente la corrección gamma (para convertir los datos de color del espacio RGB al espacio RGB estándar) al cargar datos de textura.</span><span class="sxs-lookup"><span data-stu-id="a028b-144">D3DX10 automatically performs gamma correction (to convert color data from RGB space to standard RGB space) when loading texture data.</span></span> <span data-ttu-id="a028b-145">Esto se hace automáticamente por ejemplo cuando los datos RGB se cargan desde un archivo. png en una textura sRGB.</span><span class="sxs-lookup"><span data-stu-id="a028b-145">This is automatically done for instance when RGB data is loaded from a .png file into an sRGB texture.</span></span> <span data-ttu-id="a028b-146">Use las marcas de filtro SRGB para indicar si no es necesario convertir los datos en el espacio sRGB.</span><span class="sxs-lookup"><span data-stu-id="a028b-146">Use the SRGB filter flags to indicate if the data does not need to be converted into sRGB space.</span></span>

## <a name="requirements"></a><span data-ttu-id="a028b-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a028b-147">Requirements</span></span>



| <span data-ttu-id="a028b-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="a028b-148">Requirement</span></span> | <span data-ttu-id="a028b-149">Value</span><span class="sxs-lookup"><span data-stu-id="a028b-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a028b-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a028b-150">Header</span></span><br/> | <dl> <span data-ttu-id="a028b-151"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a028b-151"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a028b-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="a028b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a028b-153">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="a028b-153">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




