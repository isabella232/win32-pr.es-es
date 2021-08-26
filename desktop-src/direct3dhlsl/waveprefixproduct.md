---
title: 'Función WavePrefixProduct '
description: Devuelve el producto de todos los valores de los canales activos de esta ola con índices menores que este.
ms.assetid: 3A5B271D-EF45-4511-9086-A9AD0D215D9A
keywords:
- Función WavePrefixProduct HLSL
topic_type:
- apiref
api_name:
- WavePrefixProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8cb780f951433afc480c38d52c8120e086a91d32117fe9bb566657e0fcf9f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948965"
---
# <a name="waveprefixproduct-function"></a>Función WavePrefixProduct 

Devuelve el producto de todos los valores de los canales activos de esta ola con índices menores que este.

## <a name="syntax"></a>Sintaxis

``` syntax
<type> WavePrefixProduct(
   <type> value
);
```

## <a name="parameters"></a>Parámetros

*value* 

Valor que se debe multiplicar.

## <a name="return-value"></a>Valor devuelto

Producto de todos los valores.

## <a name="remarks"></a>Comentarios

No se puede garantizar el orden de las operaciones en esta rutina. Por lo tanto, de \[ forma eficaz, \] la marca precisa se omite dentro de ella.

Un producto postfijo se puede calcular multiplicando el producto de prefijo por el valor del lane actual.

Tenga en cuenta que el camino activo con el índice más bajo siempre recibirá un 1 para su producto de prefijo.

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 

## <a name="examples"></a>Ejemplos

```hlsl
uint numToMultiply = 2;
uint prefixProduct = WavePrefixProduct( numToMultiply );
```

En una máquina con un tamaño de onda de 8 y todos los canales activos excepto los de los sentidos 0 y 4, se devolverían los siguientes valores de WavePrefixProduct.

| lane index | status   | prefixProduct | 
|------------|----------|---------------|
| 0          | inactivo | N/D           |
| 1          | active   | = 1           |
| 2          | active   | = 1 \* 2        |
| 3          | active   | = 1 \* 2 \* 2     |
| 4          | inactivo | N/D           |
| 5          | active   | = 1 \* 2 \* 2 \* 2       |
| 6          | active   | = 1 \* 2 \* 2 \* 2 \* 2    |
| 7          | active   | = 1 \* 2 \* 2 \* 2 \* 2 \* 2 |

## <a name="see-also"></a>Vea también

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)

[Modelo de sombreador 6](shader-model-6-0.md)
