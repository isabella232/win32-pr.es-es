---
description: Define la configuración utilizada para los cálculos de fotogramas tangentes de malla.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Enumeración D3DXTANGENT (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 5d6e57d2027a7366ec2b82ac7bd82aae4275d489c17f1922684e3ca6232be940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749775"
---
# <a name="d3dxtangent-enumeration"></a>D3DXTANGENT (enumeración)

Define la configuración utilizada para los cálculos de fotogramas tangentes de malla.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ WRAP \_ U**
</dt> <dd>

Los valores de coordenadas de textura en la dirección u están entre 0 y 1. En este caso, se elegirá un conjunto de coordenadas de textura que minimice el perímetro del triángulo. Vea [Ajuste de textura (Direct3D 9).](texture-wrapping.md)

</dd> <dt>

<span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ WRAP \_ V**
</dt> <dd>

Los valores de coordenadas de textura en la dirección v están entre 0 y 1. En este caso, se elegirá un conjunto de coordenadas de textura que minimice el perímetro del triángulo. Vea [Ajuste de textura (Direct3D 9).](texture-wrapping.md)

</dd> <dt>

<span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ WRAP \_ UV**
</dt> <dd>

Los valores de coordenadas de textura en las direcciones v y usted están entre 0 y 1. En este caso, se elegirá un conjunto de coordenadas de textura que minimice el perímetro del triángulo. Vea [Ajuste de textura (Direct3D 9).](texture-wrapping.md)

</dd> <dt>

<span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ DONT \_ NORMALIZE \_ PARTIALS**
</dt> <dd>

No normalice los derivados parciales con respecto a las coordenadas de textura. Si no se normaliza, la escala de los derivados parciales es proporcional a la escala del modelo 3D dividida por la escala del triángulo en el espacio (u, v). Este valor de escala proporciona una medida de cuánto se ajusta la textura en una dirección determinada. La longitud del vector resultante es una suma ponderada de las longitudes de los derivados parciales.

</dd> <dt>

<span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ DONT \_ ORTHOGONALIZE**
</dt> <dd>

No transforme las coordenadas de textura en coordenadas cartesianas ortogonales. Mutuamente excluyente con D3DXTANGENT \_ ORTHOGONALIZE \_ FROM you y \_ D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ V.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ V**
</dt> <dd>

Calcule el derivado parcial con respecto a la coordenada de textura v de forma independiente para cada vértice y, a continuación, calcule el derivado parcial con respecto a usted como el producto cruzado del derivado parcial con respecto a v y el vector normal. Mutuamente excluyente con D3DXTANGENT \_ DONT \_ ORTHOGONALIZE y D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ U**
</dt> <dd>

Calcule el derivado parcial con respecto a la coordenada de textura u independientemente para cada vértice y, a continuación, calcule el derivado parcial con respecto a v como el producto cruzado del vector normal y el derivado parcial con respecto a usted. Mutuamente excluyente con D3DXTANGENT \_ DONT \_ ORTHOGONALIZE y D3DXTANGENT \_ ORTHOGONALIZE \_ FROM \_ V.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT \_ WEIGHT \_ BY \_ AREA**
</dt> <dd>

Pondera la dirección del vector derivado parcial o normal por vértice calculado según las áreas de los triángulos asociados a ese vértice. Mutuamente excluyente con D3DXTANGENT \_ WEIGHT \_ EQUAL.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT \_ WEIGHT \_ EQUAL**
</dt> <dd>

Calcule un vector normal de longitud de unidad para cada triángulo de la malla de entrada. Mutuamente excluyente con D3DXTANGENT \_ WEIGHT \_ BY \_ AREA.

</dd> <dt>

<span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT \_ WIND \_ CW**
</dt> <dd>

Los vértices se ordenan en una dirección en el sentido de las agujas del reloj alrededor de cada triángulo. Por lo tanto, la dirección del vector normal calculada se invierte 180 grados desde la dirección calculada mediante la ordenación de vértices en sentido contrario a las agujas del reloj.

</dd> <dt>

<span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ CALCULATE \_ NORMALS**
</dt> <dd>

Calcule el vector normal por vértice para cada triángulo de la malla de entrada e ignore los vectores normales que ya están en la malla de entrada.

</dd> <dt>

<span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ GENERATE \_ IN \_ PLACE**
</dt> <dd>

Los resultados se almacenan en la malla de entrada original y no se usa la malla de salida.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




