---
title: Función TextureCubeArray::Sample(S,float,float,uint)
description: Muestrea una textura con un valor opcional para fijar los valores de nivel de detalle (LOD) de la muestra y devuelve el estado de la operación. | Función TextureCubeArray::Sample(S,float,float,uint)
ms.assetid: 5645841D-A32E-452E-873C-E070CF6A4C00
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
ms.openlocfilehash: 261da0f97251b2758ee8a69825e18168b206172994fa672ffd03e002652cb8c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117925"
---
# <a name="texturecubearraysamplesfloatfloatuint-function"></a>Función TextureCubeArray::Sample(S,float,float,uint)

Muestrea una textura con un valor opcional para fijar los valores de nivel de detalle (LOD) de la muestra y devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis


``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float        Location,
  in  float        Clamp,
  out uint         Status
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



| Texture-Object de datos                    | Tipo de parámetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Fijación* \[ En\]
</dt> <dd>

Valor opcional al que se fijan los valores de LOD de ejemplo. Por ejemplo, si pasa 2,0f para el valor de la fijación, asegúrese de que ninguna muestra individual tiene acceso a un nivel de mip inferior a 2,0f.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación Sample **,** **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se tomaron valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El formato de textura, que es uno de los valores con tipo enumerados [**en DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos de ejemplo](texturecubearray-sample.md)
</dt> <dt>

[**TextureCubeArray**](texturecubearray.md)
</dt> </dl>

 

 
