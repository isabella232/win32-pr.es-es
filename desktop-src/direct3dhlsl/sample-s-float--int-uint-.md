---
title: Función de ejemplo (S, Float, int, Float, uint) (referencia de HLSL)
description: Muestrea un Texture2D con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en y devuelve el estado de la operación.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
keywords:
- HLSL de la función de ejemplo
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b378cb4031acecb8e0018053c7547e1948cc3e6
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "103797565"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a>Función de ejemplo (S, Float, int, Float, uint) (referencia de HLSL)

Muestrea un [**Texture2D**](sm5-object-texture2d.md) con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en y devuelve el estado de la operación.

> [!Note]  
> Requiere el [modelo de sombreador 5](d3d11-graphics-reference-sm5.md) o superior.

 

## <a name="syntax"></a>Sintaxis

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*S* \[ en\]
</dt> <dd>

Un [Estado de muestra](dx-graphics-hlsl-sampler.md). Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.

</dd> <dt>

*Ubicación* \[ de de\]
</dt> <dd>

Las coordenadas de textura. El tipo de argumento depende del tipo de objeto de textura.



| Tipo de Texture-Object                    | Tipo de parámetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Desplazamiento* \[ de\]
</dt> <dd>

Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo. Los desplazamientos de textura deben ser estáticos. El tipo de argumento depende del tipo de objeto de textura. Para obtener más información, vea [aplicar desplazamientos de coordenadas de textura](dx-graphics-hlsl-to-sample.md).



| Tipo de Texture-Object           | Tipo de parámetro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | no admitido  |



 

</dd> <dt>

*Abrazadera* \[ de\]
</dt> <dd>

Un valor opcional en el que se van a fijar los valores LOD de ejemplo. Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.

</dd> <dt>

*Estado* \[ de enuncia\]
</dt> <dd>

Estado de la operación. No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features). Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="remarks"></a>Observaciones

El muestreo de textura usa la posición textura para buscar un valor textura. Se puede aplicar un desplazamiento a la posición antes de la búsqueda. El estado de muestra contiene las opciones de muestreo y filtrado. Este método se puede invocar dentro de un sombreador de píxeles, pero no se admite en un sombreador de vértices o un sombreador de geometría.

Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados diferentes en función de la implementación del hardware o de la configuración del controlador.

### <a name="calculating-texel-positions"></a>Calcular las posiciones de textura

Las coordenadas de textura son valores de punto flotante que hacen referencia a los datos de textura, lo que también se conoce como espacio de textura normalizado. Los modos de ajuste de direcciones se aplican en este orden (coordenadas de textura + desplazamientos + modo de ajuste) para modificar las coordenadas de textura fuera del \[ intervalo de 0... 1 \] .

En el caso de las matrices de textura, un valor adicional en el parámetro Location especifica un índice en una matriz de textura. Este índice se trata como un valor de punto flotante escalado (en lugar del espacio normalizado para las coordenadas de textura estándar). La conversión a un índice de entero se realiza en el orden siguiente (float + Round-to-Even Integer + Clamp al intervalo de la matriz).

### <a name="applying-texture-coordinate-offsets"></a>Aplicar desplazamientos de coordenadas de textura

El parámetro offset modifica las coordenadas de textura, en el espacio textura. Aunque las coordenadas de textura son números de punto flotante normalizados, el desplazamiento aplica un desplazamiento entero. Tenga en cuenta también que los desplazamientos de textura deben ser estáticos.

El formato de datos devuelto viene determinado por el formato de textura. Por ejemplo, si el recurso de textura se definió con el formato de DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB, la operación de muestreo convierte textura muestreadas de gamma 2,0 a 1,0, filtrar y escribe el resultado como un valor de punto flotante en el intervalo \[ 0.. 1 \] .

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos de ejemplo](texture-sample-overload.md)
</dt> <dt>

[Texture-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
