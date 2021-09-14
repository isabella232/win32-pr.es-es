---
title: TCN_GETOBJECT de notificación (Commctrl.h)
description: Lo envía un control de pestaña cuando tiene el estilo extendido TCS EX REGISTERDROP y se arrastra un objeto sobre un elemento \_ \_ de ficha del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT código de notificación Windows controles
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
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166173"
---
# <a name="tcn_getobject-notification-code"></a>Código de notificación GETOBJECT de TCN \_

Lo envía un control de pestaña cuando tiene el estilo extendido [**TCS \_ EX \_ REGISTERDROP**](tab-control-extended-styles.md) y se arrastra un objeto sobre un elemento de ficha del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contiene información sobre el elemento de ficha sobre el que se arrastra el objeto y recibe datos que la aplicación devuelve en respuesta a este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación que procesa este código de notificación debe devolver cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





