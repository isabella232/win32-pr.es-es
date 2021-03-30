---
title: Mensaje de TCM_DESELECTALL (commctrl. h)
description: Restablece los elementos de un control de ficha, desactivando cualquier que se haya establecido en el \_ Estado TCIS BUTTONPRESSED. Puede enviar este mensaje explícitamente o mediante la macro TabCtrl \_ DeselectAll.
ms.assetid: cc2e5131-3c1b-473a-a0ca-274a2d39a2f1
keywords:
- TCM_DESELECTALL controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150975"
---
# <a name="tcm_deselectall-message"></a>\_Mensaje DESELECTALL de TCM

Restablece los elementos de un control de ficha, desactivando cualquier que se haya establecido en el estado [**TCIS \_ BUTTONPRESSED**](tab-control-item-states.md) . Puede enviar este mensaje explícitamente o mediante la macro [**TabCtrl \_ DeselectAll**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_deselectall) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Marca que especifica el ámbito de la anulación de la selección del elemento. Si este parámetro se establece en **false**, se restablecerán todos los elementos de ficha. Si se establece en **true**, se restablecerán todos los elementos de ficha excepto el seleccionado actualmente.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

## <a name="remarks"></a>Observaciones

Este mensaje solo es significativo si se ha establecido la marca de estilo [**\_ botones de TCS**](tab-control-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





