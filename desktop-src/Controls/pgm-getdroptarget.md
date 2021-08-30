---
title: PGM_GETDROPTARGET mensaje (Commctrl.h)
description: Recupera el puntero de interfaz IDropTarget de un control de paginación. Puede enviar este mensaje explícitamente o usar la \_ macro GetDropTarget de Pager.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- PGM_GETDROPTARGET controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d07add613674166ebc4bf4cba460088e5e95d9704eead5ad382851bf4e79f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985904"
---
# <a name="pgm_getdroptarget-message"></a>Mensaje \_ GETDROPTARGET de PGM

Recupera el puntero de interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de un control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**\_ GetDropTarget de Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un [**puntero IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) que recibe el puntero de interfaz. Es responsabilidad del autor de la llamada llamar a [**Release en**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) este puntero cuando ya no es necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

