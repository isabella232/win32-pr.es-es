---
title: 'TextureCubeArray:: sample (S, Float, float) (función)'
description: 'Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en. | TextureCubeArray:: sample (S, Float, float) (función)'
ms.assetid: E3BACA5E-18FC-4BD7-A8D8-C2808BDF1517
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
ms.openlocfilehash: 0f3f822ee334262dc50950064c6b4257aca3dd1f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986402"
---
# <a name="texturecubearraysamplesfloatfloat-function"></a>TextureCubeArray:: sample (S, Float, float) (función)

Muestrea una textura con un valor opcional para Clamp valores de nivel de detalle (LOD) de ejemplo en.

## <a name="syntax"></a>Sintaxis


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
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

[Métodos de ejemplo](texturecubearray-sample.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
