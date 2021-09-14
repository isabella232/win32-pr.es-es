---
title: PGM_FORWARDMOUSE mensaje (Commctrl.h)
description: Habilita o deshabilita el reenvío del mouse para el control de paginación. Cuando el reenvío del mouse está habilitado, el control de paginación reenvía los mensajes DE WM \_ MOUSEMOVE a la ventana independiente. Puede enviar este mensaje explícitamente o usar la \_ macro ForwardMouse de Pager.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- PGM_FORWARDMOUSE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167730"
---
# <a name="pgm_forwardmouse-message"></a>Mensaje \_ FORWARDMOUSE de PGM

Habilita o deshabilita el reenvío del mouse para el control de paginación. Cuando el reenvío del mouse está habilitado, el control de paginación reenvía los mensajes [**DE WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) a la ventana independiente. Puede enviar este mensaje explícitamente o usar la macro [**\_ ForwardMouse de Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Valor BOOL** que determina si el reenvío del mouse está habilitado o deshabilitado. Si este valor es distinto de cero, se habilita el reenvío del mouse. Si este valor es cero, el reenvío del mouse está deshabilitado.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

