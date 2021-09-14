---
title: TTN_LINKCLICK de notificación (Commctrl.h)
description: Se envía cuando se hace clic en un vínculo de texto dentro de la información sobre herramientas de un globo. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK código de notificación Windows controles
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165810"
---
# <a name="ttn_linkclick-notification-code"></a>Código de notificación de TTN \_ LINKCLICK

Se envía cuando se hace clic en un vínculo de texto dentro de la información sobre herramientas de un globo. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a>Parámetros

Este código de notificación no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Valor devuelto no utilizado.

## <a name="remarks"></a>Observaciones

A continuación se muestra un ejemplo de cuándo se envía esta notificación. Supongamos que la información sobre herramientas del globo contiene el texto siguiente, "This is a link" (Este es <A>un vínculo).</A> Cuando se hace clic en "vínculo", el control de información sobre herramientas envía un código de notificación \_ LINKCLICK de TTN.

> [!Note]  
> Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





