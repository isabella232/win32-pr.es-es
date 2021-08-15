---
title: Función WaveActiveMin
description: Devuelve el valor mínimo de la expresión en todos los calles activas de la onda actual y la replica de nuevo en todos los sentidos activos.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- Función WaveActiveMin HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b97f2e58449e8b33270318f305a6fee87662a6aac4643b35152024366bf8b08b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721792"
---
# <a name="waveactivemin-function"></a>Función WaveActiveMin

Devuelve el valor mínimo de la expresión en todos los calles activas de la onda actual y la replica de nuevo en todos los sentidos activos.

## <a name="syntax"></a>Sintaxis

``` syntax
<type> WaveActiveMin(
   <type> expr
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*expr* 
</dt> <dd>

La expresión que se va a evaluar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor mínimo.

## <a name="remarks"></a>Comentarios

El orden de las operaciones es indefinido.

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




