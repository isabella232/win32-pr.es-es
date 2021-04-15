---
title: Código de notificación de TBN_RESTORE (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de restauración. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- TBN_RESTORE controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491975"
---
# <a name="tbn_restore-notification-code"></a>TBN \_ código de notificación de restauración

Notifica a la ventana primaria de una barra de herramientas que una barra de herramientas está en proceso de restauración. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación debe devolver cero en respuesta al primer código de notificación de **\_ restauración de TBN** recibido al inicio del proceso de restauración para seguir restaurando la información del botón. Si la aplicación devuelve un valor distinto de cero, se cancela el proceso de restauración.

## <a name="remarks"></a>Observaciones

La aplicación recibirá este código de notificación una vez al inicio del proceso de restauración y otra para cada botón. Este código de notificación ofrece la oportunidad de extraer la información del flujo de datos que guardó anteriormente. Si no ha guardado ninguna información, omita el código de notificación. Consulte [Personalización](toolbar-controls-overview.md) de la barra de herramientas para obtener una explicación más detallada de cómo controlar la **\_ restauración de TBN**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





