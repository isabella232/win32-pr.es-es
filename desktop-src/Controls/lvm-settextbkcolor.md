---
title: Mensaje de LVM_SETTEXTBKCOLOR (commctrl. h)
description: Establece el color de fondo del texto en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetTextBkColor de ListView.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- LVM_SETTEXTBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079204"
---
# <a name="lvm_settextbkcolor-message"></a>\_Mensaje SETTEXTBKCOLOR LVM

Establece el color de fondo del texto en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetTextBkColor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nuevo color de fondo del texto. Puede ser CLR \_ None para ningún color de fondo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





