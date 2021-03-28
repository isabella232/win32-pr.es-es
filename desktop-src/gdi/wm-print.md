---
description: El mensaje de impresión de WM \_ se envía a una ventana para solicitar que se dibuje en el contexto de dispositivo especificado, normalmente en un contexto de dispositivo de impresora.
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: Mensaje de WM_PRINT (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a012d26e4357a639a7eb8d7930937a06a991124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082507"
---
# <a name="wm_print-message"></a>Mensaje de impresión de WM \_

El mensaje de **\_ impresión de WM** se envía a una ventana para solicitar que se dibuje en el contexto de dispositivo especificado, normalmente en un contexto de dispositivo de impresora.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

Identificador del contexto de dispositivo en el que se va a dibujar.

</dd> <dt>

*lParam* 
</dt> <dd>

Opciones de dibujo. Este parámetro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                  | Significado                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**\_CHECKVISIBLE PRF**</dt> </dl> | Dibuja la ventana solo si está visible.<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**\_elementos secundarios PRF**</dt> </dl>             | Dibuja todas las ventanas secundarias visibles.<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**\_cliente PRF**</dt> </dl>                   | Dibuja el área cliente de la ventana.<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**\_ERASEBKGND PRF**</dt> </dl>       | Borra el fondo antes de dibujar la ventana.<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**no \_ cliente PRF**</dt> </dl>          | Dibuja el área no cliente de la ventana.<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**propiedad de PRF \_**</dt> </dl>                      | Dibuja todas las ventanas de propiedad.<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) procesa este mensaje en función de la opción de dibujo especificada: si se \_ especifica PRF CHECKVISIBLE y la ventana no está visible, no hace nada, si \_ se especifica PRF nonclient, dibuje el área no cliente en el contexto de dispositivo especificado, si \_ se especifica PRF ERASEBKGND, envíe la ventana a un mensaje de [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) , si \_ se especifica el cliente PRF, envíe la ventana a un mensaje de [**WM \_ PRINTCLIENT**](wm-printclient.md) , si se establece un elemento secundario PRF, \_ envíe a cada ventana secundaria visible un **\_** \_ **\_** mensaje de impresión de WM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre pintura y dibujo](painting-and-drawing.md)
</dt> <dt>

[Pintar y dibujar mensajes](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ERASEBKGND de WM \_**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**PRINTCLIENT de WM \_**](wm-printclient.md)
</dt> </dl>

 

 
