---
title: Código de notificación de NM_TOOLTIPSCREATED (barra de herramientas) (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que la barra de herramientas ha creado un control ToolTip. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0e9517c1-aa3f-4b14-82b4-195a4ce99757
keywords:
- Código de notificación de NM_TOOLTIPSCREATED (barra de herramientas) controles de Windows
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
ms.openlocfilehash: c13366348da075fab48e7a2f12381f51f7d87bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489953"
---
# <a name="nm_tooltipscreated-toolbar-notification-code"></a>NM \_ TOOLTIPSCREATED (barra de herramientas) código de notificación

Notifica a la ventana primaria de una barra de herramientas que la barra de herramientas ha creado un control ToolTip. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMTOOLTIPSCREATED) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control de barra de herramientas omite el valor devuelto de este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





