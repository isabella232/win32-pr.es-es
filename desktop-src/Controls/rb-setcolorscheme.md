---
title: RB_SETCOLORSCHEME mensaje (Commctrl.h)
description: Establece la información de combinación de colores para el control rebar.
ms.assetid: ddf8f3e4-66b7-4b53-a04e-b4dd372f71c4
keywords:
- RB_SETCOLORSCHEME controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_SETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce7715082a371c3632d8accb8fdf60bbac50d8d7d8182732d6a62c2dbb423c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169281"
---
# <a name="rb_setcolorscheme-message"></a>Mensaje \_ SETCOLORSCHEME de RB

Establece la información de combinación de colores para el control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura COLORSCHEME**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) que contiene la información de combinación de colores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="remarks"></a>Comentarios

El control rebar usa la información de combinación de colores al dibujar los elementos 3D en el control y las bandas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RB \_ GETCOLORSCHEME**](rb-getcolorscheme.md)
</dt> </dl>

 

 





