---
description: La función Int64x32Div32 implementa la fórmula ((a b)+rnd)/c, donde a es un valor de 64 bits y b, c y rnd son valores de \* 32 bits.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Función Int64x32Div32 (Wxutil.h)
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
ms.openlocfilehash: a56425d1f07346f8e546940ff5880416e4e63efc692974c78f0e344b9ec01c5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051595"
---
# <a name="int64x32div32-function"></a>Función Int64x32Div32

La función implementa la fórmula donde es un valor de `Int64x32Div32` `((a*b)+rnd)/c` 64 bits y *b*, *c* y *rnd* son valores de 32 bits. 

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

El redondeo de la división es hacia cero. La división por cero se cuenta como una condición de desbordamiento.

Las marcas de tiempo y las horas de búsqueda son valores de 64 bits, por lo que esta función es útil para realizar conversiones en sistemas de 32 bits. Por ejemplo, en MPEG-1, la referencia del reloj del sistema es de 90 kHz o 90 000 tics por segundo. La fórmula para convertir esto en tiempo de referencia (unidades de 100 nanosegundos) es


```C++
(timestamp * 1000) / 9
```



que se puede calcular como `Int64x32Div32(timestamp, 1000, 9, 0)` . Use el *parámetro rnd* como factor de redondeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxutil.h (incluir Secuencias.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares misceláneas](miscellaneous-helper-functions.md)
</dt> <dt>

[**llMulDiv**](llmuldiv.md)
</dt> </dl>

 

 




