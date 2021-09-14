---
title: TCM_DESELECTALL mensaje (Commctrl.h)
description: Restablece los elementos de un control de ficha y borra los que se han establecido en el estado \_ BUTTONPRESSED de TCIS. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ DeselectAll.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- TCM_DESELECTALL controles de Windows mensaje
topic_type:
- apiref
api_name:
- TCM_DESELECTALL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f606538075a9163d8b8dc8328b5585b51b769aa5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166285"
---
# <a name="tcm_deselectall-message"></a>Mensaje \_ TCM DESELECTALL

Restablece los elementos de un control de ficha y borra los que se han establecido en el [**estado \_ BUTTONPRESSED de TCIS.**](tab-control-item-states.md) Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ DeselectAll.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca que especifica el ámbito de la anulación de selección del elemento. Si este parámetro se establece en **FALSE,** se restablecerán todos los elementos de ficha. Si se establece en **TRUE,** se restablecerán todos los elementos de ficha excepto el seleccionado actualmente.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

Este mensaje solo es significativo si se ha [**establecido la marca de estilo \_ TCS BUTTONS.**](tab-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





