---
title: BCN_HOTITEMCHANGE de notificación (Commctrl.h)
description: Notifica al propietario del control de botón que el mouse entra o sale del área de cliente del control de botón. El control de botón envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: 92882e21-b69d-4326-94e9-ae69a0d00a83
keywords:
- BCN_HOTITEMCHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- BCN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6a7e64e95b45d0883b5adf34b384bccac8c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968728"
---
# <a name="bcn_hotitemchange-notification-code"></a>Código de notificación \_ HOTITEMCHANGE de BCN

Notifica al propietario del control de botón que el mouse entra o sale del área de cliente del control de botón. El control de botón envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
BCN_HOTITEMCHANGE

    pnmbchotitem = (NMBCHOTITEM*) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMBCHOTITEM.**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





