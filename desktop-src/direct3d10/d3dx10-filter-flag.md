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
# <a name="d3dx10_filter_flag-enumeration"></a>\_Enumeración de marcas de filtro de D3DX10 \_

Marcas de filtrado de texturas.

## <a name="syntax"></a>Sintaxis


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

<span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3DX10 \_ filtro \_ ninguno**
</dt> <dd>

No se llevará a cabo ningún ajuste de escala o filtro. Se supone que los píxeles que están fuera de los límites de la imagen de origen son negros transparentes.

</dd> <dt>

<span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**D3DX10 \_ punto de filtro \_**
</dt> <dd>

Cada píxel de destino se calcula mediante el muestreo del píxel más cercano de la imagen de origen.

</dd> <dt>

<span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**\_Filtro \_ lineal de D3DX10**
</dt> <dd>

Cada píxel de destino se calcula mediante el muestreo de los cuatro píxeles más cercanos de la imagen de origen. Este filtro funciona mejor cuando la escala en ambos ejes es menor que dos.

</dd> <dt>

<span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**\_Triángulo de filtro de D3DX10 \_**
</dt> <dd>

Cada píxel de la imagen de origen contribuye igualmente a la imagen de destino. Este es el más lento de los filtros.

</dd> <dt>

<span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**\_Cuadro de filtro de D3DX10 \_**
</dt> <dd>

Cada píxel se calcula calculando el promedio de un cuadro 2x2 (x2) de píxeles de la imagen de origen. Este filtro solo funciona cuando las dimensiones del destino son la mitad de las del origen, como sucede con los mapas MIP.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**D3DX10 \_ filtro de \_ reflejo \_ U**
</dt> <dd>

Los píxeles que están fuera del borde de la textura en el eje u deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3DX10 \_ filtro de \_ reflejo \_ V**
</dt> <dd>

Los píxeles que están fuera del borde de la textura en el eje v deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3DX10 \_ filtro \_ reflejo \_ W**
</dt> <dd>

Los píxeles que están fuera del borde de la textura en el eje w deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**D3DX10 \_ filtro \_ reflejado**
</dt> <dd>

La especificación de esta marca es la misma que la especificación de las marcas de la imagen reflejada del filtro de D3DX U, de la versión reflejada del filtro de d3dx \_ \_ \_ \_ \_ \_ \_ \_ \_ .

</dd> <dt>

<span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**\_Trama de filtro de D3DX10 \_**
</dt> <dd>

La imagen resultante debe ser interpolada mediante un algoritmo de tramado ordenado de 4x4. Esto sucede cuando se realiza la conversión de un formato a otro.

</dd> <dt>

<span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**\_Difusión de \_ interpolación de filtro de D3DX10 \_**
</dt> <dd>

Se difumina la interpolación en la imagen al cambiar de un formato a otro.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10 \_ filtro \_ sRGB \_ en**
</dt> <dd>

Los datos de entrada están en el espacio de colores RGB estándar (sRGB). Vea Notas.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10 \_ filtro \_ sRGB \_ out**
</dt> <dd>

Los datos de salida están en el espacio de colores RGB estándar (sRGB). Vea Notas.

</dd> <dt>

<span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10 \_ filtro \_ sRGB**
</dt> <dd>

Igual que al especificar el \_ filtro de d3dx \_ sRGB \_ en el \| filtro de d3dx \_ \_ \_ . Vea Notas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

D3DX10 realiza automáticamente la corrección gamma (para convertir los datos de color del espacio RGB al espacio RGB estándar) al cargar datos de textura. Esto se hace automáticamente por ejemplo cuando los datos RGB se cargan desde un archivo. png en una textura sRGB. Use las marcas de filtro SRGB para indicar si no es necesario convertir los datos en el espacio sRGB.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




