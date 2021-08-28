---
title: Función SampleLevel::SampleLevel(S,float,float,int,uint) para Texture2DArray
description: Muestrea una textura en el nivel de mapa mip especificado y devuelve el estado de la operación. Para Texture2DArray. | Función SampleLevel::SampleLevel(S,float,float,int,uint)
ms.assetid: 2A561EE4-D7CF-44D4-AC93-F6841770B868
keywords:
- Función SampleLevel HLSL
topic_type:
- apiref
api_name:
- SampleLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b00882702b44b7d4f9ccb101866400cb023cea00be637e898d9ecd71ed2e262
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118055"
---
# <a name="samplelevelsamplelevelsfloatfloatintuint-function-for-texture2darray"></a>Función SampleLevel::SampleLevel(S,float,float,int,uint) para Texture2DArray

Muestrea una textura en el nivel de mapa mip especificado y devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis


``` syntax
DXGI_FORMAT SampleLevel(
  in  SamplerState S,
  in  float        Location,
  in  float        LOD,
  in  int          Offset,
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

*LOD* \[ En\]
</dt> <dd>

Tipo: **float**

\[en \] Número que especifica el nivel de mapa mip. Si el valor es ≤ 0, se usa el nivel de mapa mip 0 (mapa más grande). El valor fraccionrio (si se proporciona) se usa para interpolar entre dos niveles de mapa mip.

</dd> <dt>

*Desplazamiento* \[ En\]
</dt> <dd>

Tipo: **int**

Desplazamiento de coordenadas de textura opcional, que se puede usar para cualquier tipo de objeto de textura; el desplazamiento se aplica a la ubicación antes del muestreo. Use un desplazamiento solo en un valor miplevel entero; De lo contrario, puede obtener resultados que no se traducen bien al hardware. El tipo de argumento depende del tipo texture-object. Para obtener más información, [vea Aplicar desplazamientos enteros.](dx-graphics-hlsl-to-sample.md)



| Texture-Object tipo           | Tipo de parámetro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | no admitido  |



 

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación **Sample**, **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se han tomado valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

Formato de textura, que es uno de los valores con tipo enumerados [**en DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos SampleLevel](texture2darray-samplelevel.md)
</dt> <dt>

[**Texture2DArray**](sm5-object-texture2darray.md)
</dt> </dl>

 

 
