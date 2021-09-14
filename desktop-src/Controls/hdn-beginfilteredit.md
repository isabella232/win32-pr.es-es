---
title: HDN_BEGINFILTEREDIT de notificación (Commctrl.h)
description: Notifica a la ventana primaria de un control de encabezado que ha comenzado una edición de filtro. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 93964453-bb94-4127-8ed4-41acb226b8e2
keywords:
- HDN_BEGINFILTEREDIT código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_BEGINFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0527427752b5621e626add17d61e60a675958f42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061957"
---
# <a name="hdn_beginfilteredit-notification-code"></a>Código de notificación \_ BEGINFILTEREDIT de HDN

Notifica a la ventana primaria de un control de encabezado que ha comenzado una edición de filtro. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_BEGINFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información adicional sobre el filtro que se está editando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





