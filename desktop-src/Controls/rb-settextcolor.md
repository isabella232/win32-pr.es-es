---
title: RB_SETTEXTCOLOR mensaje (Commctrl.h)
description: Establece el color de texto predeterminado de un control rebar.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- RB_SETTEXTCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- RB_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68311572927f2e8dac623c697ac366d37d7ab5fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167262"
---
# <a name="rb_settextcolor-message"></a>Mensaje \_ SETTEXTCOLOR de RB

Establece el color de texto predeterminado de un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Valor COLORREF**](/windows/desktop/gdi/colorref) que representa el nuevo color de texto predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un [**valor COLORREF**](/windows/desktop/gdi/colorref) que representa el color de texto predeterminado anterior.

## <a name="remarks"></a>Observaciones

El color de texto predeterminado del control rebar se usa para dibujar el texto en un control rebar y todas las bandas que se agregan después de enviar este mensaje. El color de texto predeterminado de una banda determinada se puede invalidar cuando se agrega o modifica una banda estableciendo la marca COLORES DE RBBIM en fMask y estableciendo clrBack en la estructura \_ [**REBARBANDINFO.**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)  

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RB \_ GETTEXTCOLOR**](rb-gettextcolor.md)
</dt> </dl>

 

