---
title: WaveActiveMin función)
description: Devuelve el valor mínimo de la expresión en todas las calles activas de la onda actual lo replica de nuevo en todas las calles activas.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- WaveActiveMin de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078602"
---
# <a name="waveactivemin-function"></a>WaveActiveMin función)

Devuelve el valor mínimo de la expresión en todas las calles activas de la onda actual lo replica de nuevo en todas las calles activas.

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

## <a name="remarks"></a>Observaciones

El orden de las operaciones es indefinido.

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




