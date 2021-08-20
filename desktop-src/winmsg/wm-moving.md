---
description: Se envía a una ventana que el usuario está moviendo. Al procesar este mensaje, una aplicación puede supervisar la posición del rectángulo de arrastre y, si es necesario, cambiar su posición.
ms.assetid: f56a36c1-dbaa-438a-9e52-d12697a9dac9
title: WM_MOVING mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45c27a985d8f048cc5e1b73f021b1bcf48c4f2ecf6fac435c85ea40aa8f6fc93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030794"
---
# <a name="wm_moving-message"></a>Mensaje \_ DE WM MOVING

Se envía a una ventana que el usuario está moviendo. Al procesar este mensaje, una aplicación puede supervisar la posición del rectángulo de arrastre y, si es necesario, cambiar su posición.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) con la posición actual de la ventana, en coordenadas de pantalla. Para cambiar la posición del rectángulo de arrastre, una aplicación debe cambiar los miembros de esta estructura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver **TRUE** si procesa este mensaje.

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

[**WM \_ MOVE**](wm-move.md)
</dt> <dt>

[**TAMAÑO \_ DE WM**](wm-sizing.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
