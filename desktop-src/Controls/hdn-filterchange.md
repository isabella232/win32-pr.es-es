---
title: Código de notificación de HDN_FILTERCHANGE (commctrl. h)
description: Notifica a la ventana primaria del control de encabezado que los atributos de un filtro de control de encabezado se están modificando o editando. Este código de notificación se envía en forma de mensaje de notificación de WM \_ .
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- HDN_FILTERCHANGE controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489269"
---
# <a name="hdn_filterchange-notification-code"></a>Código de notificación de FILTERCHANGE de HDN \_

Notifica a la ventana primaria del control de encabezado que los atributos de un filtro de control de encabezado se están modificando o editando. Este código de notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**HDM \_ SETFILTERCHANGETIMEOUT**](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





