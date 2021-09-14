---
description: Se envía inmediatamente antes de que el IME genere la cadena de composición como resultado de una pulsación de tecla. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 2740d009-8685-4f70-9b01-67b71f4ddcbd
title: WM_IME_STARTCOMPOSITION mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bd9a93b4c6c2e8dba6658c84b5f431dd9a54e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254798"
---
# <a name="wm_ime_startcomposition-message"></a>Mensaje \_ \_ STARTCOMPOSITION de WM IME

Se envía inmediatamente antes de que el IME genere la cadena de composición como resultado de una pulsación de tecla. Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,                
  WM_IME_STARTCOMPOSITION,  
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

Este mensaje es una notificación a una ventana de IME para abrir su ventana de composición. Una aplicación debe procesar este mensaje si muestra los propios caracteres de composición.

Si una aplicación ha creado una ventana IME, debe pasar este mensaje a esa ventana. La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) procesa el mensaje al pasarlo a la ventana de IME predeterminada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensajes del Administrador de métodos de entrada](input-method-manager-messages.md)
</dt> </dl>

 

 
