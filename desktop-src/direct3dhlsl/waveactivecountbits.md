---
title: WaveActiveCountBits función)
description: Cuenta el número de variables Booleanas que se evalúan como true en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- WaveActiveCountBits de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c4d2db55e9e3a0ad8f0a66be183d6e39d2a8b9c
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2020
ms.locfileid: "104359551"
---
# <a name="waveactivecountbits-function"></a>WaveActiveCountBits función)

Cuenta el número de variables Booleanas que se evalúan como true en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda.

## <a name="syntax"></a>Sintaxis


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bBit* 
</dt> <dd>

Variables Booleanas que se van a evaluar. Proporcionar un valor booleano true explícito devuelve el número de calles activas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El número de que se evalúa como true en todas las calles activas de la ola actual.

## <a name="remarks"></a>Observaciones

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

Esto se puede implementar de forma más eficaz que un WaveActiveSum completo, tal y como se describe en el ejemplo siguiente:

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




