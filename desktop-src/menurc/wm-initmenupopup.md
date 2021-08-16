---
title: WM_INITMENUPOPUP mensaje (Winuser.h)
description: 'WM_INITMENUPOPUP mensaje: se envía cuando un menú desplegable o submenú está a punto de activarse. Esto permite a una aplicación modificar el menú antes de que se muestre, sin cambiar todo el menú.'
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
ms.openlocfilehash: 2ba23607dcb8da7fb282e380e87fe6a2cbb9a26a50850845a5877d036983665f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869604"
---
# <a name="wm_initmenupopup-message"></a>Mensaje \_ WM INITMENUPOPUP

Se envía cuando un menú desplegable o submenú está a punto de activarse. Esto permite a una aplicación modificar el menú antes de que se muestre, sin cambiar todo el menú.


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

La palabra de orden bajo especifica la posición relativa de base cero del elemento de menú que abre el menú desplegable o submenú.

La palabra de orden superior indica si el menú desplegable es el menú de la ventana. Si el menú es el menú de la ventana, este parámetro es **TRUE**; de lo contrario, es **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM \_ INITMENU**](wm-initmenu.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

