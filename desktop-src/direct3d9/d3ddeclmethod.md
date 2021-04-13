---
description: Define el método de declaración de vértices, que es una operación predefinida realizada por del teselador (o cualquier rutina de geometría de procedimiento en los datos de vértice durante la teselación).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Enumeración D3DDECLMETHOD (D3D9Types. h)
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
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362476"
---
# <a name="d3ddeclmethod-enumeration"></a>Enumeración D3DDECLMETHOD

Define el método de declaración de vértices, que es una operación predefinida realizada por del teselador (o cualquier rutina de geometría de procedimiento en los datos de vértice durante la teselación).

## <a name="syntax"></a>Sintaxis


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

<span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**\_Valor predeterminado de D3DDECLMETHOD**
</dt> <dd>

Valor predeterminado. El del teselador copia los datos de vértice (datos de spline para las revisiones) tal cual, sin cálculos adicionales. Cuando se usa del teselador, se interpola este elemento. En caso contrario, los datos de vértice se copian en el registro de entrada. El tipo de entrada y salida puede ser cualquier valor, pero siempre son del mismo tipo.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ PARTIALU**
</dt> <dd>

Calcula la tangente en un punto de la revisión del rectángulo o del triángulo en la dirección U. El tipo de entrada puede ser uno de los siguientes:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

El tipo de salida siempre es D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ PARTIALV**
</dt> <dd>

Calcula la tangente en un punto de la revisión del rectángulo o del triángulo en la dirección V. El tipo de entrada puede ser uno de los siguientes:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

El tipo de salida siempre es D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ CROSSUV**
</dt> <dd>

Calcula el normal en un punto de la revisión del rectángulo o del triángulo tomando el producto cruzado de dos tangentes. El tipo de entrada puede ser uno de los siguientes:

-   D3DDECLTYPE \_ D3DCOLOR
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4
-   D3DDECLTYPE \_ SHORT4
-   D3DDECLTYPE \_ UBYTE4

El tipo de salida siempre es D3DDECLTYPE \_ FLOAT3.

</dd> <dt>

<span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**UV de D3DDECLMETHOD \_**
</dt> <dd>

Copie los valores de U, V en un punto de la revisión de rectángulo o triángulo. Esto da como resultado un float 2D. El tipo de entrada debe establecerse en D3DDECLTYPE \_ sin usar. El tipo de datos de salida siempre es D3DDECLTYPE \_ FLOAT2. El flujo de entrada y el desplazamiento también están sin usar (pero debe establecerse en 0).

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**\_Búsqueda D3DDECLMETHOD**
</dt> <dd>

Buscar un mapa de desplazamiento. El tipo de entrada puede ser uno de los siguientes:

-   D3DDECLTYPE \_ FLOAT2
-   D3DDECLTYPE \_ FLOAT3
-   D3DDECLTYPE \_ FLOAT4

Solo se usan los componentes. x y. y para la búsqueda de mapa de textura. El tipo de salida siempre es D3DDECLTYPE \_ FLOAT1. El dispositivo debe admitir la asignación de desplazamiento. Para obtener más información acerca de la asignación de desplazamiento, vea [asignación de desplazamiento (Direct3D 9)](displacement-mapping.md). Esta constante solo es compatible con la canalización programable en los datos de N revisiones, si están habilitadas las revisiones N.

</dd> <dt>

<span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ LOOKUPPRESAMPLED**
</dt> <dd>

Buscar un mapa de desplazamiento premuestreado. El tipo de entrada debe establecerse en D3DDECLTYPE \_ sin usar; el índice de flujo y el desplazamiento de flujo deben establecerse en 0. El tipo de salida de esta operación siempre es D3DDECLTYPE \_ FLOAT1. El dispositivo debe admitir la asignación de desplazamiento. Para obtener más información acerca de la asignación de desplazamiento, vea [asignación de desplazamiento (Direct3D 9)](displacement-mapping.md). Esta constante solo es compatible con la canalización programable en los datos de N revisiones, si están habilitadas las revisiones N. Este método solo se puede usar con el \_ ejemplo D3DDECLUSAGE.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Del teselador examina el método para determinar qué datos se deben calcular a partir de los datos de vértice durante la teselación. Los datos de la malla deben usar el valor predeterminado. Las revisiones pueden utilizar cualquiera de los otros tipos implementados.

Los datos de vértices se declaran con una matriz de estructuras [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Cada elemento de la matriz contiene un método de declaración de vértice.

Además de usar \_ el valor predeterminado de D3DDECLMETHOD, una malla normal puede usar \_ los métodos D3DDECLMETHOD Lookup y D3DDECLMETHOD \_ LOOKUPPRESAMPLED cuando se habilitan N-patches.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




