---
description: Se envía a una ventana minimizada (icono).
ms.assetid: e4f0e638-f606-4745-888b-14a846c7fd37
title: WM_QUERYDRAGICON mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20aac405a247f89a31c49f60a4e421fa171465d399dcb61a436936de5c646362
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055995"
---
# <a name="wm_querydragicon-message"></a>Mensaje \_ DE WM QUERYDRADURN

Se envía a una ventana minimizada (icono). El usuario está a punto de arrastrar la ventana, pero no tiene un icono definido para su clase. Una aplicación puede devolver un identificador a un icono o cursor. El sistema muestra este cursor o icono mientras el usuario arrastra el icono.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Una aplicación debe devolver un identificador a un cursor o icono que el sistema va a mostrar mientras el usuario arrastra el icono. El cursor o el icono deben ser compatibles con la resolución del controlador de pantalla. Si la aplicación devuelve **NULL,** el sistema muestra el cursor predeterminado.

## <a name="remarks"></a>Comentarios

Cuando el usuario arrastra el icono de una ventana sin un icono de clase, el sistema reemplaza el icono por un cursor predeterminado. Si la aplicación requiere que se muestre otro cursor durante el arrastre, debe devolver un identificador al cursor o icono compatible con la resolución del controlador de pantalla. Si una aplicación devuelve un identificador a un cursor o icono de color, el sistema convierte el cursor o el icono en blanco y negro. La aplicación puede llamar a la [**función LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora) o [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) para cargar un cursor o icono desde los recursos de su archivo ejecutable (.exe) y recuperar este identificador.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en **un valor BOOL** y devolver el valor directamente. Se omite el valor **\_ MSGRESULT** de DWL establecido por la función [**SetWindowLong.**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)

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

[**LoadCursor**](/windows/win32/api/winuser/nf-winuser-loadcursora)
</dt> <dt>

[**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
