---
title: HDN_OVERFLOWCLICK de notificación (Commctrl.h)
description: Enviado por un control de encabezado a su elemento primario cuando se hace clic en el botón de desbordamiento del encabezado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061933"
---
# <a name="hdn_overflowclick-notification-code"></a>Código de notificación DE HDN \_ OVERFLOWCLICK

Enviado por un control de encabezado a su elemento primario cuando se hace clic en el botón de desbordamiento del encabezado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* \[ En\]
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que describe el código de notificación. El proceso de llamada es responsable de asignar esta estructura, incluida la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) independiente. Establezca los miembros de la **estructura NMHDR,** incluido el *miembro* de código que debe establecerse en HDN \_ OVERFLOWCLICK.

Establezca el **miembro iItem** de la estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) en el índice del primer elemento de encabezado que no está visible y, por tanto, debe mostrarse en un desbordamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El receptor de notificaciones convierte **LPARAM** para recuperar la [**estructura NMHEADER.**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) **WPARAM** contiene el identificador del control que envía la notificación.

Este mensaje solo se envía cuando el [**estilo HDS \_ OVERFLOW**](header-control-styles.md) está establecido en el control de encabezado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





