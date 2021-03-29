---
description: Se envía a una ventana minimizada (icónica).
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: Mensaje de WM_QUERYDRAGICON (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c6040df06923e778eb717db4148bed233db4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360715"
---
# <a name="wm_querydragicon-message"></a>Mensaje de QUERYDRAGICON de WM \_

Se envía a una ventana minimizada (icónica). La ventana está a punto de ser arrastrada por el usuario, pero no tiene un icono definido para su clase. Una aplicación puede devolver un identificador a un icono o un cursor. El sistema muestra este cursor o icono mientras el usuario arrastra el icono.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_QUERYDRAGICON                0x0037
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver un identificador a un cursor o icono que el sistema va a mostrar mientras el usuario arrastra el icono. El cursor o el icono deben ser compatibles con la resolución del controlador de pantalla. Si la aplicación devuelve **null**, el sistema muestra el cursor predeterminado.

## <a name="remarks"></a>Observaciones

Cuando el usuario arrastra el icono de una ventana sin un icono de clase, el sistema reemplaza el icono por un cursor predeterminado. Si la aplicación requiere que se muestre un cursor diferente durante el arrastre, debe devolver un identificador para el cursor o el icono compatible con la resolución del controlador de pantalla. Si una aplicación devuelve un identificador a un cursor de color o un icono, el sistema convierte el cursor o el icono en blanco y negro. La aplicación puede llamar a la función [**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) o [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) para cargar un cursor o un icono de los recursos en su archivo ejecutable (. exe) y para recuperar este identificador.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en un **booleano** y devolver el valor directamente. Se omite el valor de **DWL \_ MSGRESULT** establecido por la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

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

[**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
