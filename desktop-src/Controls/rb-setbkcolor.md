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
ms.openlocfilehash: fa9365de2d790b1f28b1330c038b69d30b208143
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167285"
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

## <a name="remarks"></a>Observaciones

El color de fondo predeterminado del control rebar se usa para dibujar el fondo en un control rebar y todas las bandas que se agregan después de enviar este mensaje. El color de fondo predeterminado de una banda determinada se puede invalidar cuando se agrega o modifica una banda estableciendo la marca COLORES DE RBBIM en fMask y estableciendo clrBack en la \_ [**estructura REBARBANDINFO.**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)  

Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RB \_ GETBKCOLOR**](rb-getbkcolor.md)
</dt> </dl>

 

