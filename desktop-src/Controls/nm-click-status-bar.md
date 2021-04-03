---
title: Código de notificación de NM_CLICK (barra de estado) (commctrl. h)
description: Notifica a la ventana primaria de un control de barra de estado que el usuario ha pulsado el botón primario del mouse en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 179ccbe9-f51f-4356-b91a-10d7e3607b09
keywords:
- Código de notificación de NM_CLICK (barra de estado) controles de Windows
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6066f76a8cf0b6ca34b5298cfcdcba2b11e3fa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905690"
---
# <a name="nm_click-status-bar-notification-code"></a>NM- \_ código de notificación de clic (barra de estado)

Notifica a la ventana primaria de un control de barra de estado que el usuario ha pulsado el botón primario del mouse en el control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información adicional sobre esta notificación. El miembro **dwItemSpec** contiene el índice de la sección en la que se hizo clic.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** para indicar que se controló el clic del mouse y suprime el procesamiento predeterminado por parte del sistema. Devuelve **false** para permitir el procesamiento predeterminado del clic.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





