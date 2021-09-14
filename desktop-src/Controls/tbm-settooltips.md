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
ms.openlocfilehash: e8d60c7e108db926b85e7d9e1167f33c1ed807a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166406"
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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





