---
title: HDM_GETITEMCOUNT mensaje (Commctrl.h)
description: Obtiene un recuento de los elementos de un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro Header \_ GetItemCount.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- HDM_GETITEMCOUNT controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4500277528cc76012631734d6f7316b29fdcb7a5a92cec3cf7b6bbb42693ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436035"
---
# <a name="hdm_getitemcount-message"></a>Mensaje \_ GETITEMCOUNT de HDM

Obtiene un recuento de los elementos de un control de encabezado. Puede enviar este mensaje explícitamente o usar la macro [**Header \_ GetItemCount.**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de elementos si se realiza correctamente o -1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





