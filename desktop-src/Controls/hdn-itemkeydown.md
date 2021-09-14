---
title: HDN_ITEMKEYDOWN de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de encabezado que se ha presionado una tecla con un elemento seleccionado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- HDN_ITEMKEYDOWN código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061936"
---
# <a name="hdn_itemkeydown-notification-code"></a>Código de notificación \_ DE HDN ITEMKEYDOWN

Notifica a la ventana primaria de un control de encabezado que se ha presionado una tecla con un elemento seleccionado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información adicional sobre la clave que se está pulsando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





