---
title: TBN_HOTITEMCHANGE de notificación (Commctrl.h)
description: Enviado por un control de barra de herramientas cuando cambia el elemento de acceso rápido (resaltado). Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- TBN_HOTITEMCHANGE de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166338"
---
# <a name="tbn_hotitemchange-notification-code"></a>Código de notificación \_ HOTITEMCHANGE de TBN

Enviado por un control de barra de herramientas cuando cambia el elemento de acceso rápido (resaltado). Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) que contiene información sobre este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir que se resalte el elemento o distinto de cero para evitar que se resalte el elemento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





