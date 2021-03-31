---
title: Mensaje de LB_INSERTSTRING (Winuser. h)
description: Inserta una cadena o datos de elemento en un cuadro de lista. A diferencia del mensaje de LB \_ en lb, el \_ mensaje lb INSERTSTRING no hace que se ordene una lista con el \_ estilo de ordenación lbs.
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- LB_INSERTSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858af0e0229f90a5ed9928e7478d0ac9a71c8f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150907"
---
# <a name="lb_insertstring-message"></a>\_Mensaje lb INSERTSTRING

Inserta una cadena o datos de elemento en un cuadro de lista. A diferencia del mensaje de [**lb en lb \_**](lb-addstring.md) , el mensaje **lb \_ INSERTSTRING** no hace que se ordene una lista con el estilo de [**\_ ordenación lbs**](list-box-styles.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la posición en la que se va a insertar la cadena. Si este parámetro es-1, la cadena se agrega al final de la lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en null que se va a insertar. Si el cuadro de lista tiene un estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , este parámetro se almacena como datos de elemento en lugar de una cadena. Puede enviar los mensajes [**lb \_ GETITEMDATA**](lb-getitemdata.md) y [**lb \_ SETITEMDATA**](lb-setitemdata.md) para recuperar o modificar los datos del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de la posición en la que se insertó la cadena. Si se produce un error, el valor devuelto es LB \_ Err. Si no hay suficiente espacio para almacenar la nueva cadena, el valor devuelto es LB \_ ERRSPACE.

## <a name="remarks"></a>Observaciones

El mensaje [**lb \_ INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada para que los mensajes de **lb \_ INSERTSTRING** posteriores tarden el menor tiempo posible. Puede usar estimaciones para los parámetros *wParam* e *lParam* . Si sobrestima, se asigna la memoria adicional; Si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.

Si el cuadro de lista tiene el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e inserta una cadena más ancha que el cuadro de lista, envíe un mensaje [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparezca la barra de desplazamiento horizontal.

En el caso de una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante CP \_ ACP. Esto puede causar problemas. Por ejemplo, los caracteres romanos acentuados en un cuadro de lista no Unicode en las ventanas japonesas se desactivarán. Para solucionar este error, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ SELECTSTRING**](lb-selectstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> </dl>

 

