---
title: LB_INSERTSTRING mensaje (Winuser.h)
description: Inserta datos de cadena o elemento en un cuadro de lista. A diferencia del mensaje LB ADDSTRING, el mensaje LB INSERTSTRING no hace que se ordene una lista con el estilo \_ \_ SORT de \_ LB.
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- LB_INSERTSTRING controles de Windows mensaje
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
ms.openlocfilehash: dd47d08ef78c590ecb3b5900143b29bc49676b86d8facdcc91b05bb34c8f4aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085395"
---
# <a name="lb_insertstring-message"></a>Mensaje \_ INSERTSTRING de LB

Inserta datos de cadena o elemento en un cuadro de lista. A diferencia [**del \_ mensaje LB ADDSTRING,**](lb-addstring.md) el mensaje **LB \_ INSERTSTRING** no hace que se ordene una lista con el estilo [**SORT \_ de LB.**](list-box-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la posición en la que se va a insertar la cadena. Si este parámetro es -1, la cadena se agrega al final de la lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en NULL que se va a insertar. Si el cuadro de lista tiene un estilo dibujado por el propietario, pero no el estilo [**\_ HASSTRINGS**](list-box-styles.md) de LBS, este parámetro se almacena como datos de elemento en lugar de como una cadena. Puede enviar los mensajes [**\_ LB GETITEMDATA**](lb-getitemdata.md) [**y LB \_ SETITEMDATA**](lb-setitemdata.md) para recuperar o modificar los datos del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de la posición en la que se insertó la cadena. Si se produce un error, el valor devuelto es LB \_ ERR. Si no hay suficiente espacio para almacenar la nueva cadena, el valor devuelto es LB \_ ERRSPACE.

## <a name="remarks"></a>Comentarios

El [**mensaje \_ LB INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100). Reserva la cantidad de memoria especificada para que los mensajes **\_ LB INSERTSTRING** subsiguientes tarden el menor tiempo posible. Puede usar estimaciones para los *parámetros wParam* *y lParam.* Si sobreestima, se asigna la memoria adicional; Si se infravalora, la asignación normal se usa para los elementos que superan la cantidad solicitada.

Si el cuadro de lista tiene el estilo [**\_ WS HSCROLL**](/windows/desktop/winmsg/window-styles) e inserta una cadena más ancha que el cuadro de lista, envíe un mensaje [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparece la barra de desplazamiento horizontal.

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ SELECTSTRING**](lb-selectstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> </dl>

 

