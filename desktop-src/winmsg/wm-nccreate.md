---
description: Se envía antes del mensaje \_ WM CREATE cuando se crea una ventana por primera vez.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: WM_NCCREATE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574340"
---
# <a name="wm_nccreate-message"></a>Mensaje \_ WM NCCREATE

Se envía antes del [**mensaje \_ WM CREATE**](wm-create.md) cuando se crea una ventana por primera vez.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a la [**estructura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) que contiene información sobre la ventana que se va a crear. Los miembros de **CREATESTRUCT** son idénticos a los parámetros de [**la función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si una aplicación procesa este mensaje, debe devolver **TRUE** para continuar con la creación de la ventana. Si la aplicación devuelve **FALSE**, la [**función CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) devolverá un **identificador NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**WM \_ CREATE**](wm-create.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
