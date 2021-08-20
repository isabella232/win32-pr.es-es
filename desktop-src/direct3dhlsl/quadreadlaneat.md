---
title: Función QuadReadLaneAt
description: Devuelve el valor de origen especificado del camino identificado por el identificador de la calle dentro del cuadrándido actual.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- Función HLSL de QuadReadLaneAt
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6c06fc1118496c0f87b39ea73dfa9a515d2f2f684eb7258979c7c93dfc4eea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088651"
---
# <a name="quadreadlaneat-function"></a>Función QuadReadLaneAt

Devuelve el valor de origen especificado del camino identificado por el identificador de la calle dentro del cuadrándido actual.

## <a name="syntax"></a>Sintaxis


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sourceValue* 
</dt> <dd>

Tipo solicitado.

</dd> <dt>

*quadLaneID* 
</dt> <dd>

El identificador de la calle; será un valor de 0 a 3.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor de origen especificado. El resultado de esta función es uniforme en el cuadrándular. Si el carril de origen está inactivo, los resultados no están definidos.

## <a name="remarks"></a>Comentarios

Para obtener más información sobre los cuatros, consulte [Información general del modelo de sombreador 6.](hlsl-shader-model-6-0-features-for-direct3d-12.md)

Esta función solo se admite desde el modelo de sombreador 6.0 en sombreadores de cálculo y píxeles.



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Shader Model 6](shader-model-6-0.md)
</dt> </dl>

 

 




