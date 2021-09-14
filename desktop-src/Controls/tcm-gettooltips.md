---
title: TCM_GETTOOLTIPS mensaje (Commctrl.h)
description: Recupera el identificador del control de información sobre herramientas asociado a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetToolTips.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- TCM_GETTOOLTIPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e49334a1fa7124dd6e7a0f0b739cd1ebd24b51b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166245"
---
# <a name="tcm_gettooltips-message"></a>Mensaje \_ GETTOOLTIPS de TCM

Recupera el identificador del control de información sobre herramientas asociado a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de información sobre herramientas si se realiza correctamente o NULL en **caso** contrario.

## <a name="remarks"></a>Observaciones

Un control de pestaña crea un control de información sobre herramientas si tiene el [**estilo DE INFORMACIÓN SOBRE HERRAMIENTAS DE \_ TCS.**](tab-control-styles.md) También puede asignar un control de información sobre herramientas a un control de pestaña mediante el mensaje [**\_ SETTOOLTIPS de TCM.**](tcm-settooltips.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





