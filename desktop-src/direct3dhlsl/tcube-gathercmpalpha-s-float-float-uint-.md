---
title: Función TextureCube::GatherCmpAlpha(S,float,float,uint)
description: Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente alfa con un valor de comparación junto con el estado de asignación de mosaicos. | Función TextureCube::GatherCmpAlpha(S,float,float,uint)
ms.assetid: 8DC43B02-0B3C-49F0-AA94-80894A1A54BD
keywords:
- Función HLSL de GatherCmpAlpha
topic_type:
- apiref
api_name:
- GatherCmpAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 447328be61709dfe6cfdf0910f0ee468fa59e2b16095f1b59eb087434aedd822
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506514"
---
# <a name="texturecubegathercmpalphasfloatfloatuint-function"></a>Función TextureCube::GatherCmpAlpha(S,float,float,uint)

Para cuatro valores de texel que se usarían en una operación de filtrado bi linear, devuelve una comparación de su componente alfa con un valor de comparación junto con el estado de asignación de mosaicos.

## <a name="syntax"></a>Sintaxis


``` syntax
TemplateType GatherCmpAlpha(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  out uint         Status
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*S* \[ en\]
</dt> <dd>

Tipo: **SamplerState**

Índice de sampler de base cero.

</dd> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **float**

Coordenadas de ejemplo (u,v).

</dd> <dt>

*CompareValue* \[ En\]
</dt> <dd>

Tipo: **float**

Valor que se compara con cada valor muestreado.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación **Sample**, **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se tomaron valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Comentarios

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Métodos GatherCmpAlpha](texturecube-gathercmpalpha.md)
</dt> <dt>

[**TextureCube**](texturecube.md)
</dt> </dl>

 

 
