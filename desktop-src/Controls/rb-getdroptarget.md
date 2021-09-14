---
title: RB_GETDROPTARGET mensaje (Commctrl.h)
description: Recupera el puntero de interfaz IDropTarget de un control rebar.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- RB_GETDROPTARGET controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167365"
---
# <a name="rb_getdroptarget-message"></a>Mensaje \_ GETDROPTARGET de RB

Recupera el puntero de interfaz [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un [**puntero IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) que recibe el puntero de interfaz. Es responsabilidad del autor de la llamada llamar a [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en este puntero cuando ya no sea necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

