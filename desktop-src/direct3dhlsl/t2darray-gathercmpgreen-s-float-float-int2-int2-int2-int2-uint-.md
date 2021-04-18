---
title: 'Texture2DArray:: GatherCmpGreen (S, Float, Float, INT2, INT2, INT2, INT2, uint) (función)'
description: 'En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente verde con respecto a un valor de comparación junto con el estado de asignación de mosaicos. | Texture2DArray:: GatherCmpGreen (S, Float, Float, INT2, INT2, INT2, INT2, uint) (función)'
ms.assetid: 53AC1FE7-ECC8-489B-8FEF-5028009BC080
keywords:
- GatherCmpGreen de función HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9878e5e9474717be9842887b2945591d5883cb07
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986653"
---
# <a name="texture2darraygathercmpgreensfloatfloatint2int2int2int2uint-function"></a>Texture2DArray:: GatherCmpGreen (S, Float, Float, INT2, INT2, INT2, INT2, uint) (función)

En el caso de cuatro valores de textura que se utilizarían en una operación de filtrado bilineal, devuelve una comparación de su componente verde con respecto a un valor de comparación junto con el estado de asignación de mosaicos.

## <a name="syntax"></a>Sintaxis


``` syntax
TemplateType GatherCmpGreen(
  in  SamplerState S,
  in  float        Location,
  in  float        CompareValue,
  in  int2         Offset1,
  in  int2         Offset2,
  in  int2         Offset3,
  in  int2         Offset4,
  out uint         Status
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*S* \[ en\]
</dt> <dd>

Tipo: **SamplerState**

Índice de muestra de base cero.

</dd> <dt>

*Ubicación* \[ de de\]
</dt> <dd>

Tipo: **float**

Coordenadas de ejemplo (u, v).

</dd> <dt>

*CompareValue* \[ de\]
</dt> <dd>

Tipo: **float**

Valor que se va a comparar cada uno con cada valor muestreado.

</dd> <dt>

*Offset1* \[ de\]
</dt> <dd>

Tipo: **INT2**

Primer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset2* \[ de\]
</dt> <dd>

Tipo: **INT2**

Segundo componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset3* \[ de\]
</dt> <dd>

Tipo: **INT2**

Tercer componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Offset4* \[ de\]
</dt> <dd>

Tipo: **INT2**

Cuarto componente de desplazamiento aplicado a las coordenadas de textura antes del muestreo.

</dd> <dt>

*Estado* \[ de enuncia\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede tener acceso directamente al estado. en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** devuelve **true** si todos los valores de la operación de **ejemplo**, **recopilación** o **carga** correspondiente han tenido acceso a los mosaicos asignados en un [recurso en mosaico](/windows/desktop/direct3d11/direct3d-11-2-features). Si se tomó algún valor de un mosaico sin asignar, **CheckAccessFullyMapped** devuelve **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **TemplateType**

Un valor de cuatro componentes cuyo tipo es el mismo que el tipo de plantilla.

## <a name="remarks"></a>Observaciones

Los ejemplos de textura se pueden usar para la interpolación bilineal.

Esta función se admite para los siguientes tipos de sombreadores:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos GatherCmpGreen](texture2darray-gathercmpgreen.md)
</dt> </dl>

 

 
