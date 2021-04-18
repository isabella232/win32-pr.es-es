---
description: Identifica el uso previsto de los datos de vértices.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Enumeración D3DDECLUSAGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3997aa38a7a97455b9f36d8afbee896ca9ae937
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721445"
---
# <a name="d3ddeclusage-enumeration"></a>Enumeración D3DDECLUSAGE

Identifica el uso previsto de los datos de vértices.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**\_Posición D3DDECLUSAGE**
</dt> <dd>

Coloque los datos comprendidos entre (-1,-1) y (1,1). Use \_ la posición D3DDECLUSAGE con un índice de uso de 0 para especificar la posición sin transformar para el procesamiento de vértices de función fija y el del teselador de n-patch. Use \_ la posición D3DDECLUSAGE con un índice de uso de 1 para especificar la posición sin transformar en el sombreador de vértices de función fija para la interpolación de vértices.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ BLENDWEIGHT**
</dt> <dd>

Mezclar datos de peso. Use D3DDECLUSAGE \_ BLENDWEIGHT con un índice de uso de 0 para especificar los pesos de fusión utilizados en la mezcla de vértices indexados y no indexados.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ BLENDINDICES**
</dt> <dd>

Mezclar datos de índices. Use D3DDECLUSAGE \_ BLENDINDICES con un índice de uso de 0 para especificar índices de matriz para la numeración de paletas indizada.

</dd> <dt>

<span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ normal**
</dt> <dd>

Datos normales de vértices. Use D3DDECLUSAGE \_ normal con un índice de uso de 0 para especificar las normales de vértices para el procesamiento de vértices de función fija y la del teselador de n-patch. Use D3DDECLUSAGE \_ normal con un índice de uso de 1 para especificar las normales de vértices para el procesamiento de vértices de funciones fijas para la interpolación de vértices.

</dd> <dt>

<span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ PSIZE**
</dt> <dd>

Datos de tamaño de punto. Use D3DDECLUSAGE \_ PSIZE con un índice de uso de 0 para especificar el atributo de tamaño de punto que usa el motor de instalación del rasterizador para expandir un punto en un cuádruple para la funcionalidad de punto y Sprite.

</dd> <dt>

<span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ TEXCOORD**
</dt> <dd>

Datos de coordenadas de textura. Use D3DDECLUSAGE \_ TEXCOORD, n para especificar coordenadas de textura en el procesamiento de vértices de función fija y en sombreadores de píxeles anteriores a PS \_ 3 \_ 0. Se pueden usar para pasar datos definidos por el usuario.

</dd> <dt>

<span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**\_Tangente D3DDECLUSAGE**
</dt> <dd>

Datos de tangente de vértice.

</dd> <dt>

<span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**\_BInormalización D3DDECLUSAGE**
</dt> <dd>

Datos binormales de vértices.

</dd> <dt>

<span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ TESSFACTOR**
</dt> <dd>

Valor de punto flotante positivo único. Use D3DDECLUSAGE \_ TESSFACTOR con un índice de uso de 0 para especificar un factor de teselación usado en la unidad de teselación para controlar la velocidad de teselación. Para obtener más información sobre el tipo de datos, vea D3DDECLTYPE \_ FLOAT1.

</dd> <dt>

<span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE \_ posición**
</dt> <dd>

Los datos de vértice contienen datos de posición transformados que van de (0,0) a (ancho de la ventanilla, alto de la ventanilla). Utilice D3DDECLUSAGE \_ Position con un índice de uso de 0 para especificar la posición transformada. Cuando se establece una declaración que contiene este, la canalización no realiza el procesamiento de vértices.

</dd> <dt>

<span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**COLOR de D3DDECLUSAGE \_**
</dt> <dd>

Los datos de vértice contienen colores difusos o especulares. Use D3DDECLUSAGE \_ color con un índice de uso de 0 para especificar el color difuso en el sombreador de vértices de función fija y los sombreadores de píxeles anteriores a PS \_ 3 \_ 0. Use D3DDECLUSAGE \_ color con un índice de uso de 1 para especificar el color especular en el sombreador de vértices de función fija y los sombreadores de píxeles anteriores a PS \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**Niebla de D3DDECLUSAGE \_**
</dt> <dd>

Los datos de vértice contienen datos de niebla. Use \_ la niebla de D3DDECLUSAGE con un índice de uso de 0 para especificar un valor de mezcla de niebla usado después de que finalice el sombreado de píxeles. Esto se aplica a los sombreadores de píxeles anteriores a la versión PS \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**Profundidad de D3DDECLUSAGE \_**
</dt> <dd>

Los datos de vértice contienen datos de profundidad.

</dd> <dt>

<span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**Ejemplo de D3DDECLUSAGE \_**
</dt> <dd>

Los datos de vértice contienen datos de muestra. Use \_ el ejemplo D3DDECLUSAGE con un índice de uso de 0 para especificar el valor de desplazamiento que se va a buscar. Solo se puede usar con D3DDECLUSAGE \_ LOOKUPPRESAMPLED o D3DDECLUSAGE \_ lookup.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los datos de vértices se declaran con una matriz de estructuras [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Cada elemento de la matriz contiene un tipo de uso.

Para obtener más información sobre las declaraciones de vértices, vea [declaración de vértices (Direct3D 9)](vertex-declaration.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[Declaración de vértices (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 




