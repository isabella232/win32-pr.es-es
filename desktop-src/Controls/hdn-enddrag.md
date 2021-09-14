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
ms.openlocfilehash: 8eef628dd8ff748829542ace76642e20ad97786f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061953"
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

## <a name="remarks"></a>Observaciones

Si el propietario realiza una administración externa (manual) de arrastrar y colocar, debe devolver **FALSE.** A continuación, el propietario debe reordenar los elementos de encabezado manualmente mediante el envío de [**HDM \_ SETITEM**](hdm-setitem.md) [**o HDM \_ SETORDERARRAY**](hdm-setorderarray.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





