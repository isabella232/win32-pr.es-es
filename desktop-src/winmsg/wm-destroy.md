---
description: Se envía cuando se destruye una ventana. Se envía al procedimiento de ventana de la ventana que se va a destruir después de quitar la ventana de la pantalla.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: WM_DESTROY mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7acff03f01e9bf0c8021f8324411f646341a29a5b3b6dc1f9b3493ec89010c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587455"
---
# <a name="wm_destroy-message"></a>Mensaje \_ WM DESTROY

Se envía cuando se destruye una ventana. Se envía al procedimiento de ventana de la ventana que se va a destruir después de quitar la ventana de la pantalla.

Este mensaje se envía primero a la ventana que se está destruyendo y, después, a las ventanas secundarias (si existen) a medida que se destruyen. Durante el procesamiento del mensaje, se puede suponer que todas las ventanas secundarias siguen existiendo.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

## <a name="remarks"></a>Comentarios

Si la ventana que se destruye forma parte de la cadena del visor del Portapapeles (establecida mediante una llamada a la función [**SetClipboardViewer),**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) la ventana debe quitarse de la cadena procesando la función [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) antes de volver del **mensaje WM \_ DESTROY.**

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

[**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**WM \_ CLOSE**](wm-close.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
