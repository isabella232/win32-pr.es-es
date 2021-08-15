---
title: Función SampleGrad::SampleGrad(S,float,float,float,int,float) para Texture2D
description: Muestrea un objeto Texture2D, usando un degradado para influir en la forma en que se calcula la ubicación de la muestra, con un valor opcional para fijar los valores de nivel de detalle (LOD) de la muestra. Para Texture2D.
ms.assetid: 1216B02A-4F70-4804-9B04-37E83DFC1CE8
keywords:
- Función SampleGrad HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b043b04480de5cfa709b31a951afc13d5432a3684e61b4d29f23e7157f13a16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510584"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture2d"></a>Función SampleGrad::SampleGrad(S,float,float,float,int,float) para Texture2D

Muestrea [**un objeto Texture2D**](sm5-object-texture2d.md), usando un degradado para influir en la forma en que se calcula la ubicación de la muestra, con un valor opcional para fijar los valores de nivel de detalle (LOD) de la muestra.

## <a name="syntax"></a>Sintaxis


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
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

*DDX* \[ en\]
</dt> <dd>

Tipo: **float**

Velocidad de cambio de la geometría de la superficie en la dirección x. El tipo de argumento depende del tipo texture-object.



| Texture-Object tipo                      | Tipo de parámetro |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | FLOAT          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | no admitido  |



 

</dd> <dt>

*DDY* \[ En\]
</dt> <dd>

Tipo: **float**

Velocidad de cambio de la geometría de la superficie en la dirección y. El tipo de argumento depende del tipo texture-object.



| Texture-Object tipo                      | Tipo de parámetro |
|------------------------------------------|----------------|
| Texture1D, Texture1DArray                | FLOAT          |
| Texture2D, Texture2DArray                | float2         |
| Texture3D, TextureCube, TextureCubeArray | float3         |
| Texture2DMS, Texture2DMSArray            | no admitido  |



 

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

[Métodos SampleGrad](texture2d-samplegrad.md)
</dt> </dl>

 

 
