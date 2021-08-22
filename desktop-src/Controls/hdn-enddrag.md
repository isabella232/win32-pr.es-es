---
title: HDN_ENDDRAG de notificación (Commctrl.h)
description: Enviado por un control de encabezado cuando una operación de arrastre ha finalizado en uno de sus elementos. Este código de notificación se envía como un mensaje \_ WM NOTIFY. Solo los controles de encabezado que se establecen en el estilo DRAGDROP de HDS \_ envían este código de notificación.
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG de notificación Windows controles
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df56beb0b5b4a75716723330711714b7db9f4f27100ffe3296626d2be5798a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544625"
---
# <a name="hdn_enddrag-notification-code"></a>Código de notificación \_ ENDDRAG de HDN

Enviado por un control de encabezado cuando una operación de arrastre ha finalizado en uno de sus elementos. Este código de notificación se envía como un [**mensaje \_ WM NOTIFY.**](wm-notify.md) Solo los controles de encabezado que se establecen en el [**estilo \_ DRAGDROP**](header-control-styles.md) de HDS envían este código de notificación.


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el elemento de encabezado que se estaba arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para permitir que el control coloque y reordene automáticamente el elemento, devuelva **FALSE**. Para evitar que se coloque el elemento, devuelva **TRUE**.

## <a name="remarks"></a>Comentarios

Si el propietario realiza una administración externa (manual) de arrastrar y colocar, debe devolver **FALSE.** A continuación, el propietario debe reordenar los elementos de encabezado manualmente mediante el envío de [**HDM \_ SETITEM**](hdm-setitem.md) [**o HDM \_ SETORDERARRAY**](hdm-setorderarray.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





