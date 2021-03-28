---
title: WaveActiveBallot función)
description: Devuelve un uint4 que contiene una máscara de máscara de la evaluación de la expresión booleana para todas las calles activas de la ola actual.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- WaveActiveBallot de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104533597"
---
# <a name="waveactiveballot-function"></a>WaveActiveBallot función)

Devuelve un uint4 que contiene una máscara de máscara de la evaluación de la expresión booleana para todas las calles activas de la ola actual. 

## <a name="syntax"></a>Sintaxis

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*expr* 
</dt> <dd>

Expresión booleana que se va a evaluar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un uint4 que contiene una máscara de máscara de la evaluación de la expresión booleana para todas las calles activas de la ola actual. El bit menos significativo corresponde a la calle con el índice cero. Los bits correspondientes a las calles inactivas serán cero. Los bits que son mayores o iguales que [**WaveGetLaneCount**](wavegetlanecount.md) serán cero.

## <a name="remarks"></a>Observaciones

Diferentes GPU tienen distintos anchos de procesador SIMD (recuentos de carril). La mayoría de estas funciones **WaveXXX** pueden funcionar en el nivel de abstracción donde se oculta el ancho de la máquina SIMD. Para maximizar la portabilidad del código entre GPU, utilice los intrínsecos que no se basan en el ancho de la máquina. Por ejemplo, use:

``` syntax
uint result = WaveActiveCountBits( bBit );
```

En lugar de:

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




