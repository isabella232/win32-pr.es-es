---
title: Función Texture1DArray::Sample(S,float,int,float,uint)
description: Muestrea una textura con un valor opcional para fijar los valores de nivel de detalle (LOD) de la muestra a y devuelve el estado de la operación. | Función Texture1DArray::Sample(S,float,int,float,uint)
ms.assetid: 584901B7-4F58-4491-9543-F27433386292
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
ms.openlocfilehash: 4a2f608d7dbbd4eec51139b6f285529849f708af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966491"
---
# <a name="texture1darraysamplesfloatintfloatuint-function"></a>Función Texture1DArray::Sample(S,float,int,float,uint)

Muestrea una textura con un valor opcional para fijar los valores de nivel de detalle (LOD) de la muestra a y devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
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

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación **Sample**, **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se tomaron valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Formato de textura, que es uno de los valores con tipo enumerados [**en DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos de ejemplo](texture1darray-sample.md)
</dt> </dl>

 

 
