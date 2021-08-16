---
title: PGM_SETBKCOLOR mensaje (Commctrl.h)
description: Establece el color de fondo actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la \_ macro SetBkColor de Pager.
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- PGM_SETBKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d727bf401fae3b8c58b96fe8b5190a3ad427abb40b0478d59de087add553ddf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830186"
---
# <a name="pgm_setbkcolor-message"></a>Mensaje \_ SETBKCOLOR de PGM

Establece el color de fondo actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetBkColor de Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

**Valor COLORREF** que contiene el nuevo color de fondo del control de paginación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor COLORREF** que contiene el color de fondo anterior.

## <a name="remarks"></a>Comentarios

De forma predeterminada, el control de paginación usará el color de la cara del botón del sistema como color de fondo. Este es el mismo color que se puede recuperar llamando a [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con COLOR \_ BTNFACE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

