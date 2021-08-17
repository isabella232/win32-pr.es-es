---
title: Función WaveActiveMax
description: Devuelve el valor máximo de la expresión en todos los carriles activos de la onda actual y la replica de nuevo en todos los carriles activos.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- Función WaveActiveMax HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c85936ca28aabe0365fd912b4d764739b0ab15765241a243ad67143dacd0d7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119484205"
---
# <a name="waveactivemax-function"></a>Función WaveActiveMax

Devuelve el valor máximo de la expresión en todos los carriles activos de la onda actual y la replica de nuevo en todos los carriles activos.

## <a name="syntax"></a>Sintaxis

``` syntax
<type> WaveActiveMax(
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

Valor máximo.

## <a name="remarks"></a>Comentarios

El orden de las operaciones es indefinido.

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader Model 6](shader-model-6-0.md)
</dt> </dl>

 

 




