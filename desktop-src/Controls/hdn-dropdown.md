---
title: HDN_DROPDOWN de notificación (Commctrl.h)
description: Enviado por un control de encabezado a su elemento primario cuando se hace clic en la flecha desplegable del control de encabezado. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN código de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061954"
---
# <a name="hdn_dropdown-notification-code"></a>Código de notificación DESPLEGABLE de HDN \_

Enviado por un control de encabezado a su elemento primario cuando se hace clic en la flecha desplegable del control de encabezado. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

En el ejemplo de la sección Sintaxis se muestra cómo el receptor de notificaciones convierte **LPARAM** para recuperar la [**estructura NMHEADER.**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) **WPARAM** contiene el identificador del control que envía este mensaje.

Este mensaje solo se envía si el estilo HDF \_ SPLITBUTTON está establecido en el elemento de encabezado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





