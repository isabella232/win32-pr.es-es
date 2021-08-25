---
title: TBN_DELETINGBUTTON mensaje (Commctrl.h)
description: Enviado por un control de barra de herramientas cuando un botón está a punto de eliminarse. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 08116071-36d6-456b-88f9-62a22cdb7ed9
keywords:
- TBN_DELETINGBUTTON controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBN_DELETINGBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a426d32af308d6d254a4221bbf35b103b401f07ab1ba6fa74801b6debd46ab70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876975"
---
# <a name="tbn_deletingbutton-message"></a>Mensaje \_ DELETINGBUTTON de TBN

Enviado por un control de barra de herramientas cuando un botón está a punto de eliminarse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
 TBN_DELETINGBUTTON 

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contiene información sobre el botón que se va a eliminar. Para este código de notificación, solo los **miembros hdr** **e iItem** de esta estructura son válidos. El **miembro iItem** de esta estructura contiene el identificador de comando del botón que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





