---
title: LVN_GETINFOTIP de notificación (Commctrl.h)
description: Enviado por un control de vista de lista y vista de icono grande que tiene el estilo \_ extendido LVS EX \_ INFOTIP.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP código de notificación Windows controles
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f7477230913ec5efd0827bc48e1a6021619aa4cdbbad252426d1af364b5b36b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830446"
---
# <a name="lvn_getinfotip-notification-code"></a>Código de notificación \_ GETINFOTIP lvn

Enviado por un control de vista de lista y vista de icono grande que tiene el estilo [**\_ extendido LVS EX \_ INFOTIP.**](extended-list-view-styles.md) Este código de notificación se envía cuando el control list-view solicita información de texto adicional que se va a mostrar en una información sobre herramientas. Se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) que contiene información sobre este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="remarks"></a>Comentarios

Este código de notificación solo se envía mediante controles de vista de lista que tienen el estilo [**\_ extendido LVS EX \_ INFOTIP.**](extended-list-view-styles.md) El código de notificación \_ LVN GETINFOTIP solo se envía para el subelemento 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ GETINFOTIPW** (Unicode) y **LVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





