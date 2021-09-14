---
title: RB_GETTEXTCOLOR mensaje (Commctrl.h)
description: Recupera el color de texto predeterminado de un control rebar.
ms.assetid: fc9c731d-c606-4845-a119-737267301b29
keywords:
- RB_GETTEXTCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082079808aa553aaada5322cff16742dafa0b994
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167338"
---
# <a name="rb_gettextcolor-message"></a>Mensaje \_ GETTEXTCOLOR de RB

Recupera el color de texto predeterminado de un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un [**valor COLORREF**](/windows/desktop/gdi/colorref) que representa el color de texto predeterminado actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RB \_ SETTEXTCOLOR**](rb-settextcolor.md)
</dt> </dl>

 

