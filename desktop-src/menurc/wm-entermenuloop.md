---
title: Mensaje de WM_ENTERMENULOOP (Winuser. h)
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
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714553"
---
# <a name="wm_entermenuloop-message"></a>Mensaje de ENTERMENULOOP de WM \_

Notifica al procedimiento de ventana principal de una aplicación que se ha especificado un bucle modal de menú.


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si el menú ventana se ha especificado mediante la función [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) . Este parámetro tiene un valor **true** si el menú ventana se escribió con **TrackPopupMenu** y **false** en caso contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EXITMENULOOP de WM \_**](wm-exitmenuloop.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

