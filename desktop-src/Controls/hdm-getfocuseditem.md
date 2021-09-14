---
title: HDM_GETFOCUSEDITEM mensaje (Commctrl.h)
description: Obtiene el elemento de un control de encabezado que tiene el foco. Envíe este mensaje explícitamente o mediante la macro \_ GetFocusedItem de encabezado.
ms.assetid: 9ad8e497-6f81-4226-b138-d1101f2fd8b3
keywords:
- HDM_GETFOCUSEDITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_GETFOCUSEDITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c21fcb29f5f431e32ca3f07265b7e96620d5a67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061995"
---
# <a name="hdm_getfocuseditem-message"></a>Mensaje \_ GETFOCUSEDITEM de HDM

Obtiene el elemento de un control de encabezado que tiene el foco. Envíe este mensaje explícitamente o mediante la macro [**\_ GetFocusedItem de**](/windows/desktop/api/Commctrl/nf-commctrl-header_getfocuseditem) encabezado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>No se usa. Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>No se usa. Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento en el foco.

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

 

 





