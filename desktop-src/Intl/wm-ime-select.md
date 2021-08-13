---
description: Se envía a una aplicación cuando el sistema operativo está a punto de cambiar el IME actual. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: WM_IME_SELECT mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611ff30bac32fbd38c9aef00e459b49f9760d9702c619f7e6e7f55e6e3b10acb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644625"
---
# <a name="wm_ime_select-message"></a>Mensaje \_ SELECT de WM IME \_

Se envía a una aplicación cuando el sistema operativo está a punto de cambiar el IME actual. Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hwnd* 
</dt> <dd>

Identificador a ventana.

</dd> <dt>

*wParam* 
</dt> <dd>

Indicador de selección. Este parámetro especifica **TRUE si** se selecciona el IME indicado. El parámetro se establece en **FALSE** si el IME especificado ya no está seleccionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de configuración regional de entrada asociado al IME.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no tiene ningún valor devuelto.

## <a name="remarks"></a>Observaciones

Una aplicación que ha creado una ventana de IME debe pasar este mensaje a esa ventana para que pueda recuperar el identificador de diseño del teclado al IME recién seleccionado.

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  procesa este mensaje pasando la información a la ventana predeterminada de IME.

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

 

 
