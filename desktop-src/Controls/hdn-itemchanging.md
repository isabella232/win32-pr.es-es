---
title: HDN_ITEMCHANGING de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de encabezado que los atributos de un elemento de encabezado están a punto de cambiar. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- HDN_ITEMCHANGING código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061937"
---
# <a name="hdn_itemchanging-notification-code"></a>Código de notificación DE HDN \_ ITEMCHANGING

Notifica a la ventana primaria de un control de encabezado que los atributos de un elemento de encabezado están a punto de cambiar. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento de encabezado, incluidos los atributos que están a punto de cambiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **FALSE** para permitir los cambios o **TRUE** para evitarlos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ ITEMCHANGINGW** (Unicode) y **HDN \_ ITEMCHANGINGA** (ANSI)<br/>         |



 

 





