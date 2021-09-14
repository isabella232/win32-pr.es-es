---
title: LVN_GETINFOTIP de notificación (Commctrl.h)
description: Enviado por un control de vista de lista y vista de icono grande que tiene el estilo \_ extendido LVS EX \_ INFOTIP.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP de notificación Windows controles
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
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362595"
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

## <a name="remarks"></a>Observaciones

Este código de notificación solo se envía mediante controles de vista de lista que tienen el estilo [**\_ extendido LVS EX \_ INFOTIP.**](extended-list-view-styles.md) El código de notificación \_ LVN GETINFOTIP solo se envía para el subelemento 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVN \_ GETINFOTIPW** (Unicode) y **LVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





