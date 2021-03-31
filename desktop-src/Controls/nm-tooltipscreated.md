---
title: Código de notificación de NM_TOOLTIPSCREATED (commctrl. h)
description: Notifica a la ventana primaria de un control que el control ha creado un control ToolTip. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- NM_TOOLTIPSCREATED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2e99850b17b0f2b06948a09b70a89e67e65a50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079199"
---
# <a name="nm_tooltipscreated-notification-code"></a>Código de notificación de NM \_ TOOLTIPSCREATED

Notifica a la ventana primaria de un control que el control ha creado un control ToolTip. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

A menos que se especifique lo contrario, el control omite el valor devuelto de este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





