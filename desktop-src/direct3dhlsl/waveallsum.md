---
title: Función WaveActiveSum
description: Suma el valor de la expresión en todos los calles activas de la onda actual y la replica en todos los sentidos de la onda actual.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- Función HlSL de WaveActiveSum
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 403768b875ed9462b79fb5d0abeee9539189597591f3a3b20f5a3b9662995542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742265"
---
# <a name="waveactivesum-function"></a>Función WaveActiveSum

Suma el valor de la expresión en todos los calles activas de la onda actual y la replica en todos los sentidos de la onda actual.

## <a name="syntax"></a>Sintaxis

``` syntax
<type> WaveActiveSum(
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

Valor de suma.

## <a name="remarks"></a>Comentarios

El orden de las operaciones es indefinido.

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




