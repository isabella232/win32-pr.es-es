---
description: Marcas de filtrado de textura.
ms.assetid: bc73d916-fe18-4b15-b507-7954e157ab9a
title: D3DX10_FILTER_FLAG enumeración (D3DX10Tex.h)
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
ms.openlocfilehash: 400347efde28133055b97016d877b1bd4148624387ddd7086f4ff185ab87cca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989535"
---
# <a name="d3dx10_filter_flag-enumeration"></a>Enumeración D3DX10 \_ FILTER \_ FLAG

Marcas de filtrado de textura.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3DX10 \_ FILTER \_ NONE**
</dt> <dd>

No se realizará ningún escalado ni filtrado. Se supone que los píxeles fuera de los límites de la imagen de origen son de color negro transparente.

</dd> <dt>

<span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**PUNTO DE FILTRO D3DX10 \_ \_**
</dt> <dd>

Cada píxel de destino se calcula mediante el muestreo del píxel más cercano de la imagen de origen.

</dd> <dt>

<span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**D3DX10 \_ FILTER \_ LINEAR**
</dt> <dd>

Cada píxel de destino se calcula mediante el muestreo de los cuatro píxeles más cercanos de la imagen de origen. Este filtro funciona mejor cuando la escala en ambos ejes es menor que dos.

</dd> <dt>

<span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**TRIÁNGULO DE FILTRO D3DX10 \_ \_**
</dt> <dd>

Cada píxel de la imagen de origen contribuye igualmente a la imagen de destino. Este es el más lento de los filtros.

</dd> <dt>

<span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**CUADRO DE FILTRO D3DX10 \_ \_**
</dt> <dd>

Cada píxel se calcula calculando el promedio de un cuadro de 2 x 2(x2) de píxeles a partir de la imagen de origen. Este filtro solo funciona cuando las dimensiones del destino son la mitad de las del origen, como es el caso de los mapas mip.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**REFLEJO DEL FILTRO D3DX10 \_ \_ \_ U**
</dt> <dd>

Los píxeles del borde de la textura en el eje u deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3DX10 \_ FILTER \_ MIRROR \_ V**
</dt> <dd>

Los píxeles del borde de la textura en el eje v deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3DX10 \_ FILTER \_ MIRROR \_ W**
</dt> <dd>

Los píxeles del borde de la textura en el eje w deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**REFLEJO DEL FILTRO D3DX10 \_ \_**
</dt> <dd>

Especificar esta marca es lo mismo que especificar las marcas D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V y \_ \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.

</dd> <dt>

<span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**D3DX10 \_ FILTER \_ DITHER**
</dt> <dd>

La imagen resultante debe estar entrelazada mediante un algoritmo de dither ordenado de 4x4. Esto sucede cuando se convierte de un formato a otro.

</dd> <dt>

<span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**D3DX10 \_ FILTER \_ DITHER \_ ESTADÍA**
</dt> <dd>

Realice un difuso en la imagen al cambiar de un formato a otro.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**FILTRO D3DX10 \_ \_ SRGB \_ IN**
</dt> <dd>

Los datos de entrada están en un espacio de colores RGB (sRGB) estándar. Vea Notas.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10 \_ FILTER \_ SRGB \_ OUT**
</dt> <dd>

Los datos de salida están en un espacio de colores RGB (sRGB) estándar. Vea Notas.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10 \_ FILTER \_ SRGB**
</dt> <dd>

Igual que especificar D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT. Vea Notas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

D3DX10 realiza automáticamente la corrección gamma (para convertir los datos de color del espacio RGB al espacio RGB estándar) al cargar los datos de textura. Esto se hace automáticamente por ejemplo cuando se cargan datos RGB desde un archivo .png en una textura sRGB. Use las marcas de filtro SRGB para indicar si no es necesario convertir los datos en espacio sRGB.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




