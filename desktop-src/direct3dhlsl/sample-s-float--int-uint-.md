---
title: Función Sample(S,float,int,float,uint) (referencia hlsl)
description: Muestrea un objeto Texture2D con un valor opcional para fijar los valores de nivel de detalle (LOD) de la muestra y devuelve el estado de la operación.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
keywords:
- Función de ejemplo HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072693"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a>Función Sample(S,float,int,float,uint) (referencia hlsl)

Muestrea [**un objeto Texture2D**](sm5-object-texture2d.md) con un valor opcional para fijar los valores de nivel de detalle (LOD) de la muestra y devuelve el estado de la operación.

> [!Note]  
> Requiere [el modelo de sombreador 5](d3d11-graphics-reference-sm5.md) o superior.

 

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

Un [estado sampler](dx-graphics-hlsl-sampler.md). Se trata de un objeto declarado en un archivo de efecto que contiene asignaciones de estado.

</dd> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Las coordenadas de textura. El tipo de argumento depende del tipo texture-object.



| Texture-Object tipo                    | Tipo de parámetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Desplazamiento* \[ En\]
</dt> <dd>

Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura; el desplazamiento se aplica a la ubicación antes del muestreo. Los desplazamientos de textura deben ser estáticos. El tipo de argumento depende del tipo texture-object. Para obtener más información, vea [Aplicar desplazamientos de coordenadas de textura.](dx-graphics-hlsl-to-sample.md)



| Texture-Object tipo           | Tipo de parámetro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | no admitido  |



 

</dd> <dt>

*Fijación* \[ En\]
</dt> <dd>

Valor opcional al que se fijan los valores de LOD de ejemplo. Por ejemplo, si pasa 2,0f para el valor de fijación, asegúrese de que ninguna muestra individual tiene acceso a un nivel de mip inferior a 2,0f.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación **Sample**, **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se tomaron valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Formato de textura, que es uno de los valores con tipo enumerados [**en DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="remarks"></a>Observaciones

El muestreo de textura usa la posición del texel para buscar un valor de texel. Se puede aplicar un desplazamiento a la posición antes de la búsqueda. El estado del muestreador contiene las opciones de muestreo y filtrado. Este método se puede invocar dentro de un sombreador de píxeles, pero no se admite en un sombreador de vértices o un sombreador de geometría.

Use un desplazamiento solo en un valor miplevel entero; De lo contrario, puede obtener resultados diferentes en función de la implementación de hardware o la configuración del controlador.

### <a name="calculating-texel-positions"></a>Cálculo de posiciones de texel

Las coordenadas de textura son valores de punto flotante que hacen referencia a los datos de textura, lo que también se conoce como espacio de textura normalizado. Los modos de ajuste de direcciones se aplican en este orden (coordenadas de textura + desplazamientos + modo de ajuste) para modificar las coordenadas de textura fuera del \[ intervalo 0...1. \]

En el caso de las matrices de texturas, un valor adicional en el parámetro location especifica un índice en una matriz de textura. Este índice se trata como un valor float escalado (en lugar del espacio normalizado para las coordenadas de textura estándar). La conversión a un índice entero se realiza en el orden siguiente (float + entero round-to-nearest-even + fijación al intervalo de matriz).

### <a name="applying-texture-coordinate-offsets"></a>Aplicar desplazamientos de coordenadas de textura

El parámetro offset modifica las coordenadas de textura, en el espacio de textura. Aunque las coordenadas de textura son números de punto flotante normalizados, el desplazamiento aplica un desplazamiento entero. Tenga en cuenta también que los desplazamientos de textura deben ser estáticos.

El formato de datos devuelto viene determinado por el formato de textura. Por ejemplo, si el recurso de textura se definió con el formato DXGI FORMAT A8B8G8R8 UNORM SRGB, la operación de muestreo convierte los texeles muestreados de \_ \_ gamma \_ \_ 2.0 a 1.0, filtra y escribe el resultado como un valor de punto flotante en el \[ intervalo 0..1 \] .

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos de ejemplo](texture-sample-overload.md)
</dt> <dt>

[Texture-Object](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
