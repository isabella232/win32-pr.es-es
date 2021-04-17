---
title: Mensaje de WM_MENUSELECT (Winuser. h)
description: Se envía a la ventana propietaria de un menú cuando el usuario selecciona un elemento de menú.
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
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714649"
---
# <a name="wm_menuselect-message"></a>Mensaje de MENUSELECT de WM \_

Se envía a la ventana propietaria de un menú cuando el usuario selecciona un elemento de menú.


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

La palabra de orden inferior especifica el elemento de menú o el índice de submenú. Si el elemento seleccionado es un elemento de comando, este parámetro contiene el identificador del elemento de menú. Si el elemento seleccionado abre un menú desplegable o un submenú, este parámetro contiene el índice del menú desplegable o submenú en el menú principal, y el parámetro *lParam* contiene el identificador del menú principal (en el que se hace clic); Utilice la función [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) para obtener el identificador de menú del menú desplegable o submenú.

La palabra de orden superior especifica una o más marcas de menú. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                             | Significado                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <dt>**MF \_ MAPA de bits**</dt> <dt>0x00000004L</dt> </dl>                | El elemento muestra un mapa de bits.<br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <dt>**MF \_**</dt> <dt>0x00000008L</dt> activado </dl>             | El elemento está activado.<br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <dt>**MF \_ Deshabilitado**</dt> <dt>0x00000002L</dt> </dl>          | El elemento está deshabilitado.<br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <dt>**MF \_ 0x00000001L ATENUAdo**</dt> <dt></dt> </dl>                | El elemento está atenuado.<br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <dt>**MF \_ HILITE**</dt> <dt>0x00000080L</dt> </dl>                | El elemento está resaltado.<br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <dt>**MF \_ MOUSESELECT**</dt> <dt>0x00008000L</dt> </dl> | El elemento se selecciona con el mouse.<br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <dt>**MF \_**</dt> <dt>0X00000100L</dt> de OWNERDRAW </dl>       | El elemento es un elemento dibujado por el propietario.<br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_**</dt> <dt>0x00000010L</dt> emergente </dl>                   | Elemento abre un menú desplegable o un submenú.<br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl>             | El elemento se encuentra en el menú ventana. El parámetro *lParam* contiene un identificador para el menú asociado al mensaje.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del menú en el que se hizo clic.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Si la palabra de orden superior de *wParam* contiene 0xFFFF y el parámetro *lParam* contiene **null**, el sistema ha cerrado el menú.

No use el valor 1 para la palabra de orden superior de *wParam*, ya que este valor se especifica como (**uint**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*). Si el valor es 0xFFFF, se interpretaría como 0x0000FFFF, no como 1, debido a la conversión a **uint**.

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

[**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Vista**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

