---
title: Mensaje de TB_SETPARENT (commctrl. h)
description: Establece la ventana en la que el control de barra de herramientas envía mensajes de notificación.
ms.assetid: 4863bd9f-021b-4295-9483-459fc19325d9
keywords:
- TB_SETPARENT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905555"
---
# <a name="tb_setparent-message"></a>\_Message TB SETPARENT

Establece la ventana en la que el control de barra de herramientas envía mensajes de notificación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana para recibir mensajes de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es un identificador de la ventana de notificación anterior, o **null** si no hay ninguna ventana de notificación anterior.

## <a name="remarks"></a>Observaciones

El mensaje del objeto **\_ SETPARENT de TB** no cambia la ventana primaria que se especificó cuando se creó el control. La llamada a la función [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) para un control de barra de herramientas devolverá la ventana primaria real, no la ventana especificada en **TB \_ SETPARENT**. Para cambiar la ventana primaria del control, llame a la función [**SetParent**](/windows/desktop/api/winuser/nf-winuser-setparent) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

