---
title: Mensaje EM_SETFONTSIZE (RichEdit. h)
description: Establece el tamaño de fuente para el texto seleccionado en un control Rich Edit.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- EM_SETFONTSIZE controles de mensajes de Windows
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
ms.openlocfilehash: 8eb75276acbb86cbd452a8ad97698f1cd7382bd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490721"
---
# <a name="em_setfontsize-message"></a>\_Mensaje SETFONTSIZE em

Establece el tamaño de fuente para el texto seleccionado en un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Cambiar el tamaño en puntos del texto seleccionado. El resultado se redondeará según los valores que se muestran en la tabla siguiente. Este parámetro debe estar en el intervalo de-1637 a 1638. El tamaño de fuente resultante estará en el intervalo comprendido entre 1 y 1638.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si no se ha producido ningún error, el valor devuelto es **true**.

Si se produjo un error, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

Puede obtener fácilmente el tamaño de fuente enviando el mensaje [**\_ GETCHARFORMAT em**](em-getcharformat.md) .

La edición enriquecida primero agrega *wParam* al tamaño de fuente actual y, a continuación, usa el tamaño resultante y la tabla siguiente para determinar el valor de redondeo.



| Colores    | Valor de redondeo |
|---------|----------------|
| <= 12 | 1              |
| 28      | 2              |
| 36      | 0              |
| 48      | 0              |
| 72      | 0              |
| 80      | 0              |
| > 80 | 10             |



 

Si el tamaño de fuente resultante no es divisible de forma uniforme por el valor de redondeo, el tamaño de fuente se redondea a continuación a un número divisible por el valor de redondeo. Por tanto, si el tamaño de fuente es menor o igual que 12, el valor de redondeo será 1. Del mismo modo, si el tamaño de fuente es menor o igual que 28, el valor de redondeo es 2. En el caso de valores mayores que 28, los tamaños de fuente se redondean a la siguiente banda. Por lo tanto, el tamaño de fuente salta a 36, 48, 72, 80. Después 80, todo el redondeo se realiza en incrementos de diez puntos.

El tamaño de fuente se redondea o reduce verticalmente en función del signo de *wParam*. Si *wParam* es positivo, el redondeo siempre estará activo. De lo contrario, el redondeo siempre está inactivo. Por lo tanto, si el tamaño de fuente actual es 10 y *wParam* es 3, el tamaño de fuente resultante sería 14 (10 + 3 = 13, que no es divisible por 2, por lo que el tamaño se redondea hasta 14). Por el contrario, si el tamaño de fuente actual es 14 y *wParam* es-3, el tamaño de fuente resultante sería 10 (14-3 = 11, que no es divisible en 2, por lo que el tamaño se redondea a 10).

El cambio se aplica a cada parte de la selección. Por lo tanto, si parte del texto es 10 PTO y algún 20 PT, después de una llamada con *wParam* establecida en 1, los tamaños de fuente se convierten en 11pt y 22pt, respectivamente.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Edición enriquecida 3,0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_GETCHARFORMAT em**](em-getcharformat.md)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

**Vista**
</dt> <dt>

[Acerca de los controles Rich Edit](about-rich-edit-controls.md)
</dt> </dl>

 

 





