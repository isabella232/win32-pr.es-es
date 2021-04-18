---
description: Define la configuración utilizada para los cálculos de fotogramas tangentes de malla.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Enumeración D3DXTANGENT (D3dx9mesh. h)
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
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717731"
---
# <a name="d3dxtangent-enumeration"></a>Enumeración D3DXTANGENT

Define la configuración utilizada para los cálculos de fotogramas tangentes de malla.

## <a name="syntax"></a>Sintaxis


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

<span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ Wrap \_ U**
</dt> <dd>

Los valores de las coordenadas de textura en la dirección u se encuentran entre 0 y 1. En este caso, se elegirá un conjunto de coordenadas de textura que minimice el perímetro del triángulo. Vea [ajuste de textura (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ Wrap \_ V**
</dt> <dd>

Los valores de las coordenadas de textura en la dirección v se encuentran entre 0 y 1. En este caso, se elegirá un conjunto de coordenadas de textura que minimice el perímetro del triángulo. Vea [ajuste de textura (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT \_ encapsulado \_ UV**
</dt> <dd>

Los valores de las coordenadas de textura en ambas direcciones se encuentran entre 0 y 1. En este caso, se elegirá un conjunto de coordenadas de textura que minimice el perímetro del triángulo. Vea [ajuste de textura (Direct3D 9)](texture-wrapping.md).

</dd> <dt>

<span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ no \_ normalizar las \_ partes parciales**
</dt> <dd>

No normalice las derivadas parciales con respecto a las coordenadas de textura. Si no se normaliza, la escala de los derivados parciales es proporcional a la escala del modelo 3D dividida por la escala del triángulo en el espacio (u, v). Este valor de escala proporciona una medida de cuánto se estira la textura en una dirección determinada. La longitud del vector resultante es una suma ponderada de las longitudes de los derivados parciales.

</dd> <dt>

<span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT no se \_ \_ corortogonal**
</dt> <dd>

No transforme las coordenadas de textura en coordenadas cartesianas ortogonales. Es mutuamente excluyente con D3DXTANGENT \_ ortogonal \_ desde el \_ usuario y D3DXTANGENT \_ ortogonal \_ desde \_ V.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ ortogonal \_ desde \_ V**
</dt> <dd>

Calcule el derivado parcial con respecto a la coordenada de textura v independientemente para cada vértice y, a continuación, calcule el derivado parcial con respecto a usted como el producto cruzado de la derivada parcial con respecto a v y el vector normal. Mutuamente excluyente con D3DXTANGENT no se ortogonala \_ \_ y D3DXTANGENT se \_ ortogonala \_ desde \_ U.

</dd> <dt>

<span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ ortogonal \_ desde \_ U**
</dt> <dd>

Calcule el derivado parcial con respecto a la coordenada de textura u de forma independiente para cada vértice y, a continuación, calcule el derivado parcial con respecto a v como el producto cruzado del vector normal y el derivado parcial con respecto a usted. Mutuamente excluyente con D3DXTANGENT no se ha \_ \_ ortogonal y D3DXTANGENT \_ ortogonal \_ desde \_ V.

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**\_Peso \_ de D3DXTANGENT por \_ área**
</dt> <dd>

Ponderación de la dirección del vector calculado por vértices normal o derivado parcial calculado según las áreas de los triángulos adjuntas a ese vértice. Es mutuamente excluyente con el peso de D3DXTANGENT \_ \_ .

</dd> <dt>

<span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**Peso de D3DXTANGENT \_ \_ igual**
</dt> <dd>

Calcula un vector normal de longitud de unidad para cada triángulo de la malla de entrada. Es mutuamente excluyente con el peso de D3DXTANGENT \_ \_ por \_ área.

</dd> <dt>

<span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT de \_ viento \_ CW**
</dt> <dd>

Los vértices se ordenan en sentido de las agujas del reloj alrededor de cada triángulo. Por lo tanto, la dirección del vector normal calculado se invierte 180 grados de la dirección calculada mediante el orden de vértices en sentido contrario a las agujas del reloj.

</dd> <dt>

<span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ calcular \_ normales**
</dt> <dd>

Calcule el vector normal por vértice para cada triángulo de la malla de entrada y omita los vectores normales que ya se encuentren en la malla de entrada.

</dd> <dt>

<span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ generar \_ en \_ contexto**
</dt> <dd>

Los resultados se almacenan en la malla de entrada original y no se usa la malla de salida.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




