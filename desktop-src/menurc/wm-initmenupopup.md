---
title: Mensaje de WM_INITMENUPOPUP (Winuser. h)
description: Se envía cuando un menú desplegable o un submenú está a punto de activarse. Esto permite que una aplicación modifique el menú antes de que se muestre, sin cambiar todo el menú.
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02bf0f9b8e196c27990cc1bc839daed4c92f8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079088"
---
# <a name="wm_initmenupopup-message"></a>Mensaje de INITMENUPOPUP de WM \_

Se envía cuando un menú desplegable o un submenú está a punto de activarse. Esto permite que una aplicación modifique el menú antes de que se muestre, sin cambiar todo el menú.


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del menú desplegable o submenú.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica la posición relativa de base cero del elemento de menú que abre el menú desplegable o submenú.

La palabra de orden superior indica si el menú desplegable es el menú ventana. Si el menú es el menú ventana, este parámetro es **true**; de lo contrario, es **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**INITMENU de WM \_**](wm-initmenu.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

