---
description: Se envía a una ventana que el usuario está moviendo. Al procesar este mensaje, una aplicación puede supervisar la posición del rectángulo de arrastre y, si es necesario, cambiar su posición.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: Mensaje de WM_MOVING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5847189d64601ec999321920ead716fbdf22e2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677361"
---
# <a name="wm_moving-message"></a>Mensaje de movimiento de WM \_

Se envía a una ventana que el usuario está moviendo. Al procesar este mensaje, una aplicación puede supervisar la posición del rectángulo de arrastre y, si es necesario, cambiar su posición.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_MOVING                       0x0216
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) con la posición actual de la ventana, en coordenadas de la pantalla. Para cambiar la posición del rectángulo de arrastre, una aplicación debe cambiar los miembros de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver **true** si procesa este mensaje.

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

[**movimiento de WM \_**](wm-move.md)
</dt> <dt>

[**tamaño de WM \_**](wm-sizing.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
