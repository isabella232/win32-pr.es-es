---
title: TBM_SETTOOLTIPS mensaje (Commctrl.h)
description: Asigna un control de información sobre herramientas a un control trackbar.
ms.assetid: 9bba1084-d04e-4631-a5cc-408849a14eb1
keywords:
- TBM_SETTOOLTIPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17aad8324946a96ab47344c2edc05abf76e02fba64a459b85f4af7b924bc7a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261395"
---
# <a name="tbm_settooltips-message"></a>Mensaje \_ SETTOOLTIPS de TBM

Asigna un control de información sobre herramientas a un control trackbar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de un control de información sobre herramientas existente.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

Cuando se crea un control trackbar con el estilo [**TBS \_ TOOLTIPS,**](trackbar-control-styles.md) crea un control de información sobre herramientas predeterminado que aparece junto al control deslizante y muestra la posición actual del control deslizante.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





