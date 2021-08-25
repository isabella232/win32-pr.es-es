---
description: Se envía a una aplicación cuando se activa una ventana. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: WM_IME_SETCONTEXT mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fb3e65b47b5d62b1d37ffaee4dfc5927d76485d0c3e5de02662da64215e43f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829255"
---
# <a name="wm_ime_setcontext-message"></a>Mensaje \_ SETCONTEXT de WM IME \_

Se envía a una aplicación cuando se activa una ventana. Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,  
  WM_IME_SETCONTEXT,  
  WPARAM wParam,      
  LPARAM lParam      
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*wParam* 
</dt> <dd>

**TRUE** si la ventana está activa y FALSE en **caso** contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Opciones de visualización. Este parámetro puede tener uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                   | Significado                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <dt>**ISC \_ SHOWUICOMPOSITIONWINDOW**</dt> </dl> | Mostrar la ventana de composición por ventana de interfaz de usuario.<br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <dt>**ISC \_ SHOWUIGUIDWINDOW**</dt> </dl>                      | Mostrar la ventana de guía por ventana de interfaz de usuario.<br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <dt>**ISC \_ SHOWUISOFTKBD**</dt> </dl>                               | Mostrar el teclado suave mediante la ventana de la interfaz de usuario.<br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <dt>**ISC \_ SHOWUICANDIDATEWINDOW**</dt> </dl>       | Mostrar la ventana candidata del índice 0 por ventana de interfaz de usuario.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 1</dt> </dl>                                                                                        | Mostrar la ventana candidata del índice 1 por ventana de interfaz de usuario.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 2</dt> </dl>                                                                                        | Mostrar la ventana candidata del índice 2 por ventana de interfaz de usuario.<br/> |
| <dl> <dt>ISC \_ SHOWUICANDIDATEWINDOW << 3</dt> </dl>                                                                                        | Mostrar la ventana candidata del índice 3 por ventana de interfaz de usuario.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor devuelto por [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).

## <a name="remarks"></a>Comentarios

Si la aplicación ha creado una ventana IME, debe llamar a [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). De lo contrario, debería pasar este mensaje [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Si la aplicación dibuja la ventana de composición, la ventana IME predeterminada no tiene que mostrar su ventana de composición. En este caso, la aplicación debe borrar el valor **\_ SHOWUICOMPOSITIONWINDOW** de ISC del parámetro *lParam* antes de pasar el mensaje [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). Para mostrar una determinada ventana de interfaz de usuario, una aplicación debe quitar el valor correspondiente para que el IME no lo muestre.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                                                      |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h);</dt> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensajes del Administrador de métodos de entrada](input-method-manager-messages.md)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
