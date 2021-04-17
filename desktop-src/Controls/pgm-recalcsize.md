---
title: Mensaje de PGM_RECALCSIZE (commctrl. h)
description: Obliga al control de paginación a recalcular el tamaño de la ventana contenida. Al enviar este mensaje, se \_ enviará una notificación de CALCSIZE de PGN. Puede enviar este mensaje explícitamente o utilizar la macro RecalcSize de buscapersonas \_ .
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- PGM_RECALCSIZE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490204"
---
# <a name="pgm_recalcsize-message"></a>\_Mensaje RECALCSIZE PGM

Obliga al control de paginación a recalcular el tamaño de la ventana contenida. Al enviar este mensaje, se enviará una notificación de [ \_ CALCSIZE de PGN](pgn-calcsize.md) . Puede enviar este mensaje explícitamente o utilizar la macro [**\_ RecalcSize de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





