---
title: TTM_SETMAXTIPWIDTH mensaje (Commctrl.h)
description: Establece el ancho máximo de una ventana de información sobre herramientas.
ms.assetid: 3cfb6011-d0c3-4a57-aead-d4ec09a057cc
keywords:
- TTM_SETMAXTIPWIDTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_SETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d344a3abcbe2b3bf57a71c8020d383f76ab1922b9009cd69411912d4468fa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433765"
---
# <a name="ttm_setmaxtipwidth-message"></a>Mensaje \_ SETMAXTIPWIDTH de TTM

Establece el ancho máximo de una ventana de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Ancho máximo de la ventana de información sobre herramientas o -1 para permitir cualquier ancho.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el ancho de información sobre herramientas máximo anterior.

## <a name="remarks"></a>Observaciones

El valor de ancho máximo no indica el ancho real de una ventana de información sobre herramientas. En su lugar, si una cadena de información sobre herramientas supera el ancho máximo, el control divide el texto en varias líneas, usando espacios para determinar los saltos de línea. Si el texto no se puede segmentar en varias líneas, se muestra en una sola línea, lo que puede superar el ancho máximo de la información sobre herramientas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TTM \_ GETMAXTIPWIDTH**](ttm-getmaxtipwidth.md)
</dt> </dl>

 

 





