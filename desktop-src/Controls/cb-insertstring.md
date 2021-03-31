---
title: Mensaje de CB_INSERTSTRING (Winuser. h)
description: Inserta una cadena o datos de elemento en la lista de un cuadro combinado. A diferencia del \_ mensaje CB ADDSTRING, el \_ mensaje CB INSERTSTRING no genera una lista con el estilo de \_ ordenación CBS que se va a ordenar.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- CB_INSERTSTRING controles de mensajes de Windows
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
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490541"
---
# <a name="cb_insertstring-message"></a>\_Mensaje INSERTSTRING CB

Inserta una cadena o datos de elemento en la lista de un cuadro combinado. A diferencia del mensaje [**CB \_ ADDSTRING**](cb-addstring.md) , el mensaje **CB \_ INSERTSTRING** no genera una lista con el estilo de [**\_ ordenación CBS**](combo-box-styles.md) que se va a ordenar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la posición en la que se va a insertar la cadena. Si este parámetro es-1, la cadena se agrega al final de la lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la cadena terminada en null que se va a insertar. Si crea el cuadro combinado con un estilo dibujado por el propietario pero sin el estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , el valor del parámetro *lParam* se almacena en lugar de la cadena a la que apuntaría de otro modo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el índice de la posición en la que se insertó la cadena. Si se produce un error, el valor devuelto es CB \_ error. Si no hay suficiente espacio disponible para almacenar la nueva cadena, es CB \_ ERRSPACE.

Si el cuadro combinado tiene el estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e inserta una cadena más ancha que el cuadro combinado, debe enviar un mensaje [**lb \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) para asegurarse de que aparezca la barra de desplazamiento horizontal.

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**LB \_ SETHORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**\_directorio CB**](cb-dir.md)
</dt> </dl>

 

