---
title: Mensaje de LVM_GETCALLBACKMASK (commctrl. h)
description: Obtiene la máscara de devolución de llamada para un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetCallbackMask de ListView.
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- LVM_GETCALLBACKMASK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68438b748f5260bb7cc6e43702442aa4cbe3a84e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489070"
---
# <a name="lvm_getcallbackmask-message"></a>\_Mensaje GETCALLBACKMASK LVM

Obtiene la máscara de devolución de llamada para un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetCallbackMask de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la máscara de devolución de llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





