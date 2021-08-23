---
title: TCN_GETOBJECT de notificación (Commctrl.h)
description: Enviado por un control de pestaña cuando tiene el estilo extendido TCS EX REGISTERDROP y un objeto se arrastra sobre un elemento \_ \_ de pestaña del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT de notificación Windows controles
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf5ec3a314a7380ccff5f8613145c890f8f304d73289ad5354b8668a09070b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166908"
---
# <a name="tcn_getobject-notification-code"></a>Código de notificación GETOBJECT de TCN \_

Enviado por un control de pestaña cuando tiene el estilo extendido [**TCS \_ EX \_ REGISTERDROP**](tab-control-extended-styles.md) y un objeto se arrastra sobre un elemento de pestaña del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contiene información sobre el elemento de tabulación sobre el que se arrastra el objeto y recibe datos que la aplicación devuelve en respuesta a este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación que procesa este código de notificación debe devolver cero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





