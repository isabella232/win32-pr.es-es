---
title: WaveActiveSum función)
description: Suma el valor de la expresión en todas las calles activas de la ola actual y lo replica en todas las calles de la ola actual.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- WaveActiveSum de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b98ecf2521841b9da73e1b917d44f1d91b7876d2
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995734"
---
# <a name="waveactivesum-function"></a>WaveActiveSum función)

Suma el valor de la expresión en todas las calles activas de la ola actual y lo replica en todas las calles de la ola actual.

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

## <a name="remarks"></a>Observaciones

El orden de las operaciones es indefinido.

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




