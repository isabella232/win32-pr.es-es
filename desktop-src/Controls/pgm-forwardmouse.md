---
title: Mensaje de PGM_FORWARDMOUSE (commctrl. h)
description: Habilita o deshabilita el reenvío del mouse para el control de paginación. Cuando está habilitado el reenvío del mouse, el control de paginación reenvía \_ los mensajes de WM MOUSEMOVE a la ventana contenida. Puede enviar este mensaje explícitamente o utilizar la macro ForwardMouse de buscapersonas \_ .
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- PGM_FORWARDMOUSE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658261"
---
# <a name="pgm_forwardmouse-message"></a>\_Mensaje FORWARDMOUSE PGM

Habilita o deshabilita el reenvío del mouse para el control de paginación. Cuando está habilitado el reenvío del mouse, el control de paginación reenvía los mensajes de [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) a la ventana contenida. Puede enviar este mensaje explícitamente o utilizar la macro [**\_ ForwardMouse de buscapersonas**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **booleano** que determina si está habilitado o deshabilitado el reenvío del mouse. Si este valor es distinto de cero, se habilita el reenvío del mouse. Si este valor es cero, el reenvío del mouse está deshabilitado.

</dd> <dt>

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



 

