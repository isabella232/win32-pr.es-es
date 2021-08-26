---
description: Se envía una vez que se ha movido una ventana.
ms.assetid: 552ddc26-fe63-449b-8c82-bb927a2c1c41
title: WM_MOVE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84c18d7a4f4411f45a3338a057a60942d01905ccefd25b40ee511d3b8a5d915d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810475"
---
# <a name="wm_move-message"></a>Mensaje \_ DE WM MOVE

Se envía una vez que se ha movido una ventana.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)


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

Coordenadas x e y de la esquina superior izquierda del área cliente de la ventana. La palabra de orden bajo contiene la coordenada X, mientras que la palabra de orden superior contiene la coordenada y.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Los parámetros se dan en coordenadas de pantalla para ventanas superpuestas y emergentes y en coordenadas de cliente primario para ventanas secundarias.

En el ejemplo siguiente se muestra cómo obtener la posición del *parámetro lParam.*


```
xPos = (int)(short) LOWORD(lParam);   // horizontal position 
yPos = (int)(short) HIWORD(lParam);   // vertical position 
```



También puede usar la macro [**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints) para convertir el parámetro *lParam* en una [**estructura POINTS.**](/previous-versions//dd162808(v=vs.85))

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía los mensajes **WM \_ SIZE** y **WM \_ MOVE** cuando procesa el [**mensaje \_ WINDOWPOSCHANGED de WM.**](wm-windowposchanged.md)
Los **mensajes WM \_ SIZE** y **WM \_ MOVE** no se envían si una aplicación controla el **mensaje \_ WINDOWPOSCHANGED** de WM sin llamar a **DefWindowProc**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**VENTANA \_ WMPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**MAKEPOINTS**](/windows/win32/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Puntos**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

 
