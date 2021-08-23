---
title: TB_SETPARENT mensaje (Commctrl.h)
description: Establece la ventana a la que el control de barra de herramientas envía mensajes de notificación.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- TB_SETPARENT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd97cdab230317feea65f2bffce74a7dec34ee336d69bb46ec4c6963ca9b3eff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078149"
---
# <a name="tb_setparent-message"></a>Mensaje \_ SETPARENT de TB

Establece la ventana a la que el control de barra de herramientas envía mensajes de notificación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador en la ventana para recibir mensajes de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador de la ventana de notificación anterior o **NULL** si no hay ninguna ventana de notificación anterior.

## <a name="remarks"></a>Comentarios

El **mensaje \_ SETPARENT de TB** no cambia la ventana primaria que se especificó cuando se creó el control. Llamar a [**la función GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) para un control de barra de herramientas devolverá la ventana primaria real, no la ventana especificada en **TB \_ SETPARENT**. Para cambiar la ventana primaria del control, llame a la [**función SetParent.**](/windows/desktop/api/winuser/nf-winuser-setparent)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

