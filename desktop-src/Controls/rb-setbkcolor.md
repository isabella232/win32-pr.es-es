---
title: RB_SETBKCOLOR mensaje (Commctrl.h)
description: Establece el color de fondo predeterminado de un control rebar.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- RB_SETBKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a2fb502558b53603b59cf7f140248a72f1bf3e22366a85a6e8f740066775fb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696605"
---
# <a name="rb_setbkcolor-message"></a>Mensaje \_ SETBKCOLOR de RB

Establece el color de fondo predeterminado de un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Valor COLORREF**](/windows/desktop/gdi/colorref) que representa el nuevo color de fondo predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un [**valor COLORREF**](/windows/desktop/gdi/colorref) que representa el color de fondo predeterminado anterior.

## <a name="remarks"></a>Comentarios

El color de fondo predeterminado del control rebar se usa para dibujar el fondo en un control rebar y todas las bandas que se agregan después de enviar este mensaje. El color de fondo predeterminado de una banda determinada se puede invalidar cuando se agrega o modifica una banda estableciendo la marca COLORES DE RBBIM en fMask y estableciendo clrBack en la \_ [**estructura REBARBANDINFO.**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)  

Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RB \_ GETBKCOLOR**](rb-getbkcolor.md)
</dt> </dl>

 

