---
title: Función WaveActiveBallot
description: Devuelve un uint4 que contiene una máscara de bits de la evaluación de la expresión booleana para todos los calles activos de la onda actual.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- Función HLSL de WaveActiveBallot
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40b6c4651ba99bf97f8ec3c57e31cceca23fe3907b67f81e93080d0a853c2301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119369375"
---
# <a name="waveactiveballot-function"></a>Función WaveActiveBallot

Devuelve un uint4 que contiene una máscara de bits de la evaluación de la expresión booleana para todos los calles activos de la onda actual. 

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

Expresión booleana que se evaluará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un uint4 que contiene una máscara de bits de la evaluación de la expresión booleana para todos los calles activos de la onda actual. El bit menos significativo corresponde al lane con índice cero. Los bits correspondientes a los calles inactivos serán cero. Los bits que son mayores o iguales que [**WaveGetLaneCount**](wavegetlanecount.md) serán cero.

## <a name="remarks"></a>Comentarios

Las GPU diferentes tienen anchos de procesador SIMD diferentes (recuentos de líneas). La mayoría de **estas funciones WaveXXX** pueden funcionar en el nivel de abstracción donde el ancho de la máquina SIMD está oculto. Para maximizar la portabilidad del código entre GPU, use los intrínsecos que no se basan en el ancho de la máquina. Por ejemplo, use:

``` syntax
uint result = WaveActiveCountBits( bBit );
```

En lugar de:

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




