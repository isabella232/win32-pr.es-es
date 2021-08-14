---
title: CBEN_INSERTITEM de notificación (Commctrl.h)
description: Se envía cuando se ha insertado un nuevo elemento en el control . Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: caf60156-10d2-4cfb-91c4-def6ee99c471
keywords:
- CBEN_INSERTITEM código de notificación Windows controles
topic_type:
- apiref
api_name:
- CBEN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a58c1f8b14f4983e2f7e7444a8110f0407220b0c5bc682cfc73f72bee078ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413671"
---
# <a name="cben_insertitem-notification-code"></a>Código de \_ notificación INSERTITEM de CBEN

Se envía cuando se ha insertado un nuevo elemento en el control . Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
CBEN_INSERTITEM

    pNMInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) que contiene información sobre el código de notificación y el elemento que se insertó.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación que procesa este código de notificación debe devolver cero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





