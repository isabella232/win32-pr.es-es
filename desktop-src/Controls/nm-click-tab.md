---
title: Código de notificación de NM_CLICK (pestaña) (commctrl. h)
description: Notifica a la ventana primaria de un control de pestaña que el usuario ha haga clic en el botón primario del mouse dentro del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b892aded-d6b8-4a04-bfdd-0153b65eaccc
keywords:
- Controles de Windows de código de notificación de NM_CLICK (pestaña)
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e451a7a87d1b02140f59797c7485b8eb250dad13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151272"
---
# <a name="nm_click-tab-notification-code"></a>NM \_ código de notificación de clic (pestaña)

Notifica a la ventana primaria de un control de pestaña que el usuario ha haga clic en el botón primario del mouse dentro del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CLICK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control de pestaña omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





