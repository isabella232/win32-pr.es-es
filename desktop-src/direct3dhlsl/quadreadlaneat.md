---
title: QuadReadLaneAt función)
description: Devuelve el valor de origen especificado de la calle identificada por el ID. de calle dentro del cuádruple actual.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- QuadReadLaneAt de función HLSL
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488536"
---
# <a name="quadreadlaneat-function"></a>QuadReadLaneAt función)

Devuelve el valor de origen especificado de la calle identificada por el ID. de calle dentro del cuádruple actual.

## <a name="syntax"></a>Sintaxis


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Valor* 
</dt> <dd>

El tipo solicitado.

</dd> <dt>

*quadLaneID* 
</dt> <dd>

El identificador de la calle; Este será un valor de 0 a 3.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor de origen especificado. El resultado de esta función es uniforme en todo el cuádruple. Si la calle de origen está inactiva, los resultados son indefinidos.

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las cuádruples, consulte [información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).

Esta función se admite desde el modelo de sombreador 6,0 solo en los sombreadores de píxeles y de cálculo.



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




