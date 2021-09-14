---
title: TBN_RESTORE de notificación (Commctrl.h)
description: Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de restauración. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- TBN_RESTORE código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 374ed0fb68accbb65515d39ea01f237707eb16c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166321"
---
# <a name="tbn_restore-notification-code"></a>Código de notificación RESTORE de TBN \_

Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de restauración. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTBRESTORE.**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación debe devolver cero en respuesta al primer código de notificación **\_ RESTORE de TBN** recibido al principio del proceso de restauración para continuar restaurando la información del botón. Si la aplicación devuelve un valor distinto de cero, se cancela el proceso de restauración.

## <a name="remarks"></a>Observaciones

La aplicación recibirá este código de notificación una vez al principio del proceso de restauración y una vez para cada botón. Este código de notificación le ofrece la oportunidad de extraer la información del flujo de datos que guardó anteriormente. Si no ha guardado ninguna información, ignore el código de notificación. Vea [Personalización de la](toolbar-controls-overview.md) barra de herramientas para obtener una explicación más detallada de cómo controlar **TBN \_ RESTORE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





