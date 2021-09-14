---
title: TCM_SETTOOLTIPS mensaje (Commctrl.h)
description: Asigna un control de información sobre herramientas a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ SetToolTips.
ms.assetid: c1b173b1-9da6-441a-a2b6-3875e2c343f8
keywords:
- TCM_SETTOOLTIPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e00166fb97c49c33b22811d28b79165bed4e9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166186"
---
# <a name="tcm_settooltips-message"></a>Mensaje \_ SETTOOLTIPS de TCM

Asigna un control de información sobre herramientas a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Controlar el control de información sobre herramientas.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Puede recuperar el control de información sobre herramientas asociado a un control de ficha mediante el mensaje [**\_ GETTOOLTIPS de TCM.**](tcm-gettooltips.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





