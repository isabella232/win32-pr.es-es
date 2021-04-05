---
title: Mensaje de LVM_GETEDITCONTROL (commctrl. h)
description: Obtiene el identificador del control de edición que se usa para editar el texto de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetEditControl de ListView.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- LVM_GETEDITCONTROL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078869"
---
# <a name="lvm_geteditcontrol-message"></a>\_Mensaje GETEDITCONTROL LVM

Obtiene el identificador del control de edición que se usa para editar el texto de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetEditControl de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control de edición si se realiza correctamente, o **null** en caso contrario.

## <a name="remarks"></a>Observaciones

Cuando comienza la edición de etiquetas, se crea, coloca y Inicializa un control de edición. Antes de que se muestre, el control de vista de lista envía a su ventana primaria un código de notificación [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) .

Para personalizar la edición de etiquetas, implemente un controlador para [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) y envíe un mensaje **LVM \_ GETEDITCONTROL** al control de vista de lista. Si se está editando una etiqueta, el valor devuelto será un identificador del control de edición. Use este identificador para personalizar el control de edición mediante el envío de los mensajes de **em \_ XXX** habituales.

Cuando el usuario finaliza o cancela la edición, el control de edición se destruye y el identificador ya no es válido. Puede crear una subclase del control de edición, pero no debe destruirlo. Para cancelar la edición, envíe un mensaje de [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) al control de vista de lista.

El elemento de vista de lista que se está editando es el elemento que tiene actualmente el foco, es decir, el elemento en el estado Focused. Para buscar un elemento en función de su estado, use el mensaje [**\_ GETNEXTITEM de LVM**](lvm-getnextitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetEditControl de ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

