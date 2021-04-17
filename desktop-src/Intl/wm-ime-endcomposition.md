---
description: Se envía a una aplicación cuando el IME finaliza la composición. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: Mensaje de WM_IME_ENDCOMPOSITION (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ca9d1560810b22ae0d36010d2371e75b83a81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360325"
---
# <a name="wm_ime_endcomposition-message"></a>\_Mensaje ENDCOMPOSITION de IME de WM \_

Se envía a una aplicación cuando el IME finaliza la composición. Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,      
  WM_IME_ENDCOMPOSITION,  
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

Una aplicación debe procesar este mensaje si muestra los propios caracteres de composición.

Si la aplicación ha creado una ventana de IME, debe pasar este mensaje a esa ventana. La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  procesa este mensaje pasándolo a la ventana IME predeterminada.

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
</dt> </dl>

 

 
