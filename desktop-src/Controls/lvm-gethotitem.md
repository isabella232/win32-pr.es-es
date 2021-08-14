---
title: LVM_GETHOTITEM mensaje (Commctrl.h)
description: Recupera el índice del elemento de acceso actual. Puede enviar este mensaje explícitamente o usar la macro ListView \_ GetHotItem.
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- LVM_GETHOTITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 743bd7a80a58bec41fa5a75f24b0e333ab33ad152909adb6ea69a9c4ca0fd78b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958405"
---
# <a name="lvm_gethotitem-message"></a>Mensaje \_ GETHOTITEM de LVM

Recupera el índice del elemento de acceso actual. Puede enviar este mensaje explícitamente o usar la macro [**ListView \_ GetHotItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento que está en caliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





