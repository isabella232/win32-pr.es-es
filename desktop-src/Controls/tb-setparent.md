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
ms.openlocfilehash: f8137406c8e6854f86ed81d8d6b96293074ae67b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166574"
---
# <a name="tb_setparent-message"></a>Mensaje \_ SETPARENT de TB

Establece la ventana a la que el control de barra de herramientas envía mensajes de notificación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Controlar en la ventana para recibir mensajes de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador de la ventana de notificación anterior o **NULL** si no hay ninguna ventana de notificación anterior.

## <a name="remarks"></a>Observaciones

El **mensaje \_ SETPARENT de TB** no cambia la ventana primaria que se especificó cuando se creó el control. Al llamar [**a la función GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) para un control de barra de herramientas, se devolverá la ventana primaria real, no la ventana especificada en **TB \_ SETPARENT**. Para cambiar la ventana primaria del control, llame a la [**función SetParent.**](/windows/desktop/api/winuser/nf-winuser-setparent)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

