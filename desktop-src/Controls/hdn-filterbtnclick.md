---
title: HDN_FILTERBTNCLICK de notificación (Commctrl.h)
description: Notifica a la ventana primaria del control de encabezado cuando se hace clic en el botón de filtro o en respuesta a un mensaje \_ SETITEM de HDM. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061950"
---
# <a name="hdn_filterbtnclick-notification-code"></a>Código de notificación \_ FILTERBTNCLICK de HDN

Notifica a la ventana primaria del control de encabezado cuando se hace clic en el botón de filtro o en respuesta a un [**mensaje \_ SETITEM de HDM.**](hdm-setitem.md) Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) que contiene información sobre el control de encabezado y el botón de filtro de encabezado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si devuelve **TRUE**, se enviará un código de [notificación \_ FILTERCHANGE](hdn-filterchange.md) de HDN a la ventana primaria del control de encabezado. Este código de notificación ofrece a la ventana primaria la oportunidad de sincronizar sus elementos de interfaz de usuario. Devuelve **FALSE** si no quieres que se envíe la notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





