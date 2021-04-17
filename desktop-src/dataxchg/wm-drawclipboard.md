---
title: Mensaje de WM_DRAWCLIPBOARD (Winuser. h)
description: Se envía a la primera ventana de la cadena del visor del portapapeles cuando cambia el contenido del portapapeles. Esto permite que una ventana del visor del portapapeles muestre el nuevo contenido del portapapeles. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- Intercambio de datos de mensajes de WM_DRAWCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665993"
---
# <a name="wm_drawclipboard-message"></a>Mensaje de DRAWCLIPBOARD de WM \_

Se envía a la primera ventana de la cadena del visor del portapapeles cuando cambia el contenido del portapapeles. Esto permite que una ventana del visor del portapapeles muestre el nuevo contenido del portapapeles.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Solo las ventanas del visor del portapapeles reciben este mensaje. Se trata de ventanas que se han agregado a la cadena del visor del portapapeles mediante la función [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .

Cada ventana que recibe el mensaje de **\_ DRAWCLIPBOARD de WM** debe llamar a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para pasar el mensaje a la siguiente ventana de la cadena del visor del portapapeles. [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)devuelve el identificador de la siguiente ventana de la cadena y puede cambiar en respuesta a un mensaje de [**\_ CHANGECBCHAIN de WM**](wm-changecbchain.md) .

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

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**CHANGECBCHAIN de WM \_**](wm-changecbchain.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

