---
description: Se envía a una aplicación cuando finaliza la composición del IME. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: d0f05524-4dfc-45b2-9476-6f1244190de5
title: WM_IME_ENDCOMPOSITION mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9e19bcf1834d4f9e721efb2a2be53ca20268c7be42109975a7dea52e75d214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560405"
---
# <a name="wm_ime_endcomposition-message"></a>Mensaje \_ \_ ENDCOMPOSITION de WM IME

Se envía a una aplicación cuando finaliza la composición del IME. Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

## <a name="remarks"></a>Comentarios

Una aplicación debe procesar este mensaje si muestra los propios caracteres de composición.

Si la aplicación ha creado una ventana de IME, debe pasar este mensaje a esa ventana. La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  procesa este mensaje al pasarlo a la ventana predeterminada de IME.

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

 

 
