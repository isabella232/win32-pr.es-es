---
title: Mensaje de LVM_GETVIEWRECT (commctrl. h)
description: Recupera el rectángulo delimitador de todos los elementos del control de vista de lista. La vista de lista debe estar en el icono o en la vista de iconos pequeños. Puede enviar este mensaje explícitamente o mediante la \_ macro GetViewRect de ListView.
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- LVM_GETVIEWRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079650"
---
# <a name="lvm_getviewrect-message"></a>\_Mensaje GETVIEWRECT LVM

Recupera el rectángulo delimitador de todos los elementos del control de vista de lista. La vista de lista debe estar en el icono o en la vista de iconos pequeños. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetViewRect de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo delimitador. Todas las coordenadas son relativas al área visible del control de vista de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

