---
title: 'Texture1D:: sample (S, Float, int, float) (función)'
description: 'Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. | Texture1D:: sample (S, Float, int, float) (función)'
ms.assetid: D2E2E143-8240-43AA-AD70-BD793B3CFD19
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
ms.openlocfilehash: f119955a66f7aec336ce52d730d54a5f11756527
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083664"
---
# <a name="texture1dsamplesfloatintfloat-function"></a>Texture1D:: sample (S, Float, int, float) (función)

Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.

## <a name="syntax"></a>Sintaxis


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
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

*Desplazamiento* \[ de\]
</dt> <dd>

Tipo: **int**

Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura. el desplazamiento se aplica a la ubicación antes del muestreo. Use un desplazamiento solo en un entero miplevel; de lo contrario, puede obtener resultados que no se traduzcan bien al hardware. El tipo de argumento depende del tipo de objeto de textura. Para obtener más información, vea [aplicar desplazamientos enteros](dx-graphics-hlsl-to-sample.md).



| Tipo de Texture-Object           | Tipo de parámetro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | no admitido  |



 

</dd> <dt>

*Abrazadera* \[ de\]
</dt> <dd>

Tipo: **float**

Un valor opcional en el que se van a fijar los valores LOD de ejemplo. Por ejemplo, si se pasa 2.0 f para el valor Clamp, se asegura de que ningún ejemplo individual tenga acceso a un nivel de MIP inferior a 2.0 f.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Formato de textura, que es uno de los valores con tipo que aparecen [**en \_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos de ejemplo](texture1d-sample.md)
</dt> </dl>

 

 
