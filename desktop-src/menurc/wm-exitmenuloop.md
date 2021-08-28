---
title: WM_EXITMENULOOP mensaje (Winuser.h)
description: Notifica al procedimiento de ventana principal de una aplicación que se ha cerrado un bucle modal de menú.
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- WM_EXITMENULOOP menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec6d2cfb8457a748b7bb7bbdda481a0a1f73e5331891d45bd1bf1cabdfe0c5c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886385"
---
# <a name="wm_exitmenuloop-message"></a>Mensaje \_ EXITMENULOOP de WM

Notifica al procedimiento de ventana principal de una aplicación que se ha cerrado un bucle modal de menú.


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si el menú es un menú contextual. Este parámetro tiene un valor **de TRUE si** es un menú contextual, **FALSE** si no lo es.

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

[**WM \_ ENTERMENULOOP**](wm-entermenuloop.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

