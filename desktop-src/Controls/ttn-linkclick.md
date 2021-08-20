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
ms.openlocfilehash: a2a31b1f942627ee22fb050bbddd0b74ac10dd09a7a8f14018189620f6c8155f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166101"
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

## <a name="remarks"></a>Comentarios

A continuación se muestra un ejemplo de cuándo se envía esta notificación. Suponga que la información sobre herramientas del globo contiene el texto siguiente, "This is a link" (Este es <A>un vínculo).</A> Cuando se hace clic en "vínculo", el control de información sobre herramientas envía un código de notificación \_ LINKCLICK de TTN.

> [!Note]  
> Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





