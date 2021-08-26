---
title: EM_SETFONTSIZE mensaje (Richedit.h)
description: Establece el tamaño de fuente del texto seleccionado en un control de edición enriquecido.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- EM_SETFONTSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e646d58626a034f4764d6b9636e5b4b3eedba5befd7986eade9979c1f4a4fd5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048465"
---
# <a name="em_setfontsize-message"></a>Mensaje \_ EM SETFONTSIZE

Establece el tamaño de fuente del texto seleccionado en un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Cambiar el tamaño de punto del texto seleccionado. El resultado se redondeará según los valores que se muestran en la tabla siguiente. Este parámetro debe estar en el intervalo de -1637 a 1638. El tamaño de fuente resultante estará dentro del intervalo de 1 a 1638.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si no se ha producido ningún error, el valor devuelto es **TRUE.**

Si se produjo un error, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Comentarios

Puede obtener fácilmente el tamaño de fuente enviando el [**mensaje \_ EM GETCHARFORMAT.**](em-getcharformat.md)

Rich Edit agrega *primero wParam* al tamaño de fuente actual y, a continuación, usa el tamaño resultante y la tabla siguiente para determinar el valor de redondeo.



| Banda    | Valor de redondeo |
|---------|----------------|
| <=12 | 1              |
| 28      | 2              |
| 36      | 0              |
| 48      | 0              |
| 72      | 0              |
| 80      | 0              |
| > 80 | 10             |



 

Si el tamaño de fuente resultante no es divisible uniformemente por el valor de redondeo, el tamaño de fuente se redondea a un número divisible uniformemente por el valor de redondeo. Por lo tanto, si el tamaño de fuente es menor o igual que 12, el valor de redondeo será 1. De forma similar, si el tamaño de fuente es menor o igual que 28, el valor de redondeo es 2. Para los valores mayores que 28, los tamaños de fuente se redondea a la banda siguiente. Por lo tanto, el tamaño de fuente salta a 36, 48, 72, 80. Después de 80, todo el redondeo se realiza en incrementos de diez puntos.

El tamaño de fuente se redondea hacia arriba o hacia abajo según el signo *de wParam*. Si *wParam es* positivo, el redondeo siempre está hacia arriba. De lo contrario, el redondeo siempre está hacia abajo. Por lo tanto, si el tamaño de fuente actual es 10 y *wParam* es 3, el tamaño de fuente resultante sería 14 (10 + 3 = 13, que no se puede dividir entre 2, por lo que el tamaño se redondea hasta 14). Por el contrario, si el tamaño de fuente actual es 14 y *wParam* es -3, el tamaño de fuente resultante sería 10 (14 - 3 = 11, que no es divisible por 2, por lo que el tamaño se redondea a 10).

El cambio se aplica a cada parte de la selección. Por lo tanto, si parte del texto es de 10 y algunos 20pt, después de una llamada con *wParam* establecido en 1, los tamaños de fuente se convierten en 11 y 22pt, respectivamente.

En la tabla siguiente se muestran ejemplos adicionales.



| Tamaño de fuente original | *wParam* | Tamaño de fuente resultante |
|--------------------|----------|---------------------|
| 7                  | 1        | 8                   |
| 7                  | 3        | 10                  |
| 10                 | 3        | 14                  |
| 14                 | -3       | 10                  |
| 28                 | 1        | 36                  |
| 28                 | 3        | 36                  |
| 80                 | 1        | 90                  |
| 80                 | -1       | 72                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ GETCHARFORMAT**](em-getcharformat.md)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de los controles Rich Edit](about-rich-edit-controls.md)
</dt> </dl>

 

 





