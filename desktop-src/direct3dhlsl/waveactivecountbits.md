---
title: Función WaveActiveCountBits
description: Cuenta el número de variables booleanas que se evalúan como true en todos los carriles activos de la ola actual y replica el resultado en todos los carriles de la onda.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- Función WaveActiveCountBits HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a53a2953ba7d77f1969a7d5dabef3c17437e8bbb
ms.sourcegitcommit: 8d7ce0c4827f8a4fd501cc6487f1a8360e944577
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/24/2021
ms.locfileid: "122767609"
---
# <a name="waveactivecountbits-function"></a>Función WaveActiveCountBits

Cuenta el número de variables booleanas que se evalúan como true en todos los carriles activos de la ola actual y replica el resultado en todos los carriles de la onda.

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

Variables booleanas que se evaluarán. Si se proporciona un valor booleano verdadero explícito, se devuelve el número de rutas activas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Número de rutas para las que la variable booleana se evalúa como true en todos los carriles activos de la ola actual.

## <a name="remarks"></a>Observaciones

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

Esto se puede implementar de forma más eficaz que un waveActiveSum completo, como se describe en el ejemplo siguiente:

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader Model 6](shader-model-6-0.md)
</dt> </dl>

 

 




