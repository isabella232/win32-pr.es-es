---
title: Mensaje de PGM_SETBKCOLOR (commctrl. h)
description: Establece el color de fondo actual para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro SetBkColor de buscapersonas \_ .
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- PGM_SETBKCOLOR controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150193"
---
# <a name="pgm_setbkcolor-message"></a>\_Mensaje SETBKCOLOR PGM

Establece el color de fondo actual para el control de paginación. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ SetBkColor de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor de **COLORREF** que contiene el nuevo color de fondo del control de paginación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de **COLORREF** que contiene el color de fondo anterior.

## <a name="remarks"></a>Observaciones

De forma predeterminada, el control de paginación usará el color de la superficie del botón del sistema como color de fondo. Este es el mismo color que se puede recuperar llamando a [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) con el color \_ BTNFACE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

