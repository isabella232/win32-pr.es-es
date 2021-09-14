---
title: WM_DRAWCLIPBOARD mensaje (Winuser.h)
description: Se envía a la primera ventana de la cadena de visor del Portapapeles cuando cambia el contenido del Portapapeles. Esto permite que una ventana del visor del Portapapeles muestre el nuevo contenido del Portapapeles. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- WM_DRAWCLIPBOARD mensaje Data Exchange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174869"
---
# <a name="wm_drawclipboard-message"></a>Mensaje \_ DRAWCLIPBOARD de WM

Se envía a la primera ventana de la cadena de visor del Portapapeles cuando cambia el contenido del Portapapeles. Esto permite que una ventana del visor del Portapapeles muestre el nuevo contenido del Portapapeles.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Solo las ventanas del visor del Portapapeles reciben este mensaje. Se trata de ventanas que se han agregado a la cadena de visores del Portapapeles mediante la [**función SetClipboardViewer.**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)

Cada ventana que recibe el **mensaje \_ DRAWCLIPBOARD** de WM debe llamar a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para pasar el mensaje a la siguiente ventana de la cadena de visor del Portapapeles. [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)devuelve el identificador de la siguiente ventana de la cadena y puede cambiar en respuesta a un [**mensaje \_ CHANGECBCHAIN**](wm-changecbchain.md) de WM.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**WM \_ CHANGECBCHAIN**](wm-changecbchain.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

