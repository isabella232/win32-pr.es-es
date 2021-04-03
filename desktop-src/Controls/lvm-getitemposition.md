---
title: Mensaje de LVM_GETITEMPOSITION (commctrl. h)
description: Recupera la posición de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetItemPosition de ListView.
ms.assetid: e5841089-c34e-498e-b94c-45c845bfc747
keywords:
- LVM_GETITEMPOSITION controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMPOSITION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f40b5899634e2f357068caa6ef96339be82f600b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905508"
---
# <a name="lvm_getitemposition-message"></a>\_Mensaje GETITEMPOSITION LVM

Recupera la posición de un elemento de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetItemPosition de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemposition) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) que recibe la posición de la esquina superior izquierda del elemento, en coordenadas de la vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

