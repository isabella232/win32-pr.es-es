---
title: LB_ADDSTRING mensaje (Winuser.h)
description: Agrega una cadena a un cuadro de lista. Si el cuadro de lista no tiene el estilo SORT de LBS, la cadena \_ se agrega al final de la lista. De lo contrario, la cadena se inserta en la lista y la lista se ordena.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- LB_ADDSTRING controles de Windows mensaje
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
ms.openlocfilehash: 552e3c344a730ad1fc00337cafa71a19a6586b9a4c95f2ed1ebce352d9d909aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671691"
---
# <a name="lb_addstring-message"></a>Mensaje \_ ADDSTRING de LB

Agrega una cadena a un cuadro de lista. Si el cuadro de lista no tiene el estilo [**\_ SORT de LBS,**](list-box-styles.md) la cadena se agrega al final de la lista. De lo contrario, la cadena se inserta en la lista y la lista se ordena.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en NULL que se va a agregar.

Si el cuadro de lista tiene un estilo dibujado por el propietario pero no el estilo [**\_ HASSTRINGS**](list-box-styles.md) de LBS, este parámetro se almacena como datos de elemento en lugar de como una cadena. Puede enviar los mensajes **\_ LB GETITEMDATA** y **LB \_ SETITEMDATA** para recuperar o modificar los datos del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de base cero de la cadena en el cuadro de lista. Si se produce un error, el valor devuelto es LB \_ ERR. Si no hay suficiente espacio para almacenar la nueva cadena, el valor devuelto es LB \_ ERRSPACE.

## <a name="remarks"></a>Observaciones

Si el cuadro de lista tiene un estilo dibujado por el propietario y el estilo SORT de [**\_ LBS,**](list-box-styles.md) pero no el estilo [**\_ HASSTRINGS**](list-box-styles.md) de LBS, el sistema envía el mensaje [**\_ COMPAREITEM**](wm-compareitem.md) de WM una o varias veces al propietario del cuadro de lista para colocar el nuevo elemento correctamente en el cuadro de lista.

El [**mensaje \_ LB INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada para que los mensajes **\_ LB ADDSTRING** subsiguientes tarden el menor tiempo posible. Puede usar estimaciones para los *parámetros wParam* *y lParam.* Si sobreestima, se asigna la memoria adicional; Si se infravalora, la asignación normal se usa para los elementos que superan la cantidad solicitada.

Si el cuadro de lista tiene el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) y agrega una cadena más ancha que el cuadro de lista, envíe un mensaje [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparece la barra de desplazamiento horizontal.

Para una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante CP \_ ACP. Esto puede causar problemas. Por ejemplo, los caracteres latinos acentuados en un cuadro de lista que no es Unicode en Windows japonés aparecerán desconsolados. Para solucionar este problema, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



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

 

