---
title: D3DX11_FILTER_FLAG enumeración (D3DX11tex.h)
description: 'Nota: La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Marcas de filtrado de textura.'
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- D3DX11_FILTER_FLAG enumeración Direct3D 11
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
ms.openlocfilehash: b02ddbf1785d1032ab28a990d022950b2f28acc4b032ecdc9a72d5704665c03b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118537006"
---
# <a name="d3dx11_filter_flag-enumeration"></a>D3DX11 \_ FILTER \_ FLAG (enumeración)

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Marcas de filtrado de textura.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11 \_ FILTER \_ NONE**
</dt> <dd>

No se realizará ningún escalado ni filtrado. Se supone que los píxeles fuera de los límites de la imagen de origen son de color negro transparente.

</dd> <dt>

<span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**PUNTO DE FILTRO D3DX11 \_ \_**
</dt> <dd>

Cada píxel de destino se calcula mediante el muestreo del píxel más cercano de la imagen de origen.

</dd> <dt>

<span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11 \_ FILTER \_ LINEAR**
</dt> <dd>

Cada píxel de destino se calcula mediante el muestreo de los cuatro píxeles más cercanos de la imagen de origen. Este filtro funciona mejor cuando la escala en ambos ejes es menor que dos.

</dd> <dt>

<span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**TRIÁNGULO DE FILTRO D3DX11 \_ \_**
</dt> <dd>

Cada píxel de la imagen de origen contribuye igualmente a la imagen de destino. Este es el más lento de los filtros.

</dd> <dt>

<span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**CUADRO DE FILTRO D3DX11 \_ \_**
</dt> <dd>

Cada píxel se calcula calcula calculando un promedio de un cuadro de 2 x 2 (x2) de píxeles de la imagen de origen. Este filtro solo funciona cuando las dimensiones del destino son la mitad de las del origen, como es el caso de los mapas mip.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11 \_ FILTRO \_ REFLEJADO \_ U**
</dt> <dd>

Los píxeles del borde de la textura en el eje U deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11 \_ FILTER \_ MIRROR \_ V**
</dt> <dd>

Los píxeles del borde de la textura en el eje v deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**REFLEJO DEL FILTRO D3DX11 \_ \_ \_ W**
</dt> <dd>

Los píxeles del borde de la textura en el eje w deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**REFLEJO DEL FILTRO D3DX11 \_ \_**
</dt> <dd>

Especificar esta marca es igual que especificar las marcas D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR V y \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**D3DX11 \_ FILTER \_ DITHER**
</dt> <dd>

La imagen resultante debe estar entrelazada mediante un algoritmo de dither ordenado de 4x4. Esto sucede cuando se convierte de un formato a otro.

</dd> <dt>

<span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**D3DX11 \_ FILTER \_ DITHER LO QUE SE HA \_ FILTRADO**
</dt> <dd>

Realice el dithering difuso en la imagen al cambiar de un formato a otro.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**FILTRO D3DX11 \_ \_ SRGB \_ IN**
</dt> <dd>

Los datos de entrada están en un espacio de colores RGB (sRGB) estándar. Vea Notas.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**FILTRO D3DX11 \_ \_ SRGB \_ OUT**
</dt> <dd>

Los datos de salida están en un espacio de colores RGB (sRGB) estándar. Vea Notas.

</dd> <dt>

<span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**FILTRO D3DX11 \_ \_ SRGB**
</dt> <dd>

Igual que especificar D3DX \_ FILTER \_ SRGB \_ IN \| D3DX \_ FILTER \_ SRGB \_ OUT. Vea Notas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

D3DX11 realiza automáticamente la corrección gamma (para convertir datos de color del espacio RGB al espacio RGB estándar) al cargar datos de textura. Esto se hace automáticamente por ejemplo cuando se cargan datos RGB desde un archivo .png en una textura sRGB. Use las marcas de filtro SRGB para indicar si no es necesario convertir los datos en espacio sRGB.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





