---
title: CB_INSERTSTRING mensaje (Winuser.h)
description: Inserta datos de cadena o elemento en la lista de un cuadro combinado. A diferencia del mensaje CB ADDSTRING, el mensaje INSERTSTRING de CB no hace que se ordene una lista con el estilo \_ \_ \_ CBS SORT.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- CB_INSERTSTRING controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcebd3ed5c52a40f3ca5d49031948f76edfa9d6d98974cec104c4b8e283c101a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089075"
---
# <a name="cb_insertstring-message"></a>Mensaje \_ INSERTSTRING de CB

Inserta datos de cadena o elemento en la lista de un cuadro combinado. A diferencia [**del mensaje \_ CB ADDSTRING,**](cb-addstring.md) el mensaje **\_ INSERTSTRING de CB** no hace que se ordene una lista con el estilo [**\_ CBS SORT.**](combo-box-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la posición en la que se va a insertar la cadena. Si este parámetro es -1, la cadena se agrega al final de la lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en NULL que se va a insertar. Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**\_ HASSTRINGS de CBS,**](combo-box-styles.md) el valor del parámetro *lParam* se almacena en lugar de la cadena a la que apuntaría de otro modo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de la posición en la que se insertó la cadena. Si se produce un error, el valor devuelto es CB \_ ERR. Si no hay suficiente espacio disponible para almacenar la nueva cadena, es CB \_ ERRSPACE.

Si el cuadro combinado tiene el estilo [**\_ WS HSCROLL**](/windows/desktop/winmsg/window-styles) e inserta una cadena más ancha que el cuadro combinado, debe enviar un mensaje [**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparece la barra de desplazamiento horizontal.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**CB \_ DIR**](cb-dir.md)
</dt> </dl>

 

