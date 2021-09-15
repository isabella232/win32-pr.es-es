---
description: Una aplicación envía el mensaje WM MDICREATE a una ventana cliente de interfaz de múltiples documentos \_ (MDI) para crear una ventana secundaria MDI.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: WM_MDICREATE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571301"
---
# <a name="wm_mdicreate-message"></a>Mensaje \_ MDICREATE de WM

Una aplicación envía el **mensaje \_ WM MDICREATE** a una ventana cliente de interfaz de múltiples documentos (MDI) para crear una ventana secundaria MDI.


```C++
#define WM_MDICREATE                    0x0220
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) que contiene información que el sistema usa para crear la ventana secundaria MDI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HWND**

Si el mensaje se realiza correctamente, el valor devuelto es el identificador de la nueva ventana secundaria.

Si se produce un error en el mensaje, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

La ventana secundaria MDI se crea con los [**bits**](window-styles.md) de estilo de ventana **WS \_ CHILD**, **WS \_ CLIPSIBLINGS**, **WS \_ CLIPCHILDREN**, **WS \_ SYSMENU**, **WS \_ CAPTION**, **WS \_ THICKFRAME,** **WS \_ MINIMIZEBOX** y **WS \_ MAXIMIZEBOX,** además de bits de estilo adicionales especificados en la [**estructura MDICREATESTRUCT.**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) El sistema agrega el título de la nueva ventana secundaria al menú de ventana de la ventana de marco. Una aplicación debe usar este mensaje para crear todas las ventanas secundarias de la ventana de cliente.

Si una ventana cliente MDI recibe algún mensaje que cambia la activación de sus ventanas secundarias mientras se maximiza la ventana secundaria activa, el sistema restaura la ventana secundaria activa y maximiza la ventana secundaria recién activada.

Cuando se crea una ventana secundaria de MDI, el sistema envía el [**mensaje WM \_ CREATE**](wm-create.md) a la ventana. El *parámetro lParam* del mensaje **WM \_ CREATE** contiene un puntero a una [**estructura CREATESTRUCT.**](/windows/win32/api/winuser/ns-winuser-createstructa) El *miembro lpCreateParams* de esta estructura contiene un puntero a la estructura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) pasada con el mensaje **\_ MDICREATE** de WM que creó la ventana secundaria MDI.

Una aplicación no debe enviar un segundo mensaje **\_ MDICREATE de WM** mientras se sigue procesando un mensaje **\_ MDICREATE** de WM. Por ejemplo, no debe enviar un mensaje **\_ MDICREATE** de WM mientras una ventana secundaria de MDI está procesando su **\_ mensaje MDICREATE de WM.**

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

[**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[**WM \_ CREATE**](wm-create.md)
</dt> <dt>

[**WM \_ MDIDESTROY**](wm-mdidestroy.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 
