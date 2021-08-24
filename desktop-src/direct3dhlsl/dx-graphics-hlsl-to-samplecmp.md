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
ms.openlocfilehash: a606ad9081f1ca1fdc4261d862ea6edfef4460989bb6d51d839d85f5797c1466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854645"
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

\[en \] Coordenadas de textura. El tipo de argumento depende del tipo texture-object.

| Texture-Object type          | Tipo de parámetro |
|------------------------------|----------------|
| Texture1D                    | FLOAT          |
| Texture1DArray, Texture2D    | float2         |
| Texture2DArray así como TextureCube | float3         |
| TextureCubeArray¹            | float4         |

</dd> <dt>

<span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*
</dt> <dd>

Valor de punto flotante que se usará como valor de comparación.

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Compensar*
</dt> <dd>

\[en Un desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura; el desplazamiento se aplica a \] la ubicación antes del muestreo. Los desplazamientos de textura deben ser estáticos. El tipo de argumento depende del tipo texture-object. Para obtener más información, vea [Aplicar desplazamientos de coordenadas de textura.](dx-graphics-hlsl-to-sample.md)

| Texture-Object type            | Tipo de parámetro |
|--------------------------------|----------------|
| Texture1D, Texture1DArray      | int            |
| Texture2D, Texture2DArray¹     | int2           |
| TextureCube, TextureCubeArray¹ | No compatible  |

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de punto flotante en el \[ intervalo 0..1 \] .

Para cada texel que se captura (según la configuración del muestreador del modo de filtro), **SampleCmp** realiza una comparación del valor z (tercer componente de entrada) del sombreador con el valor de texel (1 si se supera la comparación; en caso contrario, 0). **SampleCmp** combina estos resultados 0 y 1 para cada texel juntos como en el filtrado de textura normal (no un promedio) y devuelve el valor \[ 0..1 resultante al sombreador. \]

## <a name="remarks"></a>Comentarios

El filtrado de comparación proporciona una operación de filtrado básica que resulta útil para el filtrado de porcentaje más cercano.

Cuando se usa este método en un recurso de punto flotante (en lugar de un formato con o sin signo normalizado), el valor de comparación no se fija automáticamente entre 0,0 y 1,0. Por lo tanto, puede ser necesaria una fijación manual del valor de comparación para técnicas de sombreado comunes.

Use un desplazamiento solo en un miplevel entero; De lo contrario, puede obtener resultados diferentes en función de la implementación de hardware o la configuración del controlador.

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.

| vs \_ 4 \_ 0 | frente \_ a 4 \_ 1 | ps \_ 4 \_ 0 | ps \_ 4 \_ 1 además | gs \_ 4 \_ 0 | gs \_ 4 \_ 1 |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x¹       | x         |          |           |

1.  Texture2DArray y TextureCubeArray están disponibles en Shader Model 4.1 o superior.
2.  El modelo de sombreador 4.1 está disponible en Direct3D 10.1 o posterior.

> [!NOTE]  
> **SampleCmp** también está disponible en ps 4 \_ 0 nivel 9 1 y 4 0 nivel 9 3 cuando se usan las técnicas que se describen en Implementación de búferes de sombra para el nivel de característica \_ \_ \_ \_ \_ \_ \_ [9 de Direct3D.](/previous-versions/windows/apps/jj262110(v=win.10))

## <a name="related-topics"></a>Temas relacionados

[Texture-Object](dx-graphics-hlsl-to-type.md)
