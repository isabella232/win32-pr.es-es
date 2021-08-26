---
title: LVM_GETCALLBACKMASK mensaje (Commctrl.h)
description: Obtiene la máscara de devolución de llamada para un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetCallbackMask.
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- LVM_GETCALLBACKMASK controles de Windows mensaje
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
ms.openlocfilehash: 58cbfec76df9418c2bc94e0083928f28e462188383a203237dd03f3f175c74b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920235"
---
# <a name="lvm_getcallbackmask-message"></a>Mensaje \_ GETCALLBACKMASK de LVM

Obtiene la máscara de devolución de llamada para un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetCallbackMask.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask)

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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





