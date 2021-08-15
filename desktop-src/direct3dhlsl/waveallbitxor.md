---
title: Función WaveActiveBitXor
description: Devuelve el XOR bit a bit de todos los valores de la expresión en todos los carriles activos de la ola actual y lo replica de nuevo en todos los carriles activos.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- Función WaveActiveBitXor HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 733ab8c40a59b784af8a7d50c4f8e1e543f344ee2d75ed9b6896992e6176ff18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504885"
---
# <a name="waveactivebitxor-function"></a>Función WaveActiveBitXor

Devuelve el XOR bit a bit de todos los valores de la expresión en todos los carriles activos de la ola actual y lo replica de nuevo en todos los carriles activos.

## <a name="syntax"></a>Sintaxis

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*expr* 
</dt> <dd>

La expresión que se va a evaluar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Valor XOR bit a bit.

## <a name="remarks"></a>Comentarios

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader Model 6](shader-model-6-0.md)
</dt> </dl>

 

 




