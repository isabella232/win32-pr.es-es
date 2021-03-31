---
title: Mensaje de LB_ADDSTRING (Winuser. h)
description: Agrega una cadena a un cuadro de lista. Si el cuadro de lista no tiene el \_ estilo de ordenación lbs, la cadena se agrega al final de la lista. De lo contrario, la cadena se inserta en la lista y la lista está ordenada.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- LB_ADDSTRING controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87e1c820b7a4c122012076c82ce20adc0d01e2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079305"
---
# <a name="lb_addstring-message"></a>Mensaje de LB \_ ADDSTRING

Agrega una cadena a un cuadro de lista. Si el cuadro de lista no tiene el estilo de [**\_ ordenación lbs**](list-box-styles.md) , la cadena se agrega al final de la lista. De lo contrario, la cadena se inserta en la lista y la lista está ordenada.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en null que se va a agregar.

Si el cuadro de lista tiene un estilo dibujado por el propietario pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , este parámetro se almacena como datos de elemento en lugar de una cadena. Puede enviar los mensajes **lb \_ GETITEMDATA** y **lb \_ SETITEMDATA** para recuperar o modificar los datos del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero de la cadena en el cuadro de lista. Si se produce un error, el valor devuelto es LB \_ Err. Si no hay suficiente espacio para almacenar la nueva cadena, el valor devuelto es LB \_ ERRSPACE.

## <a name="remarks"></a>Observaciones

Si el cuadro de lista tiene un estilo dibujado por el propietario y el estilo de [**\_ ordenación lbs**](list-box-styles.md) , pero no el estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , el sistema envía el mensaje [**\_ COMPAREITEM de WM**](wm-compareitem.md) una o varias veces al propietario del cuadro de lista para colocar el nuevo elemento correctamente en el cuadro de lista.

El mensaje [**lb \_ INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada para que los mensajes de **lb \_ ADDSTRING** posteriores tarden el menor tiempo posible. Puede usar estimaciones para los parámetros *wParam* e *lParam* . Si sobrestima, se asigna la memoria adicional; Si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.

Si el cuadro de lista tiene el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) y agrega una cadena más ancha que el cuadro de lista, envíe un mensaje [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparezca la barra de desplazamiento horizontal.

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

[**LB \_ DELETESTRING**](lb-deletestring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**LB \_ SELECTSTRING**](lb-selectstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**COMPAREITEM de WM \_**](wm-compareitem.md)
</dt> </dl>

 

