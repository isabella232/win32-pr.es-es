---
title: HDM_SETFOCUSEDITEM mensaje (Commctrl.h)
description: Establece el foco en un elemento especificado de un control de encabezado. Envíe este mensaje explícitamente o mediante la macro \_ SetFocusedItem de encabezado.
ms.assetid: 20a321ce-4420-4239-b34d-9e7f24a89fc3
keywords:
- HDM_SETFOCUSEDITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_SETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd416744478248760f4e2c9f94a362db5a8d327
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061975"
---
# <a name="hdm_setfocuseditem-message"></a>Mensaje \_ SETFOCUSEDITEM de HDM

Establece el foco en un elemento especificado de un control de encabezado. Envíe este mensaje explícitamente o mediante la macro [**\_ SetFocusedItem de**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfocuseditem) encabezado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>No se usa. Debe ser cero.</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Índice del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Acerca de los controles de encabezado](header-controls.md)
</dt> </dl>

 

 





