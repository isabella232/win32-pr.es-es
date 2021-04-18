---
title: Mensaje de HDM_GETFOCUSEDITEM (commctrl. h)
description: Obtiene el elemento de un control de encabezado que tiene el foco. Envíe este mensaje explícitamente o mediante la \_ macro header GetFocusedItem.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- HDM_GETFOCUSEDITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491477"
---
# <a name="hdm_getfocuseditem-message"></a>HDM \_ GETFOCUSEDITEM

Obtiene el elemento de un control de encabezado que tiene el foco. Envíe este mensaje explícitamente o mediante la macro [**Header \_ GetFocusedItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>No se utiliza. Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>No se utiliza. Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento en el foco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acerca de los controles de encabezado](header-controls.md)
</dt> </dl>

 

 





