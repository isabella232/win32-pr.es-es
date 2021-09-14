---
title: HDN_FILTERCHANGE de notificación (Commctrl.h)
description: Notifica a la ventana primaria del control de encabezado que los atributos de un filtro de control de encabezado se están cambiando o editando. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- HDN_FILTERCHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061940"
---
# <a name="hdn_filterchange-notification-code"></a>Código de notificación FILTERCHANGE de HDN \_

Notifica a la ventana primaria del control de encabezado que los atributos de un filtro de control de encabezado se están cambiando o editando. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento de encabezado, incluidos los atributos que están a punto de cambiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**HDM \_ SETFILTERCHANGETIMEOUT**](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





