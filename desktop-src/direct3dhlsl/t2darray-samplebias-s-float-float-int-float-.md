---
title: Función SampleBias::SampleBias(S,float,float,int,float) para Texture2DArray
description: La función SampleBias::SampleBias(S,float,float,int,float) para Texture2DArray muestrea una textura después de aplicar el valor de sesgo al nivel mipmap.
ms.assetid: CC399CB8-1BD8-4CDE-9BFF-66A8917FDAFC
keywords:
- Función SampleBias HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39acbe329effb206b26685ac150ed8a5a8d310fc7698b2c4508e78b9ed7ed0c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276345"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture2darray"></a>Función SampleBias::SampleBias(S,float,float,int,float) para Texture2DArray

Muestrea una textura, después de aplicar el valor de sesgo al nivel de mapa mip, con un valor opcional para fijar los valores de nivel de detalle (LOD) de la muestra.

## <a name="syntax"></a>Sintaxis


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*S* \[ en\]
</dt> <dd>

Tipo: **SamplerState**

Un [estado sampler](dx-graphics-hlsl-sampler.md). Se trata de un objeto declarado en un archivo de efecto que contiene asignaciones de estado.

</dd> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **float**

Las coordenadas de textura. El tipo de argumento depende del tipo texture-object.



| Texture-Object tipo                    | Tipo de parámetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Sesgo* \[ En\]
</dt> <dd>

Tipo: **float**

El valor de sesgo, que es un número de punto flotante entre 0,0 y 1,0 inclusive, se aplica a un nivel de mip antes del muestreo.

</dd> <dt>

*Desplazamiento* \[ En\]
</dt> <dd>

Tipo: **int**

Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura; el desplazamiento se aplica a la ubicación antes del muestreo. Use un desplazamiento solo en un valor miplevel entero; De lo contrario, puede obtener resultados que no se traducen bien al hardware. El tipo de argumento depende del tipo texture-object. Para obtener más información, [vea Aplicar desplazamientos de enteros.](dx-graphics-hlsl-to-sample.md)



| Texture-Object tipo           | Tipo de parámetro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | no admitido  |



 

</dd> <dt>

*Fijación* \[ En\]
</dt> <dd>

Tipo: **float**

Valor opcional al que se fijan los valores de LOD de ejemplo. Por ejemplo, si pasa 2,0f para el valor de fijación, asegúrese de que ninguna muestra individual tiene acceso a un nivel de mip inferior a 2,0f.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Formato de textura, que es uno de los valores con tipo enumerados [**en DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos SampleBias](texture2darray-samplebias.md)
</dt> </dl>

 

 
