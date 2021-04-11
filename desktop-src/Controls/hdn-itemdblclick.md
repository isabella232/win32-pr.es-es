---
title: Código de notificación de HDN_ITEMDBLCLICK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario hizo doble clic en el control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM. Solo los controles de encabezado que se establecen en el estilo de los botones de HDS \_ envían este código de notificación.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- HDN_ITEMDBLCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e61117303ecc478a998da8799867988dbc1ca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274547"
---
# <a name="hdn_itemdblclick-notification-code"></a>Código de notificación de ITEMDBLCLICK de HDN \_

Notifica a la ventana primaria de un control de encabezado que el usuario hizo doble clic en el control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . Solo los controles de encabezado que se establecen en el estilo de los [**\_ botones de HDS**](header-control-styles.md) envían este código de notificación.


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ ITEMDBLCLICKW** (Unicode) y **HDN \_ ITEMDBLCLICKA** (ANSI)<br/>         |



 

 





