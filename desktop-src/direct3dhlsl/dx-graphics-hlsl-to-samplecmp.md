---
title: SampleCmp (objeto de textura HLSL de DirectX)
description: Muestrea una textura y compara un único componente con el valor de comparación especificado.
ms.assetid: e21894c4-e8c5-4c3d-92c1-727964f8fd94
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6991bead4bfc42451c26fe5476b4c114626eb7e8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573792"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a>SampleCmp (objeto de textura HLSL de DirectX)

Muestrea una textura y compara un único componente con el valor de comparación especificado.

<table>
<tbody>
<tr class="odd">
<td>float Object.SampleCmp( <dl> SamplerComparisonState S,<br />
float Location,<br />
float CompareValue,<br />
[int Offset]<br />
</dl>);</td>
</tr>
</tbody>
</table>
 

La comparación es una comparación de un solo componente entre el primer componente almacenado en la textura y el valor de comparación pasado al método .

Este método solo se puede invocar desde un sombreador de píxeles; no se admite en un sombreador de vértices o geometría.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*
</dt> <dd>

Cualquier [tipo de objeto de](dx-graphics-hlsl-to-type.md) textura (excepto Texture2DMS, Texture2DMSArray o Texture3D).

</dd> <dt>

<span id="S"></span><span id="s"></span>*S*
</dt> <dd>

\[en un estado de comparación de muestreador, que es el estado del muestreador más un estado de comparación (una función de comparación \] y un filtro de comparación). Consulte el [tipo de sampler](dx-graphics-hlsl-sampler.md) para obtener más información y un ejemplo.

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Ubicación*
</dt> <dd>

\[en \] Las coordenadas de textura. El tipo de argumento depende del tipo texture-object.

| Texture-Object tipo          | Tipo de parámetro |
|------------------------------|----------------|
| Texture1D                    | FLOAT          |
| Texture1DArray, Texture2D    | float2         |
| Texture2DArray¹, TextureCube | float3         |
| TextureCubeArray¹            | float4         |

</dd> <dt>

<span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*
</dt> <dd>

Valor de punto flotante que se usará como valor de comparación.

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Compensar*
</dt> <dd>

\[en Un desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura; el desplazamiento se aplica a \] la ubicación antes del muestreo. Los desplazamientos de textura deben ser estáticos. El tipo de argumento depende del tipo texture-object. Para obtener más información, vea [Aplicar desplazamientos de coordenadas de textura.](dx-graphics-hlsl-to-sample.md)

| Texture-Object tipo            | Tipo de parámetro |
|--------------------------------|----------------|
| Texture1D, Texture1DArray      | int            |
| Texture2D, Texture2DArray¹     | int2           |
| TextureCube, TextureCubeArray¹ | No compatible  |

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de punto flotante en el \[ intervalo 0..1 \] .

Para cada elemento de textura capturada (según la configuración del muestreador del modo de filtro), **SampleCmp** realiza una comparación del valor z (tercer componente de entrada) del sombreador con el valor de texel (1 si se supera la comparación; de lo contrario, 0). A continuación, **SampleCmp** combina estos resultados 0 y 1 para cada elemento de textura como en el filtrado de textura normal (no un promedio) y devuelve el valor \[ 0..1 resultante al \] sombreador.

## <a name="remarks"></a>Observaciones

El filtrado de comparación proporciona una operación de filtrado básica que resulta útil para el filtrado de porcentaje más cercano.

Cuando se usa este método en un recurso de punto flotante (en lugar de un formato con o sin signo normalizado o con signo), el valor de comparación no se fija automáticamente entre 0,0 y 1,0. Por lo tanto, puede ser necesaria una fijación manual del valor de comparación para las técnicas de sombreado comunes.

Use un desplazamiento solo en un valor miplevel entero; De lo contrario, puede obtener resultados diferentes en función de la implementación de hardware o la configuración del controlador.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.

| vs \_ 4 \_ 0 | frente \_ a 4 \_ 1 | ps \_ 4 \_ 0 | ps \_ 4 \_ 1 así | gs \_ 4 \_ 0 | gs \_ 4 \_ 1ntes |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x¹       | x         |          |           |

1.  Texture2DArray y TextureCubeArray están disponibles en Shader Model 4.1 o posterior.
2.  El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o superior.

> [!NOTE]  
> **SampleCmp** también está disponible en ps 4 \_ 0 \_ level \_ 9 \_ 1 y 4 \_ 0 level 9 3 cuando se usan las técnicas que se describen en Implementación de búferes de sombra para el nivel 9 de características \_ \_ de \_ [Direct3D.](/previous-versions/windows/apps/jj262110(v=win.10))

## <a name="related-topics"></a>Temas relacionados

[Texture-Object](dx-graphics-hlsl-to-type.md)
