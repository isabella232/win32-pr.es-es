---
title: WaveActiveMax función)
description: Devuelve el valor máximo de la expresión en todas las calles activas de la ola actual y lo replica de nuevo en todas las calles activas.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- WaveActiveMax de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2020
ms.locfileid: "104421676"
---
# <a name="waveactivemax-function"></a>WaveActiveMax función)

Devuelve el valor máximo de la expresión en todas las calles activas de la ola actual y lo replica de nuevo en todas las calles activas.

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

## <a name="remarks"></a>Observaciones

El orden de las operaciones es indefinido.

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




