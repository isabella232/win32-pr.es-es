---
description: Se envía a una aplicación cuando se activa una ventana. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: ba1e7877-1612-4f2f-aced-0dd982352ad6
title: Mensaje de WM_IME_SETCONTEXT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b36cb1e80127d1a451dabcc457dc364a27878ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275441"
---
# <a name="wm_ime_setcontext-message"></a>\_Mensaje SETCONTEXT de IME de WM \_

Se envía a una aplicación cuando se activa una ventana. Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

*identificador* 
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*wParam* 
</dt> <dd>

**True** si la ventana está activa y **false** en caso contrario.

</dd> <dt>

*lParam* 
</dt> <dd>

Opciones de visualización. Este parámetro puede tener uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                   | Significado                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="ISC_SHOWUICOMPOSITIONWINDOW"></span><span id="isc_showuicompositionwindow"></span><dl> <dt>**SHOWUICOMPOSITIONWINDOW de ISC \_**</dt> </dl> | Mostrar la ventana de composición por la ventana de la interfaz de usuario.<br/>          |
| <span id="ISC_SHOWUIGUIDWINDOW"></span><span id="isc_showuiguidwindow"></span><dl> <dt>**SHOWUIGUIDWINDOW de ISC \_**</dt> </dl>                      | Mostrar la ventana guía por la ventana de la interfaz de usuario.<br/>                |
| <span id="ISC_SHOWUISOFTKBD"></span><span id="isc_showuisoftkbd"></span><dl> <dt>**SHOWUISOFTKBD de ISC \_**</dt> </dl>                               | Mostrar la ventana de la interfaz de usuario de teclado en pantalla.<br/>               |
| <span id="ISC_SHOWUICANDIDATEWINDOW"></span><span id="isc_showuicandidatewindow"></span><dl> <dt>**SHOWUICANDIDATEWINDOW de ISC \_**</dt> </dl>       | Mostrar la ventana de candidatos de índice 0 por ventana de interfaz de usuario.<br/> |
| <dl> <dt>SHOWUICANDIDATEWINDOW de ISC \_ << 1</dt> </dl>                                                                                        | Mostrar la ventana de candidatos de índice 1 por ventana de interfaz de usuario.<br/> |
| <dl> <dt>SHOWUICANDIDATEWINDOW de ISC \_ << 2</dt> </dl>                                                                                        | Mostrar la ventana candidatos de índice 2 por ventana de la interfaz de usuario.<br/> |
| <dl> <dt>SHOWUICANDIDATEWINDOW de ISC \_ << 3</dt> </dl>                                                                                        | Mostrar la ventana candidato de la ventana índice 3 por interfaz de usuario.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor devuelto por [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea).

## <a name="remarks"></a>Observaciones

Si la aplicación ha creado una ventana de IME, debe llamar a [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). De lo contrario, debe pasar este mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

Si la aplicación dibuja la ventana de composición, la ventana del IME predeterminada no tiene que mostrar su ventana de composición. En este caso, la aplicación debe borrar el valor de **\_ SHOWUICOMPOSITIONWINDOW de ISC** del parámetro *lParam* antes de pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) o [**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea). Para mostrar una determinada ventana de la interfaz de usuario, una aplicación debe quitar el valor correspondiente para que el IME no la muestre.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                                                      |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (include Windows. h); </dt> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Administrador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensajes del administrador de métodos de entrada](input-method-manager-messages.md)
</dt> <dt>

[**ImmIsUIMessage**](/windows/desktop/api/Imm/nf-imm-immisuimessagea)
</dt> </dl>

 

 
