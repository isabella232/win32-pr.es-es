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
ms.openlocfilehash: fa9e8dc1c0cad3e60bdde3f3c05d77d8c57b98ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167694"
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

## <a name="remarks"></a>Observaciones

De forma predeterminada, el control de paginación usará el color de la cara del botón del sistema como color de fondo. Este es el mismo color que se puede recuperar llamando a [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con COLOR \_ BTNFACE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

