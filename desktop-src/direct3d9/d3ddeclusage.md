---
description: Identifica el uso previsto de los datos de vértice.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Enumeración D3DDECLUSAGE (D3D9Types.h)
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
ms.openlocfilehash: 707a5b7b886ac9366733e1b17322ac61c7d9703cb6ef8ac1e095cf1300fd508d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857515"
---
# <a name="d3ddeclusage-enumeration"></a>D3DDECLUSAGE (enumeración)

Identifica el uso previsto de los datos de vértice.

## <a name="syntax"></a>Syntax


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

<span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE \_ POSITION**
</dt> <dd>

Datos de posición que van de (-1,-1) a (1,1). Use D3DDECLUSAGE POSITION con un índice de uso de 0 para especificar la posición sin transformación para el procesamiento de vértices de función fija y el teselador de n \_ revisiones. Use D3DDECLUSAGE POSITION con un índice de uso de 1 para especificar la posición sintransformar en el sombreador de vértices de función fija para la interpolación \_ de vértices.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ BLENDWEIGHT**
</dt> <dd>

Combinar datos de peso. Use D3DDECLUSAGE BLENDWEIGHT con un índice de uso de 0 para especificar los pesos de mezcla usados en la mezcla de vértices indexados y no \_ indexados.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ BLENDINDICES**
</dt> <dd>

Combinar datos de índices. Use D3DDECLUSAGE BLENDINDICES con un índice de uso de 0 para especificar los índices de matriz para la \_ despeinación de paleta indizada.

</dd> <dt>

<span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ NORMAL**
</dt> <dd>

Datos normales de vértices. Use D3DDECLUSAGE NORMAL con un índice de uso de 0 para especificar las normales de vértice para el procesamiento de vértices de función fija y el teselador de n \_ revisiones. Use D3DDECLUSAGE NORMAL con un índice de uso de 1 para especificar normales de vértice para el procesamiento de vértices de función fija para la interpolación \_ de vértices.

</dd> <dt>

<span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ PSIZE**
</dt> <dd>

Datos de tamaño de punto. Use D3DDECLUSAGE PSIZE con un índice de uso de 0 para especificar el atributo de tamaño de punto utilizado por el motor de instalación del rasterizador para expandir un punto en un cuadráncho para la funcionalidad de \_ sprite de punto.

</dd> <dt>

<span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ TEXCOORD**
</dt> <dd>

Datos de coordenadas de textura. Use D3DDECLUSAGE TEXCOORD, n para especificar coordenadas de textura en el procesamiento de vértices de función fija y en sombreadores de píxeles anteriores a \_ ps \_ 3 \_ 0. Se pueden usar para pasar datos definidos por el usuario.

</dd> <dt>

<span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**TANGENTE D3DDECLUSAGE \_**
</dt> <dd>

Datos tangentes de vértices.

</dd> <dt>

<span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ BINORMAL**
</dt> <dd>

Datos binormales de vértices.

</dd> <dt>

<span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ TESSFACTOR**
</dt> <dd>

Valor de punto flotante positivo único. Use D3DDECLUSAGE TESSFACTOR con un índice de uso de 0 para especificar un factor de teselación usado en la unidad de teselación para controlar la velocidad de \_ teselación. Para obtener más información sobre el tipo de datos, vea D3DDECLTYPE \_ FLOAT1.

</dd> <dt>

<span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE \_ POSITIONT**
</dt> <dd>

Los datos de vértices contienen datos de posición transformados que van de (0,0) a (ancho de ventanilla, alto de ventanilla). Use D3DDECLUSAGE \_ POSITIONT con un índice de uso de 0 para especificar la posición transformada. Cuando se establece una declaración que contiene esto, la canalización no realiza el procesamiento de vértices.

</dd> <dt>

<span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE \_ COLOR**
</dt> <dd>

Los datos de vértice contienen un color difuso o especular. Use D3DDECLUSAGE COLOR con un índice de uso de 0 para especificar el color difuso en el sombreador de vértices de función fija y los sombreadores de píxeles anteriores \_ a ps \_ 3 \_ 0. Use D3DDECLUSAGE COLOR con un índice de uso de 1 para especificar el color especular en el sombreador de vértices de función fija y los sombreadores de píxeles anteriores \_ a ps \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGEMAS \_**
</dt> <dd>

Los datos de vértices contienen datos de ángulo. Use D3DDECLUSAGE DOW con un índice de uso de 0 para especificar un valor de mezcla usado después de que finalice el \_ sombreado de píxeles. Esto se aplica a los sombreadores de píxeles anteriores a la versión ps \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**PROFUNDIDAD DE D3DDECLUSAGE \_**
</dt> <dd>

Los datos de vértice contienen datos de profundidad.

</dd> <dt>

<span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE \_ SAMPLE**
</dt> <dd>

Los datos de vértices contienen datos del muestreador. Use D3DDECLUSAGE SAMPLE con un índice de uso de 0 para especificar \_ el valor de desplazamiento que se buscará. Solo se puede usar con D3DDECLUSAGE \_ LOOKUPPRESAMPLED o D3DDECLUSAGE \_ LOOKUP.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los datos de vértice se declaran con una matriz [**de estructuras D3DVERTEXELEMENT9.**](d3dvertexelement9.md) Cada elemento de la matriz contiene un tipo de uso.

Para obtener más información sobre las declaraciones de vértices, vea [Declaración de vértice (Direct3D 9).](vertex-declaration.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[Declaración de vértice (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 




