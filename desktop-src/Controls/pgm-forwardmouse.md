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
ms.openlocfilehash: 705b63ad39faea86e1f38a5b59dc73c6fc12f1e19fc17d0619c9a4b3dd5c6d26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046975"
---
# <a name="pgm_forwardmouse-message"></a>Mensaje \_ FORWARDMOUSE de PGM

Habilita o deshabilita el reenvío del mouse para el control de paginación. Cuando el reenvío del mouse está habilitado, el control de paginación reenvía [**los mensajes DE WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) a la ventana independiente. Puede enviar este mensaje explícitamente o usar la macro [**\_ ForwardMouse de Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)

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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

