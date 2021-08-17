---
description: La función llMulDiv implementa la fórmula ((a \* b)+rnd)/c, donde cada término es un valor de 64 bits.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: Función llMulDiv (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df58175955106906027a6d2d10c465b82ad6313cd493e3ef9ef3ba279cd0115f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952354"
---
# <a name="llmuldiv-function"></a>función llMulDiv

La `llMulDiv` función implementa la fórmula donde cada término es un valor de `((a*b)+rnd)/c` 64 bits.

Las marcas de tiempo y los tiempos de búsqueda son valores de 64 bits, por lo que esta función es útil para realizar conversiones en sistemas de 32 bits. Por ejemplo, la fórmula para bytes por segundo es


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



que se puede calcular como `llMulDiv(nBytes, rtTime, 10000000, 0)` . Use el *parámetro rnd* como factor de redondeo.

## <a name="syntax"></a>Sintaxis


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Un* 
</dt> <dd>

Multiplicando.

</dd> <dt>

*b* 
</dt> <dd>

Multiplicador.

</dd> <dt>

*c* 
</dt> <dd>

Divisor.

</dd> <dt>

*Rnd* 
</dt> <dd>

Factor de redondeo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el `(a * b + rnd)/c` cálculo o uno de los valores siguientes.



| Código devuelto                                                                                       | Descripción                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**0x7FFFFFFFFFFFFFFF**</dt> </dl> | Se produjo un desbordamiento porque el resultado es demasiado grande (positivo).<br/> |
| <dl> <dt>**0x8000000000000000**</dt> </dl> | Se produjo un desbordamiento porque el resultado es demasiado grande (negativo).<br/> |



 

## <a name="remarks"></a>Comentarios

El redondeo en la división es hacia cero. La división por cero se cuenta como una condición de desbordamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares misceláneas](miscellaneous-helper-functions.md)
</dt> <dt>

[**Int64x32Div32**](int64x32div32.md)
</dt> </dl>

 

 




