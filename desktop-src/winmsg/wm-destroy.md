---
description: Se envía cuando se destruye una ventana. Se envía al procedimiento de ventana de la ventana que se va a destruir después de quitar la ventana de la pantalla.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: Mensaje de WM_DESTROY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db195c22c38759146fb76e98edf4ca7f605a1c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277766"
---
# <a name="wm_destroy-message"></a>Mensaje de destrucción de WM \_

Se envía cuando se destruye una ventana. Se envía al procedimiento de ventana de la ventana que se va a destruir después de quitar la ventana de la pantalla.

Este mensaje se envía primero a la ventana que se está destruyendo y, a continuación, a las ventanas secundarias (si existen) a medida que se destruyen. Durante el procesamiento del mensaje, se puede suponer que todas las ventanas secundarias todavía existen.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_DESTROY                      0x0002
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

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Si la ventana que se va a destruir forma parte de la cadena del visor del portapapeles (establecida mediante una llamada a la función [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) ), la ventana debe quitarse de la cadena procesando la función [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) antes de volver del mensaje de **\_ destrucción de WM** .

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

[**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**cierre de WM \_**](wm-close.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
