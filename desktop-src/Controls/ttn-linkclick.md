---
title: Código de notificación de TTN_LINKCLICK (commctrl. h)
description: Se envía cuando se hace clic en un vínculo de texto dentro de una información sobre herramientas de globo. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658231"
---
# <a name="ttn_linkclick-notification-code"></a>Código de notificación de LINKCLICK de TTN \_

Se envía cuando se hace clic en un vínculo de texto dentro de una información sobre herramientas de globo. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a>Parámetros

Este código de notificación no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="remarks"></a>Observaciones

El siguiente es un ejemplo de Cuándo se envía esta notificación. Supongamos que la información sobre herramientas de globo contiene el texto siguiente, "este es un <A>vínculo</A>". Cuando se hace clic en "link", el control ToolTip envía un \_ código de notificación TTN LINKCLICK.

> [!Note]  
> Para usar este código de notificación, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





