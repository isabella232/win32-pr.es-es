---
title: TTM_GETMAXTIPWIDTH mensaje (Commctrl.h)
description: Recupera el ancho máximo de una ventana de información sobre herramientas.
ms.assetid: 0f0a5403-fe2e-4e5a-96c2-a435827a5fd7
keywords:
- TTM_GETMAXTIPWIDTH controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_GETMAXTIPWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bce561b254645932b214b48879aa0be04deb31b32e8dc591fc3183ec39871273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751055"
---
# <a name="ttm_getmaxtipwidth-message"></a>Mensaje \_ GETMAXTIPWIDTH de TTM

Recupera el ancho máximo de una ventana de información sobre herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor INT** que representa el ancho máximo de la información sobre herramientas, en píxeles. Si no se estableció anteriormente ningún ancho máximo, el mensaje devuelve -1.

## <a name="remarks"></a>Comentarios

El valor de ancho máximo de la información sobre herramientas no indica el ancho real de una ventana de información sobre herramientas. En su lugar, si una cadena de información sobre herramientas supera el ancho máximo, el control divide el texto en varias líneas, usando espacios para determinar los saltos de línea. Si el texto no se puede segmentar en varias líneas, se mostrará en una sola línea. La longitud de esta línea puede superar el ancho máximo de la información sobre herramientas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TTM \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





