---
title: SampleCmp (objeto de textura de HLSL de DirectX)
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
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "104997193"
---
# <a name="samplecmp-directx-hlsl-texture-object"></a>SampleCmp (objeto de textura de HLSL de DirectX)

Muestrea una textura y compara un único componente con el valor de comparación especificado.

<table>
<tbody>
<tr class="odd">
<td>Float Object. SampleCmp ( <dl> SamplerComparisonState S,<br />
Ubicación Float,<br />
Float CompareValue,<br />
[desplazamiento int]<br />
</dl>);</td>
</tr>
</tbody>
</table>
 

La comparación es una comparación de un solo componente entre el primer componente almacenado en la textura y el valor de comparación pasado en el método.

Este método solo se puede invocar desde un sombreador de píxeles; no se admite en un sombreador de vértices o de geometría.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*
</dt> <dd>

Cualquier tipo [de objeto de textura](dx-graphics-hlsl-to-type.md) (excepto Texture2DMS, Texture2DMSArray o Texture3D).

</dd> <dt>

<span id="S"></span><span id="s"></span>*Seg*
</dt> <dd>

\[en \] un estado de comparación de muestra, que es el estado de la muestra más un estado de comparación (una función de comparación y un filtro de comparación). Vea el [tipo de muestra](dx-graphics-hlsl-sampler.md) para obtener más información y un ejemplo.

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Cód*
</dt> <dd>

\[en \] las coordenadas de textura. El tipo de argumento depende del tipo de objeto de textura.

| Tipo de Texture-Object          | Tipo de parámetro |
|------------------------------|----------------|
| Texture1D                    | FLOAT          |
| Texture1DArray, Texture2D    | float2         |
| Texture2DArray ¹, TextureCube | float3         |
| TextureCubeArray ¹            | float4         |

</dd> <dt>

<span id="CompareValue"></span><span id="comparevalue"></span><span id="COMPAREVALUE"></span>*CompareValue*
</dt> <dd>

Un valor de punto flotante que se va a utilizar como valor de comparación.

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Posición*
</dt> <dd>

\[en \] un desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura, el desplazamiento se aplica a la ubicación antes del muestreo. Los desplazamientos de textura deben ser estáticos. El tipo de argumento depende del tipo de objeto de textura. Para obtener más información, vea [aplicar desplazamientos de coordenadas de textura](dx-graphics-hlsl-to-sample.md).

| Tipo de Texture-Object            | Tipo de parámetro |
|--------------------------------|----------------|
| Texture1D, Texture1DArray      | int            |
| Texture2D, Texture2DArray ¹     | int2           |
| TextureCube, TextureCubeArray ¹ | No compatible  |

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de punto flotante en el intervalo de \[ 0.. 1 \] .

Para cada textura capturada (según la configuración de muestra del modo de filtro), **SampleCmp** realiza una comparación del valor z (tercer componente de la entrada) del sombreador con el valor textura (1 si se pasa la comparación; en caso contrario, 0). A continuación, **SampleCmp** combina estos 0 y 1 resultados para cada textura, como en el filtrado de textura normal (no un promedio) y devuelve el \[ valor 0.. 1 resultante \] al sombreador.

## <a name="remarks"></a>Observaciones

El filtrado de comparación proporciona una operación de filtrado básica que resulta útil para el filtrado porcentual y más detallado.

Cuando se usa este método en un recurso de punto flotante (en lugar de un formato normalizado con o sin signo), el valor de comparación no se fija automáticamente entre 0,0 y 1,0. Por lo tanto, puede ser necesaria una abrazadera manual del valor de comparación para las técnicas de sombreado comunes.

Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados diferentes en función de la implementación del hardware o de la configuración del controlador.

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.

| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 ² | PS \_ 4 \_ 0 | PS \_ 4 \_ 1 ² | GS \_ 4 \_ 0 | GS \_ 4 \_ 1 ² |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x ¹       | x         |          |           |

1.  Texture2DArray y TextureCubeArray están disponibles en el modelo de sombreador 4,1 o superior.
2.  El modelo de sombreador 4,1 está disponible en Direct3D 10,1 o superior.

> [!NOTE]  
> **SampleCmp** también está disponible en \_ \_ \_ los niveles 9 \_ 1 y 4 0 nivel 9 3 de PS 4 \_ \_ \_ \_ , cuando se usan las técnicas que se describen en [implementación de búferes de sombras para el nivel de características 9 de Direct3D](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>Temas relacionados

[Texture-objeto](dx-graphics-hlsl-to-type.md)
