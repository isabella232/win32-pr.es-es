---
description: Se envía a una aplicación cuando la ventana del IME no encuentra ningún espacio para extender el área de la ventana de composición. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: Mensaje de WM_IME_COMPOSITIONFULL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33051ac3e4e893eb803d4b13d7bfbf53751258b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279489"
---
# <a name="wm_ime_compositionfull-message"></a>\_Mensaje COMPOSITIONFULL de IME de WM \_

Se envía a una aplicación cuando la ventana del IME no encuentra ningún espacio para extender el área de la ventana de composición. Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,
  WM_IME_COMPOSITIONFULL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a>Parámetros

Este mensaje no tiene parámetros.

<dl></dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

La aplicación debe usar el comando [IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) para especificar cómo se debe mostrar la ventana.

La ventana del IME, en lugar del IME, envía este mensaje de notificación mediante la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensajes del administrador de métodos de entrada](input-method-manager-messages.md)
</dt> <dt>

[SETCOMPOSITIONWINDOW de IMC \_](imc-setcompositionwindow.md)
</dt> </dl>

 

 
