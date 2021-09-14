---
title: 'Función WavePrefixSum '
description: Devuelve la suma de todos los valores de los carriles activos con índices más pequeños que este.
ms.assetid: F51B90AB-3E85-4521-8A2C-7C16A4ECB1F9
keywords:
- Función WavePrefixSum HLSL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888105"
---
# <a name="waveprefixsum-function"></a>Función WavePrefixSum 

Devuelve la suma de todos los valores de los carriles activos con índices más pequeños que este.

## <a name="syntax"></a>Sintaxis

``` syntax
<type> WavePrefixSum(
   <type> value
);
```

## <a name="parameters"></a>Parámetros

*value* 

Valor que se suma.

## <a name="return-value"></a>Valor devuelto

Suma de los valores.

## <a name="remarks"></a>Observaciones

No se puede garantizar el orden de las operaciones en esta rutina. Por lo tanto, de \[ forma eficaz, \] la marca precisa se omite dentro de ella.

Una suma de postfijo se puede calcular agregando la suma del prefijo al valor del lane actual.

Tenga en cuenta que el carril activo con el índice más bajo siempre recibirá un 0 para su suma de prefijo.

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 

## <a name="examples"></a>Ejemplos

```hlsl
uint numToSum = 2;
uint prefixSum = WavePrefixSum( numToSum );
```

En una máquina con un tamaño de onda de 8 y todos los carriles activos excepto los 0 y 4, se devolverían los siguientes valores de WavePrefixSum.

| lane index | status   | prefixSum     | 
|------------|----------|---------------|
| 0          | inactivo | N/D           |
| 1          | active   | = 0           |
| 2          | active   | = 0+2         |
| 3          | active   | = 0+2+2       |
| 4          | inactivo | N/D           |
| 5          | active   | = 0+2+2+2     |
| 6          | active   | = 0+2+2+2+2   |
| 7          | active   | = 0+2+2+2+2+2 |

## <a name="see-also"></a>Consulte también

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Shader Model 6](shader-model-6-0.md)
