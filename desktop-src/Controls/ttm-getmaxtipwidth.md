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
ms.openlocfilehash: f89c56692db9d451eb18db61af262cc0f3a715f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165917"
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

## <a name="remarks"></a>Observaciones

El valor de ancho máximo de información sobre herramientas no indica el ancho real de una ventana de información sobre herramientas. En su lugar, si una cadena de información sobre herramientas supera el ancho máximo, el control divide el texto en varias líneas, usando espacios para determinar los saltos de línea. Si el texto no se puede segmentar en varias líneas, se mostrará en una sola línea. La longitud de esta línea puede superar el ancho máximo de información sobre herramientas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETMAXTIPWIDTH de TTM**](ttm-setmaxtipwidth.md)
</dt> </dl>

 

 





