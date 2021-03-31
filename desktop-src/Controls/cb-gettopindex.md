---
title: Mensaje de CB_GETTOPINDEX (Winuser. h)
description: Una aplicación envía el \_ mensaje CB GETTOPINDEX para recuperar el índice de base cero del primer elemento visible en la parte de cuadro de lista de un cuadro combinado.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- CB_GETTOPINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996376"
---
# <a name="cb_gettopindex-message"></a>\_Mensaje GETTOPINDEX CB

Una aplicación envía el mensaje **CB \_ GETTOPINDEX** para recuperar el índice de base cero del primer elemento visible en la parte de cuadro de lista de un cuadro combinado. Inicialmente, el elemento con el índice 0 está en la parte superior del cuadro de lista, pero si se ha desplazado el contenido del cuadro de lista, es posible que haya otro elemento en la parte superior.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el índice del primer elemento visible en el cuadro de lista del cuadro combinado.

Si se produce un error en el mensaje, el valor devuelto es CB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CB \_ SETTOPINDEX**](cb-settopindex.md)
</dt> </dl>

 

 





