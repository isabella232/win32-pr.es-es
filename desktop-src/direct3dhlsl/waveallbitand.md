---
title: Función WaveActiveBitAnd
description: Devuelve el AND bit a bit de todos los valores de la expresión en todos los sentidos activos de la onda actual y lo replica de nuevo en todos los sentidos activos.
ms.assetid: 602884CD-E656-4DEB-A30A-8A7D127A2217
keywords:
- Función HLSL de WaveActiveBitAnd
topic_type:
- apiref
api_name:
- WaveActiveBitAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96d09d91df4ff9226a8fb86203be0bd79bc3c11d1882553607358c3c84d3814c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283003"
---
# <a name="waveactivebitand-function"></a>Función WaveActiveBitAnd

Devuelve el AND bit a bit de todos los valores de la expresión en todos los sentidos activos de la onda actual y lo replica de nuevo en todos los sentidos activos.

## <a name="syntax"></a>Sintaxis


``` syntax
<int_type> WaveActiveBitAnd(
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

Valor AND bit a bit.

## <a name="remarks"></a>Comentarios

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




