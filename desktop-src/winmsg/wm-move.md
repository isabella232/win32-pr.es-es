---
description: Se envía una vez que se ha despasado una ventana.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: Mensaje de WM_MOVE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56004ec47266a50bf2ac82a828b9046c84a8ebfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677918"
---
# <a name="wm_move-message"></a>Mensaje de movimiento de WM \_

Se envía una vez que se ha despasado una ventana.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .


```C++
#define WM_MOVE                         0x0003
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Las coordenadas x e y de la esquina superior izquierda del área de cliente de la ventana. La palabra de orden inferior contiene la coordenada x mientras que la palabra de orden superior contiene la coordenada y.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Los parámetros se proporcionan en coordenadas de pantalla para las ventanas superpuestas y ventanas emergentes, y en las coordenadas de cliente primario para las ventanas secundarias.

En el ejemplo siguiente se muestra cómo obtener la posición del parámetro *lParam* .


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



También puede usar la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) para convertir el parámetro *lParam* en una estructura [**Points**](/previous-versions//dd162808(v=vs.85)) .

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía los mensajes de **\_ tamaño de WM** y **\_ movimiento de WM** cuando procesa el mensaje de [**\_ WINDOWPOSCHANGED de WM**](wm-windowposchanged.md) .
Los mensajes de **\_ tamaño de WM** y **\_ movimiento de WM** no se envían si una aplicación controla el mensaje de **\_ WINDOWPOSCHANGED de WM** sin llamar a **DefWindowProc**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WINDOWPOSCHANGED de WM \_**](wm-windowposchanged.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**CIMA**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

 
