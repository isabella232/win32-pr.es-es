---
title: RBN_GETOBJECT de notificación (Commctrl.h)
description: Enviado por un control rebar creado con el estilo REGISTERDROP de RBS cuando se arrastra un objeto \_ sobre una banda del control. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- RBN_GETOBJECT de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167209"
---
# <a name="rbn_getobject-notification-code"></a>Código de notificación GETOBJECT de RBN \_

Enviado por un control rebar creado con el estilo [**\_ REGISTERDROP**](rebar-control-styles.md) de RBS cuando se arrastra un objeto sobre una banda del control. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a [**una estructura NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contiene información sobre la banda sobre la que se arrastra el objeto y también recibe los datos proporcionados por la aplicación receptora en respuesta a este código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto para este código de notificación debe ser cero.

## <a name="remarks"></a>Observaciones

Para recibir el código de notificación GETOBJECT de RBN, inicialice OLE con una llamada \_ a [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) o [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

