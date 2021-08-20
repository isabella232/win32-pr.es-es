---
title: RB_GETTOOLTIPS mensaje (Commctrl.h)
description: Recupera el identificador de cualquier control de información sobre herramientas asociado al control rebar.
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- RB_GETTOOLTIPS controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 859934dcdec85d0b160f9076f2a77263a02a187ebf49f8ccbb4af20fc3e82d13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540065"
---
# <a name="rb_gettooltips-message"></a>Mensaje \_ GETTOOLTIPS de RB

Recupera el identificador de cualquier control de información sobre herramientas asociado al control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HWND** que es el identificador del control de información sobre herramientas asociado al control rebar, o cero si no hay ningún control de información sobre herramientas asociado al control rebar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





