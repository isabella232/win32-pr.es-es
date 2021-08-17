---
description: El mensaje WM PRINT se envía a una ventana para solicitar que se dibuje en el contexto de dispositivo especificado, normalmente en un \_ contexto de dispositivo de impresora.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: WM_PRINT mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09d3cb7dbb3b4a4fca7a2af4272f1b4175aa26e911d1def909c97ba35f3d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964855"
---
# <a name="wm_print-message"></a>Mensaje \_ DE WM PRINT

El **mensaje \_ WM PRINT** se envía a una ventana para solicitar que se dibuje en el contexto de dispositivo especificado, normalmente en un contexto de dispositivo de impresora.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto del dispositivo en el que se dibujará.

</dd> <dt>

*lParam* 
</dt> <dd>

Opciones de dibujo. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                  | Significado                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**PRF \_ CHECKVISIBLE**</dt> </dl> | Dibuja la ventana solo si está visible.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**PRF \_ CHILDREN**</dt> </dl>             | Dibuja todas las ventanas secundarios visibles.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**CLIENTE \_ DE PRF**</dt> </dl>                   | Dibuja el área de cliente de la ventana.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**PRF \_ ERASEB PREPND**</dt> </dl>       | Borra el fondo antes de dibujar la ventana.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**PRF \_ NONCLIENT**</dt> </dl>          | Dibuja el área no cliente de la ventana.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**PROPIEDAD \_ DE PRF**</dt> </dl>                      | Dibuja todas las ventanas de propiedad.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) procesa este mensaje en función de la opción de dibujo especificada: si se especifica PRF CHECKVISIBLE y la ventana no está visible, No haga nada, si se especifica PRF NONCLIENT, dibuje el área no cliente en el contexto de dispositivo especificado; si se especifica PRF ERASEB PREPND, envíe a la ventana un mensaje \_ WM \_ \_ [**\_ ERASEB NONCLIENTND;**](../winmsg/wm-erasebkgnd.md) si se especifica PRF CLIENT, envíe a la ventana un mensaje \_ [**\_ PRINTCLIENT**](wm-printclient.md) de WM; si se establece PRF \_ CHILDREN, **\_** \_ **\_** envíe a cada ventana secundaria visible un mensaje WM PRINT; si se establece PRF OWNED, envíe a cada ventana de propiedad visible un mensaje PRINT de WM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre dibujo y dibujo](painting-and-drawing.md)
</dt> <dt>

[Pintar y dibujar mensajes](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ERASEBND**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ PRINTCLIENT**](wm-printclient.md)
</dt> </dl>

 

 
