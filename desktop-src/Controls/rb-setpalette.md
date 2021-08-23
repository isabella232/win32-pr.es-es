---
title: RB_SETPALETTE mensaje (Commctrl.h)
description: Establece la paleta actual del control rebar.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- RB_SETPALETTE controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85cd2968fa5fa74915e37f40f30dd47751e2316e8d91d0f51f9d3c7145b893fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434945"
---
# <a name="rb_setpalette-message"></a>Mensaje \_ SETPALETTE de RB

Establece la paleta actual del control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

**HPATTE que** especifica la nueva paleta que usará el control rebar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **HPATTE** que especifica la paleta anterior del control rebar.

## <a name="remarks"></a>Observaciones

Es responsabilidad de la aplicación que envía este mensaje eliminar el **HPATTE** pasado en este mensaje (vea [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). El control rebar no eliminará un **conjunto de HPATTE** con este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RB \_ GETPALETTE**](rb-getpalette.md)
</dt> </dl>

 

