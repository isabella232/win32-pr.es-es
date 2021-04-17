---
description: La función Int64x32Div32 implementa la fórmula ((a \* b) + RND)/c, donde a es un valor de 64 bits y b, c y RND son valores de 32 bits.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Función Int64x32Div32 (Wxutil. h)
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
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680962"
---
# <a name="int64x32div32-function"></a>Int64x32Div32 función)

La `Int64x32Div32` función implementa la fórmula `((a*b)+rnd)/c` donde *a* es un valor de 64 bits y *b*, *c* y *RND* son valores de 32 bits.

## <a name="syntax"></a>Sintaxis


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*un* 
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

*NúmAleat* 
</dt> <dd>

Factor de redondeo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el `(a * b + rnd)/c` cálculo o uno de los valores siguientes.



| Código devuelto                                                                                       | Descripción                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**0x7FFFFFFFFFFFFFFF**</dt> </dl> | Se produjo un desbordamiento porque el resultado es demasiado grande (positivo).<br/> |
| <dl> <dt>**0x8000000000000000**</dt> </dl> | Se produjo un desbordamiento porque el resultado es demasiado grande (negativo).<br/> |



 

## <a name="remarks"></a>Observaciones

El redondeo en la división es hacia cero. La división por cero se cuenta como una condición de desbordamiento.

Las marcas de tiempo y los tiempos de búsqueda son valores de 64 bits, por lo que esta función es útil para realizar conversiones en sistemas de 32 bits. Por ejemplo, en MPEG-1, la referencia del reloj del sistema es 90 kHz o 90.000 TICs por segundo. La fórmula que se va a convertir en el tiempo de referencia (unidades 100-nanosegundos) es


```C++
(timestamp * 1000) / 9
```



que se puede calcular como `Int64x32Div32(timestamp, 1000, 9, 0)` . Use el parámetro *RND* como factor de redondeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil. h (incluir streams. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares misceláneas](miscellaneous-helper-functions.md)
</dt> <dt>

[**llMulDiv**](llmuldiv.md)
</dt> </dl>

 

 




