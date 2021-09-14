---
title: CB_GETTOPINDEX mensaje (Winuser.h)
description: Una aplicación envía el mensaje CB GETTOPINDEX para recuperar el índice de base cero del primer elemento visible en la parte del cuadro de \_ lista de un cuadro combinado.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- CB_GETTOPINDEX controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174185"
---
# <a name="cb_gettopindex-message"></a>Mensaje \_ GETTOPINDEX de CB

Una aplicación envía el mensaje **\_ CB GETTOPINDEX** para recuperar el índice de base cero del primer elemento visible en la parte del cuadro de lista de un cuadro combinado. Inicialmente, el elemento con índice 0 está en la parte superior del cuadro de lista, pero si el contenido del cuadro de lista se ha desplazando, es posible que otro elemento esté en la parte superior.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, el valor devuelto es el índice del primer elemento visible en el cuadro de lista del cuadro combinado.

Si se produce un error en el mensaje, el valor devuelto es CB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CB \_ SETTOPINDEX**](cb-settopindex.md)
</dt> </dl>

 

 





