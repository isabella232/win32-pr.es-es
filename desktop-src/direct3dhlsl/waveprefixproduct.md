---
title: 'Función WavePrefixProduct '
description: Devuelve el producto de todos los valores de las calles activas en esta ola con índices inferiores a esta calle.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- WavePrefixProduct de función HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d073d72590951ddbbbb74274d4cd237e0a138c4f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421623"
---
# <a name="waveprefixproduct-function"></a>Función WavePrefixProduct 

Devuelve el producto de todos los valores de las calles activas en esta ola con índices inferiores a esta calle.

## <a name="syntax"></a>Sintaxis

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a>Parámetros

*value* 

Valor que se va a multiplicar.

## <a name="return-value"></a>Valor devuelto

Producto de todos los valores.

## <a name="remarks"></a>Observaciones

No se puede garantizar el orden de las operaciones en esta rutina. Por lo tanto, de hecho, \[ \] se omite la marca precisa dentro de ella.

Un producto postfijo se puede calcular multiplicando el prefijo del producto por el valor de la calle actual.

Tenga en cuenta que la calle activa con el índice más bajo siempre recibirá un 1 para su producto de prefijo.

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 

## <a name="examples"></a>Ejemplos

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

En una máquina con un tamaño de onda de 8 y todas las calles activas excepto las calles 0 y 4, los siguientes valores se devolverían desde WavePrefixProduct.

| Índice de Lane | status   | prefixProduct | 
|------------|----------|---------------|
| 0          | inactivo | N/D           |
| 1          | active   | = 1           |
| 2          | active   | = 1 \* 2        |
| 3          | active   | = 1 \* 2 \* 2     |
| 4          | inactivo | N/D           |
| 5          | active   | = 1 \* 2 \* 2 2 \*       |
| 6          | active   | = 1 \* 2 \* 2 \* 2 \* 2    |
| 7          | active   | = 1 \* 2 \* 2 \* 2 \* 2 \* 2 |

## <a name="see-also"></a>Vea también

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Modelo de sombreador 6](shader-model-6-0.md)
