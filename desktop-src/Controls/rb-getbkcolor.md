---
title: RB_GETBKCOLOR mensaje (Commctrl.h)
description: Recupera el color de fondo predeterminado de un control rebar.
ms.assetid: be90d1ce-a1f8-446d-ae64-001f7174ab05
keywords:
- RB_GETBKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56e2b6c60076d878ddea275f5383f98c5a92ee868e00074c716c113382b7678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085005"
---
# <a name="rb_getbkcolor-message"></a>Mensaje \_ GETBKCOLOR de RB

Recupera el color de fondo predeterminado de un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un [**valor COLORREF**](/windows/desktop/gdi/colorref) que representa el color de fondo predeterminado actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RB \_ SETBKCOLOR**](rb-setbkcolor.md)
</dt> </dl>

 

