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
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167278"
---
# <a name="rb_setpalette-message"></a>Mensaje \_ SETPALETTE de RB

Establece la paleta actual del control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

**HPALETTE que** especifica la nueva paleta que usará el control rebar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve una **HPALETTE** que especifica la paleta anterior del control rebar.

## <a name="remarks"></a>Observaciones

Es responsabilidad de la aplicación que envía este mensaje eliminar el **HPALETTE** pasado en este mensaje (vea [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)). El control rebar no eliminará un **conjunto HPALETTE** con este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RB \_ GETPALETTE**](rb-getpalette.md)
</dt> </dl>

 

