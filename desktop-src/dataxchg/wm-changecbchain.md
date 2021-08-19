---
title: WM_CHANGECBCHAIN mensaje (Winuser.h)
description: Se envía a la primera ventana de la cadena de visor del Portapapeles cuando se quita una ventana de la cadena. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- WM_CHANGECBCHAIN mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25dac74784a214f77f8b2912e2fd643624ae767027121e2262d81989d54d3831
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736319"
---
# <a name="wm_changecbchain-message"></a>Mensaje \_ CHANGECBCHAIN de WM

Se envía a la primera ventana de la cadena de visor del Portapapeles cuando se quita una ventana de la cadena.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana que se va a quitar de la cadena de visor del Portapapeles.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la siguiente ventana de la cadena que sigue a la ventana que se va a quitar. Este parámetro es **NULL** si la ventana que se quita es la última ventana de la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Cada ventana del visor del Portapapeles guarda el identificador en la siguiente ventana de la cadena de visor del Portapapeles. Inicialmente, este identificador es el valor devuelto de la [**función SetClipboardViewer.**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)

Cuando una ventana del visor del Portapapeles recibe el mensaje **\_ CHANGECBCHAIN** de WM, debe llamar a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para pasar el mensaje a la siguiente ventana de la cadena, a menos que la ventana siguiente sea la ventana que se va a quitar. En este caso, el visor del Portapapeles debe guardar el identificador especificado por el parámetro *lParam* como la siguiente ventana de la cadena.

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

**Conceptual**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

