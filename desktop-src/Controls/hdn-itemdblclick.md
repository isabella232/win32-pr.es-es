---
title: HDN_ITEMDBLCLICK de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario ha hecho doble clic en el control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY. Solo los controles de encabezado establecidos en el estilo HDS \_ BUTTONS envían este código de notificación.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7117ceb8d17447eed8003f7da3dab70a17252c750bfb3885cd3f235a70b7bb53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544624"
---
# <a name="hdn_itemdblclick-notification-code"></a>Código de notificación \_ ITEMDBLCLICK de HDN

Notifica a la ventana primaria de un control de encabezado que el usuario ha hecho doble clic en el control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) Solo los controles de encabezado establecidos en el estilo [**HDS \_ BUTTONS**](header-control-styles.md) envían este código de notificación.


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ ITEMDBLCLICKW** (Unicode) y **HDN \_ ITEMDBLCLICKA** (ANSI)<br/>         |



 

 





