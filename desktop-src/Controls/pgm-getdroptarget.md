---
title: Mensaje de PGM_GETDROPTARGET (commctrl. h)
description: Recupera el puntero de interfaz IDropTarget de un control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro GetDropTarget de buscapersonas \_ .
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- PGM_GETDROPTARGET controles de mensajes de Windows
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
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491789"
---
# <a name="pgm_getdroptarget-message"></a>\_Mensaje GETDROPTARGET PGM

Recupera el puntero de interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de un control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ GetDropTarget de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un puntero [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) que recibe el puntero de interfaz. Es responsabilidad del autor de la llamada llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en este puntero cuando ya no se necesita.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

