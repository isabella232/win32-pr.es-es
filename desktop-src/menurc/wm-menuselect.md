---
title: WM_MENUSELECT mensaje (Winuser.h)
description: Se envía a la ventana de propietario de un menú cuando el usuario selecciona un elemento de menú.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1708aabf8ea12bf20c919f1306672358c2966a3d23aa0badccb1f4592c543f3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952225"
---
# <a name="wm_menuselect-message"></a>Mensaje \_ WM MENUSELECT

Se envía a la ventana de propietario de un menú cuando el usuario selecciona un elemento de menú.


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden bajo especifica el elemento de menú o el índice de submenú. Si el elemento seleccionado es un elemento de comando, este parámetro contiene el identificador del elemento de menú. Si el elemento seleccionado abre un menú desplegable o submenú, este parámetro contiene el índice del menú desplegable o submenú en el menú principal, y el parámetro *lParam* contiene el identificador del menú principal (en el que se hace clic); use la [**función GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) para obtener el identificador de menú al menú desplegable o submenú.

La palabra de orden superior especifica una o varias marcas de menú. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                             | Significado                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <dt>**MF \_ BITMAP**</dt> <dt>0x00000004L</dt> </dl>                | El elemento muestra un mapa de bits.<br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <dt>**MF \_ CHECKED**</dt> <dt>0x00000008L</dt> </dl>             | El elemento está activado.<br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <dt>**MF \_ DISABLED**</dt> <dt>0x00000002L</dt> </dl>          | El elemento está deshabilitado.<br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <dt>**MF \_ GRAYED**</dt> <dt>0x00000001L</dt> </dl>                | El elemento está atenuado.<br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <dt>**MF \_ HILITE**</dt> <dt>0x00000080L</dt> </dl>                | El elemento está resaltado.<br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <dt>**MF \_ MOUSESELECT**</dt> <dt>0x00008000L</dt> </dl> | El elemento se selecciona con el mouse.<br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <dt>**MF \_ OWNERDRAW**</dt> <dt>0x00000100L</dt> </dl>       | Item es un elemento dibujado por el propietario.<br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x00000010L</dt> </dl>                   | Elemento abre un menú desplegable o submenú.<br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl>             | El elemento se encuentra en el menú de la ventana. El *parámetro lParam* contiene un identificador para el menú asociado al mensaje.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del menú en el que se hizo clic.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Si la palabra de orden superior *de wParam* contiene 0xFFFF y el parámetro *lParam* contiene **NULL,** el sistema ha cerrado el menú.

No use el valor 1 para la palabra de orden superior de *wParam*, porque este valor se especifica como (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*). Si el valor 0xFFFF, se interpretaría como 0x0000FFFF, no 1, debido a la conversión a **un UINT**.

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

[**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Conceptual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

