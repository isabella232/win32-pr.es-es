---
description: Indica a una ventana de colocación de la imagen que actualice con la nueva información de DROPDESCRIPTION.
title: Mensaje DDWM_UPDATEWINDOW
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
ms.openlocfilehash: 2bff0e007c735fcf202aaf16cf304eb4ff5358f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984315"
---
# <a name="ddwm_updatewindow-message"></a>DDWM \_ UPDATEWINDOW

Indica a una ventana de colocación de la imagen que actualice con la nueva información de [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

No se utiliza.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

DDWM \_ UPDATEWINDOW se define como usuario de WM \_ + 3.

Cuando cambia el estado de una operación de colocar, por ejemplo, en respuesta a una tecla modificadora,[**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) devuelve un nuevo valor de [**DROPEFFECT**](../com/dropeffect-constants.md) (este valor de **DROPEFFECT** también se puede recibir a través de [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)). En respuesta, la aplicación actualiza la estructura [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) del destino de colocación con un nuevo valor [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) que indica la decoración que se va a aplicar al visual de la ventana de arrastre. por ejemplo, indica que el archivo se está copiando en lugar de moverse o que el objeto no se puede quitar a esa ubicación. Sin embargo, los objetos visuales no se actualizan hasta que el objeto recibe un mensaje **\_ UPDATEWINDOW de DDWM** .

El formato del portapapeles de [DragWindow](clipboard.md) proporciona el **hWnd** de la ventana de arrastre del destinatario al remitente del mensaje de **\_ UPDATEWINDOW de DDWM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



 

 
