---
title: HDM_DELETEITEM mensaje (Commctrl.h)
description: Elimina un elemento de un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro Header \_ DeleteItem.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- HDM_DELETEITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b0a48d769117ffd68f2ba2af9695fe7fce00031f297626ae48c111d4574dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697355"
---
# <a name="hdm_deleteitem-message"></a>Mensaje \_ DELETEITEM de HDM

Elimina un elemento de un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro [**Header \_ DeleteItem.**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento que se eliminará.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





