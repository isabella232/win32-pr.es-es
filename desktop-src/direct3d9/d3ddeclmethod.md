---
description: Define el método de declaración de vértices, que es una operación predefinida realizada por el teselador (o cualquier rutina de geometría de procedimientos en los datos del vértice durante la teselación).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Enumeración D3DDECLMETHOD (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f34700666ecb830470e58a3f3389cd6207be68403e612f50ddafc841dd839ed2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565065"
---
# <a name="d3ddeclmethod-enumeration"></a>D3DDECLMETHOD (enumeración)

Define el método de declaración de vértices, que es una operación predefinida realizada por el teselador (o cualquier rutina de geometría de procedimientos en los datos del vértice durante la teselación).

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ PREDETERMINADO**
</dt> <dd>

Valor predeterminado. El teselador copia los datos de vértice (datos spline para revisiones) tal y como están, sin cálculos adicionales. Cuando se usa el teselador, este elemento se interpola. De lo contrario, los datos de vértice se copian en el registro de entrada. El tipo de entrada y salida puede ser cualquier valor, pero siempre son del mismo tipo.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ PARTIALU**
</dt> <dd>

Calcula la tangente en un punto del rectángulo o la revisión del triángulo en la dirección U. El tipo de entrada puede ser uno de los siguientes:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

El tipo de salida es siempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ PARTIALV**
</dt> <dd>

Calcula la tangente en un punto del rectángulo o la revisión del triángulo en la dirección V. El tipo de entrada puede ser uno de los siguientes:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

El tipo de salida es siempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ CROSSUV**
</dt> <dd>

Calcula la normal en un punto de la revisión de rectángulo o triángulo tomando el producto cruzado de dos tangentes. El tipo de entrada puede ser uno de los siguientes:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

El tipo de salida es siempre D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD \_ UV**
</dt> <dd>

Copie los valores de U y V en un punto del rectángulo o la revisión del triángulo. Esto da como resultado un valor float 2D. El tipo de entrada debe establecerse en D3DDECLTYPE \_ UNUSED. El tipo de datos de salida es siempre D3DDECLTYPE \_ FLOAT2. El flujo de entrada y el desplazamiento también no se usan (pero deben establecerse en 0).

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD \_ LOOKUP**
</dt> <dd>

Busque un mapa de desplazamiento. El tipo de entrada puede ser uno de los siguientes:

-   D3DDECLTYPE \_ FLOAT2
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4

Solo se usan los componentes .x y .y para la búsqueda del mapa de textura. El tipo de salida es siempre D3DDECLTYPE \_ FLOAT1. El dispositivo debe admitir la asignación de desplazamiento. Para obtener más información sobre la asignación de desplazamiento, vea [Asignación de desplazamiento (Direct3D 9).](displacement-mapping.md) Esta constante solo es compatible con la canalización programable en los datos de N revisiones, si están habilitadas las N revisiones.

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ LOOKUPPRESAMPLED**
</dt> <dd>

Busque un mapa de desplazamiento de ejemplo previo. El tipo de entrada debe establecerse en D3DDECLTYPE UNUSED; el índice de secuencia y el desplazamiento de flujo deben \_ establecerse en 0. El tipo de salida de esta operación es siempre D3DDECLTYPE \_ FLOAT1. El dispositivo debe admitir la asignación de desplazamiento. Para obtener más información sobre la asignación de desplazamiento, vea [Asignación de desplazamiento (Direct3D 9).](displacement-mapping.md) Esta constante solo es compatible con la canalización programable en los datos de N revisiones, si están habilitadas las N revisiones. Este método solo se puede usar con D3DDECLUSAGE \_ SAMPLE.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El teselador examina el método para determinar qué datos se calculan a partir de los datos de vértice durante la teselación. Los datos de malla deben usar el valor predeterminado. Las revisiones pueden usar cualquiera de los otros tipos implementados.

Los datos de vértice se declaran con una matriz de [**estructuras D3DVERTEXELEMENT9.**](d3dvertexelement9.md) Cada elemento de la matriz contiene un método de declaración de vértice.

Además de usar D3DDECLMETHOD DEFAULT, una malla normal puede usar los métodos \_ D3DDECLMETHOD LOOKUP y \_ D3DDECLMETHOD LOOKUPPRESAMPLED cuando se \_ habilitan N revisiones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




