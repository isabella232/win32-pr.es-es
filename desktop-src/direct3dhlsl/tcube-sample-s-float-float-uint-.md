---
title: Función TextureCube::Sample(S,float,float,uint)
description: Muestrea una textura con un valor opcional para fijar los valores de nivel de detalle (LOD) de la muestra y devuelve el estado de la operación. | Función TextureCube::Sample(S,float,float,uint)
ms.assetid: 8FA17583-9002-4DEC-A6D5-85B25DEA19B7
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
ms.openlocfilehash: 9a91e9a3dcc2df617f50175eb0872398bc564103
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070344"
---
# <a name="texturecubesamplesfloatfloatuint-function"></a>Función TextureCube::Sample(S,float,float,uint)

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



| Texture-Object type                    | Tipo de parámetro |
|----------------------------------------|----------------|
| Texture1D                              | FLOAT          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Fijación* \[ En\]
</dt> <dd>

Valor opcional al que se fijan los valores de LOD de ejemplo. Por ejemplo, si pasa 2,0f para el valor de la fijación, asegúrese de que ninguna muestra individual acceda a un nivel de mip inferior a 2,0f.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación Sample **,** **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se tomaron valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El formato de textura, que es uno de los valores con tipo enumerados en [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos de ejemplo](texturecube-sample.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
