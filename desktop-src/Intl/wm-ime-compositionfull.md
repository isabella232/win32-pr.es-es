---
description: Se envía a una aplicación cuando la ventana de IME no encuentra espacio para ampliar el área de la ventana de composición. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: d81d6438-c470-4ae5-8016-8d816bcba9b8
title: WM_IME_COMPOSITIONFULL mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954a5f91283ca5c4944c274d422508ef0b91b55b8acc34f790cf446f93a598ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811495"
---
# <a name="wm_ime_compositionfull-message"></a>Mensaje \_ DE WM IME \_ COMPOSITIONFULL

Se envía a una aplicación cuando la ventana de IME no encuentra espacio para ampliar el área de la ventana de composición. Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

## <a name="remarks"></a>Comentarios

La aplicación debe usar el [comando \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md) de IMC para especificar cómo se debe mostrar la ventana.

La ventana IME, en lugar del IME, envía este mensaje de notificación por la [**función SendMessage.**](/windows/win32/api/winuser/nf-winuser-sendmessage)

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
</dt> <dt>

[IMC \_ SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md)
</dt> </dl>

 

 
