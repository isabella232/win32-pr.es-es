---
title: Mensaje de CB_SETTOPINDEX (Winuser. h)
description: Una aplicación envía el \_ mensaje CB SETTOPINDEX para asegurarse de que un elemento determinado esté visible en el cuadro de lista de un cuadro combinado.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- CB_SETTOPINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801238"
---
# <a name="cb_settopindex-message"></a>\_Mensaje SETTOPINDEX CB

Una aplicación envía el mensaje **CB \_ SETTOPINDEX** para asegurarse de que un elemento determinado esté visible en el cuadro de lista de un cuadro combinado. El sistema desplaza el contenido del cuadro de lista para que el elemento especificado aparezca en la parte superior del cuadro de lista o hasta que se alcance el intervalo de desplazamiento máximo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el índice de base cero del elemento de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es cero.

Si se produce un error en el mensaje, el valor devuelto es CB \_ Err.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CB \_ GETTOPINDEX**](cb-gettopindex.md)
</dt> </dl>

 

 





