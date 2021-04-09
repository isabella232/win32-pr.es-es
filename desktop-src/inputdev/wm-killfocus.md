---
title: Mensaje de WM_KILLFOCUS (Winuser. h)
description: Se envía a una ventana inmediatamente antes de que pierda el foco de teclado.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- Entrada de mouse y teclado de mensaje de WM_KILLFOCUS
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e3bba54f2cdb500ba2ba691ffd30419d5beff1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079235"
---
# <a name="wm_killfocus-message"></a>Mensaje de KILLFOCUS de WM \_

Se envía a una ventana inmediatamente antes de que pierda el foco de teclado.


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana que recibe el foco de teclado. Este parámetro puede ser **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Si una aplicación muestra un símbolo de intercalación, el símbolo de intercalación debería destruirse en este momento.

Al procesar este mensaje, no realice ninguna llamada de función que muestre o Active una ventana. Esto hace que el subproceso produzca el control y puede hacer que la aplicación deje de responder a los mensajes. Para obtener más información, vea [interbloqueos de mensajes](/windows/desktop/winmsg/about-messages-and-message-queues).

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

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**SETFOCUS de WM \_**](wm-setfocus.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

