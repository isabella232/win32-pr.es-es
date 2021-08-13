---
title: Función WaveActiveCountBits
description: Cuenta el número de variables booleanas que se evalúan como true en todos los sentidos activos de la onda actual y replica el resultado en todos los sentidos de la onda.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- Función HLSL de WaveActiveCountBits
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e1642cbd5cbdef162511185e9d2c05e849d78486b82e8219623286f33e39223
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504940"
---
# <a name="waveactivecountbits-function"></a>Función WaveActiveCountBits

Cuenta el número de variables booleanas que se evalúan como true en todos los sentidos activos de la onda actual y replica el resultado en todos los sentidos de la onda.

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

Variables booleanas que se evaluarán. Si se proporciona un valor booleano verdadero explícito, se devuelve el número de pistas activas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El número de que se evalúa como true en todos los sentidos activos de la ola actual.

## <a name="remarks"></a>Comentarios

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

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




