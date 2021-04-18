---
title: 'Función SampleBias:: SampleBias (S, Float, Float, float) para TextureCube'
description: 'La función SampleBias:: SampleBias (S, Float, Float, float) para TextureCube muestrea una textura, después de aplicar el valor de Bias al nivel de mipmap.'
ms.assetid: BCDDADD9-D8B0-47C9-A312-5E6AF9C3C07B
keywords:
- SampleBias de función HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55404f2e32f45e5b19e7b0cd4c109a6d5a8bcc13
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187690"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecube"></a>Función SampleBias:: SampleBias (S, Float, Float, float) para TextureCube

Muestrea una textura, después de aplicar el valor de diferencia al nivel de mipmap, con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.

## <a name="syntax"></a>Sintaxis


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*S* \[ en\]
</dt> <dd>

Tipo: **SamplerState**

Un [Estado de muestra](dx-graphics-hlsl-sampler.md). Se trata de un objeto declarado en un archivo de efectos que contiene las asignaciones de estado.

</dd> <dt>

*Ubicación* \[ de de\]
</dt> <dd>

Tipo: **float**

Las coordenadas de textura. El tipo de argumento depende del tipo de objeto de textura.



| Tipo de Texture-Object                    | Tipo de parámetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Bias* \[ de\]
</dt> <dd>

Tipo: **float**

El valor de diferencia, que es un número de punto flotante entre 0,0 y 1,0, ambos inclusive, se aplica a un nivel de MIP antes del muestreo.

</dd> <dt>

*Abrazadera* \[ de\]
</dt> <dd>

Tipo: **float**

Un valor opcional en el que se van a fijar los valores LOD de ejemplo. Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos SampleBias](texturecube-samplebias.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
