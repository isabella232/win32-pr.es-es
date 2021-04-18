---
title: Mensaje de RB_SETBKCOLOR (commctrl. h)
description: Establece el color de fondo predeterminado del control rebar.
ms.assetid: 450a1e16-24f6-4f86-8e46-14009da05efc
keywords:
- RB_SETBKCOLOR controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658227"
---
# <a name="rb_setbkcolor-message"></a>Mensaje de SETBKCOLOR de RB \_

Establece el color de fondo predeterminado del control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el nuevo color de fondo predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el color de fondo predeterminado anterior.

## <a name="remarks"></a>Observaciones

El color de fondo predeterminado del control rebar se usa para dibujar el fondo en un control rebar y se han enviado todas las bandas que se agregan después de este mensaje. El color de fondo predeterminado para una banda determinada se puede invalidar Cuando se agrega o se modifica una banda mediante la configuración de la \_ marca de colores RBBIM en **fMask** y el establecimiento de **ClrBack** en la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .

Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETBKCOLOR RB**](rb-getbkcolor.md)
</dt> </dl>

 

