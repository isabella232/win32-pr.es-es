---
title: Código de notificación de HDN_FILTERBTNCLICK (commctrl. h)
description: Notifica a la ventana primaria del control de encabezado cuando se hace clic en el botón de filtro o en respuesta a un \_ mensaje SETITEM de HDM. Este código de notificación se envía en forma de mensaje de notificación de WM \_ .
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905033"
---
# <a name="hdn_filterbtnclick-notification-code"></a>Código de notificación de FILTERBTNCLICK de HDN \_

Notifica a la ventana primaria del control de encabezado cuando se hace clic en el botón de filtro o en respuesta a un mensaje [**\_ SETITEM de HDM**](hdm-setitem.md) . Este código de notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) .


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

Si devuelve **true**, se enviará un código de notificación [HDN \_ FILTERCHANGE](hdn-filterchange.md) a la ventana primaria del control de encabezado. Este código de notificación proporciona a la ventana primaria una oportunidad para sincronizar sus elementos de la interfaz de usuario. Devuelve **false** si no desea que se envíe la notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





