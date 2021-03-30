---
title: Mensaje de TCM_GETTOOLTIPS (commctrl. h)
description: Recupera el identificador del control de información sobre herramientas asociado a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ GetToolTips.
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- TCM_GETTOOLTIPS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150971"
---
# <a name="tcm_gettooltips-message"></a>\_Mensaje GETTOOLTIPS de TCM

Recupera el identificador del control de información sobre herramientas asociado a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del control de información sobre herramientas si se realiza correctamente o **null** en caso contrario.

## <a name="remarks"></a>Observaciones

Un control de ficha crea un control de información sobre herramientas si tiene el estilo [**\_ información sobre herramientas de TCS**](tab-control-styles.md) . También puede asignar un control de información sobre herramientas a un control de ficha mediante el mensaje [**\_ SETTOOLTIPS de TCM**](tcm-settooltips.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





