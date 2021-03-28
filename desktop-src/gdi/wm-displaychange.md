---
description: El mensaje de DISPLAYCHANGE de WM \_ se envía a todas las ventanas cuando cambia la resolución de pantalla.
ms.assetid: 5a6111fd-648e-41a9-aaf8-e5d93f5d54cd
title: Mensaje de WM_DISPLAYCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 682612529fd40b22481612bb26a954bec45e3901
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276448"
---
# <a name="wm_displaychange-message"></a>Mensaje de DISPLAYCHANGE de WM \_

El mensaje de **\_ DISPLAYCHANGE de WM** se envía a todas las ventanas cuando cambia la resolución de pantalla.

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

Nueva profundidad de imagen de la pantalla, en bits por píxel.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica la resolución horizontal de la pantalla.

La palabra de orden superior especifica la resolución vertical de la pantalla.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este mensaje solo se envía a las ventanas de nivel superior. Para todas las demás ventanas que se publican.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

 
