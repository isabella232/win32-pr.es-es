---
title: WM_ENTERMENULOOP mensaje (Winuser.h)
description: Notifica al procedimiento de ventana principal de una aplicación que se ha especificado un bucle modal de menú.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5851109e44100d558603fb268a4668c1f138fff97e5e87db50a28445e70adb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939615"
---
# <a name="wm_entermenuloop-message"></a>Mensaje \_ ENTERMENULOOP de WM

Notifica al procedimiento de ventana principal de una aplicación que se ha especificado un bucle modal de menú.


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si el menú de la ventana se especificó mediante [**la función TrackPopupMenu.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) Este parámetro tiene un valor de **TRUE si** el menú de la ventana se escribió mediante **TrackPopupMenu** y **FALSE** si no lo era.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ EXITMENULOOP**](wm-exitmenuloop.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

