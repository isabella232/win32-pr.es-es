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
ms.openlocfilehash: c8bfec3b7272ceae3dcbf1781e3bb17a988f2252b3c0a74822677bff6ea39209
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104695"
---
# <a name="tcm_settooltips-message"></a>Mensaje \_ SETTOOLTIPS de TCM

Asigna un control de información sobre herramientas a un control de ficha. Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ SetToolTips.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_settooltips)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del control de información sobre herramientas.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Puede recuperar el control de información sobre herramientas asociado a un control de pestaña mediante el mensaje [**\_ GETTOOLTIPS de TCM.**](tcm-gettooltips.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





