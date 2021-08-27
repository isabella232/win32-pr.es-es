---
description: Indica a una ventana de quitar imagen que se actualice con la nueva información dropdescription.
title: DDWM_UPDATEWINDOW mensaje
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a17e015d6dff2ae5133f3ce8245c5ead3c3381f8eb5c48e74946fdf9bcb46ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032843"
---
# <a name="ddwm_updatewindow-message"></a>Mensaje UPDATEWINDOW de DDWM \_

Indica a una ventana de quitar imagen que se actualice con la [**nueva información DROPDESCRIPTION.**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

No se usa.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

DDWM \_ UPDATEWINDOW se define como WM \_ USER+3.

Cuando cambia el estado de una operación de colocación(por ejemplo, en respuesta a una tecla modificadora),[**IDropTarget::D ragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) devuelve un nuevo valor [**DROPEFFECT**](../com/dropeffect-constants.md) (este valor **DROPEFFECT** también se puede recibir a través de [**IDropSource::GiveFeedback).**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback) En respuesta, la aplicación actualiza la estructura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) del destino de colocación con un nuevo valor [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) que indica la decoración que se va a aplicar al objeto visual de la ventana de arrastre. Por ejemplo, una indicación de que el archivo se está copiando en lugar de moverse o que el objeto no se puede eliminar en esa ubicación. Sin embargo, los objetos visuales no se actualizan hasta que el objeto recibe un mensaje **\_ UPDATEWINDOW de DDWM.**

El [formato del Portapapeles DragWindow](clipboard.md) proporciona el **HWND** de la ventana de arrastre del destinatario al remitente del mensaje **\_ UPDATEWINDOW de DDWM.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



 

 
