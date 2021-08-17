---
title: CB_SETTOPINDEX mensaje (Winuser.h)
description: Una aplicación envía el mensaje CB SETTOPINDEX para asegurarse de que un elemento determinado está visible en el \_ cuadro de lista de un cuadro combinado.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- CB_SETTOPINDEX controles de Windows mensaje
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
ms.openlocfilehash: d9364ef5013ef692adda76f96752f11691d5f4cc87c857386914105d16decb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832293"
---
# <a name="cb_settopindex-message"></a>Mensaje \_ SETTOPINDEX de CB

Una aplicación envía el **mensaje \_ CB SETTOPINDEX** para asegurarse de que un elemento determinado está visible en el cuadro de lista de un cuadro combinado. El sistema desplaza el contenido del cuadro de lista para que el elemento especificado aparezca en la parte superior del cuadro de lista o se haya alcanzado el intervalo de desplazamiento máximo.

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

Si el mensaje es correcto, el valor devuelto es cero.

Si se produce un error en el mensaje, el valor devuelto es CB \_ ERR.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CB \_ GETTOPINDEX**](cb-gettopindex.md)
</dt> </dl>

 

 





