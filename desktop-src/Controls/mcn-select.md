---
title: MCN_SELECT de notificación (Commctrl.h)
description: Enviado por un control de calendario mensual cuando el usuario realiza una selección de fecha explícita dentro de un control de calendario mensual. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT código de notificación Windows controles
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e71674ebccd9a896a92f701e65c7767866b64edac25208248f4683792b5261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018973"
---
# <a name="mcn_select-notification-code"></a>Código de notificación \_ DE MCN SELECT

Enviado por un control de calendario mensual cuando el usuario realiza una selección de fecha explícita dentro de un control de calendario mensual. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) que contiene información sobre el intervalo de fechas seleccionado actualmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **código de notificación DE \_ MCN SELECT** es similar a [**MCN \_ SELCHANGE,**](mcn-selchange.md)pero **MCN \_ SELECT** solo se envía en respuesta a las selecciones de fecha explícitas de un usuario. **MCN \_ SELCHANGE se** aplica a cualquier cambio de selección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





