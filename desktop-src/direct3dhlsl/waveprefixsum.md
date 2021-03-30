---
title: 'Función WavePrefixSum '
description: Devuelve la suma de todos los valores de las calles activas con índices más pequeños que este.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- WavePrefixSum de función HLSL
topic_type:
- apiref
api_name:
- WavePrefixSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b133aa37b522156df73914eef66c4d3695a70ed7
ms.sourcegitcommit: 41c742c88f7d9ce05e107008f186b6e872ff9288
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/31/2021
ms.locfileid: "104986151"
---
# <a name="waveprefixsum-function"></a>Función WavePrefixSum 

Devuelve la suma de todos los valores de las calles activas con índices más pequeños que este.

## <a name="syntax"></a>Sintaxis

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a>Parámetros

*value* 

Valor que se va a sumar.

## <a name="return-value"></a>Valor devuelto

Suma de los valores de.

## <a name="remarks"></a>Observaciones

No se puede garantizar el orden de las operaciones en esta rutina. Por lo tanto, de hecho, \[ \] se omite la marca precisa dentro de ella.

Una suma de postfijo se puede calcular agregando la suma del prefijo al valor de la calle actual.

Tenga en cuenta que la calle activa con el índice más bajo siempre recibirá un 0 para su suma de prefijo.

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 

## <a name="examples"></a>Ejemplos

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

En una máquina con un tamaño de onda de 8 y todas las calles activas excepto las calles 0 y 4, los siguientes valores se devolverían desde WavePrefixSum.

| Índice de Lane | status   | prefixSum     | 
|------------|----------|---------------|
| 0          | inactivo | N/D           |
| 1          | active   | = 0           |
| 2          | active   | = 0 + 2         |
| 3          | active   | = 0 + 2 + 2       |
| 4          | inactivo | N/D           |
| 5          | active   | = 0 + 2 + 2 + 2     |
| 6          | active   | = 0 + 2 + 2 + 2 + 2   |
| 7          | active   | = 0 + 2 + 2 + 2 + 2 + 2 |

## <a name="see-also"></a>Vea también

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Modelo de sombreador 6](shader-model-6-0.md)
