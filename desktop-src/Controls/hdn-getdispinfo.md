---
title: Código de notificación de HDN_GETDISPINFO (commctrl. h)
description: Se envía al propietario de un control de encabezado cuando el control necesita información sobre un elemento de encabezado de devolución de llamada. Este código de notificación se envía como un mensaje de notificación de WM \_ .
ms.assetid: 51522df0-83ae-4d9a-a8fc-31083e24242a
keywords:
- HDN_GETDISPINFO controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078945"
---
# <a name="hdn_getdispinfo-notification-code"></a>Código de notificación de GETDISPINFO de HDN \_

Se envía al propietario de un control de encabezado cuando el control necesita información sobre un elemento de encabezado de devolución de llamada. Este código de notificación se envía como un mensaje de notificación de [**WM \_**](wm-notify.md) .


```C++
HDN_GETDISPINFO

   pNMHDDispInfo = (LPNMHDDISPINFO) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) . En la entrada, los campos de la estructura especifican qué información se requiere y el elemento de interés.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un LRESULT.

## <a name="remarks"></a>Observaciones

Rellene los miembros adecuados de la estructura para devolver la información solicitada al control de encabezado. Si el controlador de mensajes establece el miembro de **máscara** de la estructura [**NMHDDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmhddispinfoa) en HDI \_ di \_ SETITEM, el control de encabezado almacena la información y no la volverá a solicitar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ GETDISPINFOW** (Unicode) y **HDN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





