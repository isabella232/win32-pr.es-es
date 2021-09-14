---
title: PGM_GETBKCOLOR mensaje (Commctrl.h)
description: Recupera el color de fondo actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la \_ macro GetBkColor de Pager.
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- PGM_GETBKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b58b139dd1caafcdefc6893e2b8a5e3312d3e28
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167726"
---
# <a name="pgm_getbkcolor-message"></a>Mensaje \_ GETBKCOLOR de PGM

Recupera el color de fondo actual para el control de paginación. Puede enviar este mensaje explícitamente o usar la macro [**\_ GetBkColor de Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor COLORREF** que contiene el color de fondo actual.

## <a name="remarks"></a>Observaciones

De forma predeterminada, el control de paginación usará el color de la cara del botón del sistema como color de fondo. Este es el mismo color que se puede recuperar llamando a [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con COLOR \_ BTNFACE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

