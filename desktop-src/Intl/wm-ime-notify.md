---
description: Se envía a una aplicación para notificar los cambios en la ventana del IME. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 20e064b8-2baf-4b4c-8341-36c3e4643eff
title: Mensaje de WM_IME_NOTIFY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca5ab1b2a1fd62d159ab4f216bf9b1bb6892ed69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686819"
---
# <a name="wm_ime_notify-message"></a>Mensaje WM_IME_NOTIFY

Se envía a una aplicación para notificar los cambios en la ventana del IME. Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_NOTIFY,   
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

El comando. Este parámetro puede tener uno de los valores siguientes.

<dl>
<dd><a href="imn-changecandidate.md">IMN_CHANGECANDIDATE</a></dd> 
<dd><a href="imn-closecandidate.md">IMN_CLOSECANDIDATE</a></dd> 
<dd><a href="imn-closestatuswindow.md">IMN_CLOSESTATUSWINDOW</a></dd> 
<dd><a href="imn-guideline.md">IMN_GUIDELINE</a></dd> 
<dd><a href="imn-opencandidate.md">IMN_OPENCANDIDATE</a></dd> 
<dd><a href="imn-openstatuswindow.md">IMN_OPENSTATUSWINDOW</a></dd> 
<dd><a href="imn-setcandidatepos.md">IMN_SETCANDIDATEPOS</a></dd> 
<dd><a href="imn-setcompositionfont.md">IMN_SETCOMPOSITIONFONT</a></dd> 
<dd><a href="imn-setcompositionwindow.md">IMN_SETCOMPOSITIONWINDOW</a></dd> 
<dd><a href="imn-setconversionmode.md">IMN_SETCONVERSIONMODE</a></dd> 
<dd><a href="imn-setopenstatus.md">IMN_SETOPENSTATUS</a></dd> 
<dd><a href="imn-setsentencemode.md">IMN_SETSENTENCEMODE</a></dd> 
<dd><a href="imn-setstatuswindowpos.md">IMN_SETSTATUSWINDOWPOS</a></dd> 
</dl> 
</dd> 
<dt>

*lParam* 
</dt> <dd>

Datos específicos del comando, con el formato que depende del valor del parámetro *wParam* . Para obtener más información, consulte la documentación de cada comando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto depende del comando enviado.

## <a name="remarks"></a>Observaciones

Una aplicación procesa este mensaje si es responsable de administrar la ventana del IME.

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

[IMN_CHANGECANDIDATE](imn-changecandidate.md)
</dt> <dt>

[IMN_CLOSECANDIDATE](imn-closecandidate.md)
</dt> <dt>

[IMN_CLOSESTATUSWINDOW](imn-closestatuswindow.md)
</dt> <dt>

[IMN_GUIDELINE](imn-guideline.md)
</dt> <dt>

[IMN_OPENCANDIDATE](imn-opencandidate.md)
</dt> <dt>

[IMN_OPENSTATUSWINDOW](imn-openstatuswindow.md)
</dt> <dt>

[IMN_SETCANDIDATEPOS](imn-setcandidatepos.md)
</dt> <dt>

[IMN_SETCOMPOSITIONFONT](imn-setcompositionfont.md)
</dt> <dt>

[IMN_SETCOMPOSITIONWINDOW](imn-setcompositionwindow.md)
</dt> <dt>

[IMN_SETCONVERSIONMODE](imn-setconversionmode.md)
</dt> <dt>

[IMN_SETOPENSTATUS](imn-setopenstatus.md)
</dt> <dt>

[IMN_SETSENTENCEMODE](imn-setsentencemode.md)
</dt> <dt>

[IMN_SETSTATUSWINDOWPOS](imn-setstatuswindowpos.md)
</dt> </dl>

 

 
