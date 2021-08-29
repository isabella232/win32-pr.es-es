---
title: LVM_GETHEADER mensaje (Commctrl.h)
description: Obtiene el identificador del control de encabezado utilizado por el control list-view. Puede enviar este mensaje explícitamente o usar la macro ListView \_ GetHeader.
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- LVM_GETHEADER controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETHEADER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d372085a6b8c81b61bc375bade7f4c9c502fc5cba38cc7c44039a881af2ada9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062595"
---
# <a name="lvm_getheader-message"></a>Mensaje \_ GETHEADER de LVM

Obtiene el identificador del control de encabezado utilizado por el control list-view. Puede enviar este mensaje explícitamente o usar la macro [**ListView \_ GetHeader.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de encabezado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





