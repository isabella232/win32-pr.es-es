---
description: Una aplicación envía el mensaje de MDICREATE de WM \_ a una ventana de cliente de la interfaz de múltiples documentos (MDI) para crear una ventana secundaria MDI.
ms.assetid: f2313ffd-867f-4870-a667-3e5f5402776f
title: Mensaje de WM_MDICREATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fc11e9dfc561b138a95b711d68ecd831a43d2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716443"
---
# <a name="wm_mdicreate-message"></a>Mensaje de MDICREATE de WM \_

Una aplicación envía el mensaje de **\_ MDICREATE de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para crear una ventana secundaria MDI.


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

Puntero a una estructura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) que contiene información que el sistema usa para crear la ventana secundaria MDI.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **hWnd**

Si el mensaje se realiza correctamente, el valor devuelto es el identificador de la nueva ventana secundaria.

Si se produce un error en el mensaje, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

La ventana secundaria MDI se crea con el [**estilo de ventana**](window-styles.md) bits **WS \_ secundario**, **WS \_ CLIPSIBLINGS**, **WS \_ CLIPCHILDREN**, **WS \_ SYSMENU**, **WS \_ Caption**, **WS \_ THICKFRAME**, **WS \_ MINIMIZEBOX** y **WS \_ MAXIMIZEBOX**, además de los bits de estilo adicionales especificados en la estructura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) . El sistema agrega el título de la nueva ventana secundaria al menú ventana de la ventana marco. Una aplicación debe usar este mensaje para crear todas las ventanas secundarias de la ventana de cliente.

Si una ventana de cliente MDI recibe cualquier mensaje que cambie la activación de sus ventanas secundarias mientras la ventana secundaria activa está maximizada, el sistema restaura la ventana secundaria activa y maximiza la ventana secundaria que se acaba de activar.

Cuando se crea una ventana secundaria MDI, el sistema envía el mensaje de [**\_ creación de WM**](wm-create.md) a la ventana. El parámetro *lParam* del mensaje **de \_ creación de WM** contiene un puntero a una estructura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) . El miembro *lpCreateParams* de esta estructura contiene un puntero a la estructura [**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa) pasada con el mensaje de **\_ MDICREATE de WM** que creó la ventana secundaria MDI.

Una aplicación no debe enviar un segundo mensaje de **\_ MDICREATE de WM** mientras se sigue procesando un mensaje de **\_ MDICREATE de WM** . Por ejemplo, no debería enviar un mensaje de **WM \_ MDICREATE** mientras una ventana secundaria MDI esté procesando su mensaje de **WM \_ MDICREATE** .

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

[**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**MDICREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-mdicreatestructa)
</dt> <dt>

[**creación de WM \_**](wm-create.md)
</dt> <dt>

[**MDIDESTROY de WM \_**](wm-mdidestroy.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 
