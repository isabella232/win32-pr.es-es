---
title: WM_SETFOCUS mensaje (Winuser.h)
description: Se envía a una ventana después de que haya obtenido el foco del teclado.
ms.assetid: 77180e4c-95a6-41a4-93d9-033381ae7543
keywords:
- WM_SETFOCUS entrada de teclado y mouse
topic_type:
- apiref
api_name:
- WM_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ba202a4f0205a28d294d2d4f54372921205ebb72516f6f26c4042e08d9cfe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757378"
---
# <a name="wm_setfocus-message"></a>Mensaje \_ SETFOCUS de WM

Se envía a una ventana después de que haya obtenido el foco del teclado.


```C++
#define WM_SETFOCUS                     0x0007
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana que ha perdido el foco del teclado. Este parámetro puede ser **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Para mostrar un caret, una aplicación debe llamar a las funciones de caret adecuadas cuando recibe el **mensaje \_ SETFOCUS de WM.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**Setfocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**WM \_ KILLFOCUS**](wm-killfocus.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

