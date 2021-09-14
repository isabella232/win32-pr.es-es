---
title: HDN_GETDISPINFO de notificación (Commctrl.h)
description: Se envía al propietario de un control de encabezado cuando el control necesita información sobre un elemento de encabezado de devolución de llamada. Este código de notificación se envía como un mensaje WM \_ NOTIFY.
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_GETDISPINFO
- HDN_GETDISPINFOA
- HDN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45fe753b610fae69956b89caadade394566d0dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061939"
---
# <a name="hdn_getdispinfo-notification-code"></a>Código de notificación \_ GETDISPINFO de HDN

Se envía al propietario de un control de encabezado cuando el control necesita información sobre un elemento de encabezado de devolución de llamada. Este código de notificación se envía como un [**mensaje WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMHDDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) En la entrada, los campos de la estructura especifican qué información es necesaria y el elemento de interés.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un LRESULT.

## <a name="remarks"></a>Observaciones

Rellene los miembros adecuados de la estructura para devolver la información solicitada al control de encabezado. Si el controlador de mensajes establece el miembro **mask** de la estructura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) en HDI DI SETITEM, el control de encabezado almacena la información y no la \_ \_ volverá a solicitar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ GETDISPINFOW** (Unicode) y **HDN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





