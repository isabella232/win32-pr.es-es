---
title: Mensaje de RB_SETTEXTCOLOR (commctrl. h)
description: Establece el color de texto predeterminado del control rebar.
ms.assetid: 85f120bd-39aa-43f8-a794-3bb4f3fe1cd4
keywords:
- RB_SETTEXTCOLOR controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491752"
---
# <a name="rb_settextcolor-message"></a>Mensaje de SETTEXTCOLOR de RB \_

Establece el color de texto predeterminado del control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el nuevo color de texto predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el color de texto predeterminado anterior.

## <a name="remarks"></a>Observaciones

El color de texto predeterminado del control rebar se usa para dibujar el texto en un control rebar y se han enviado todas las bandas que se agregan después de este mensaje. El color de texto predeterminado para una banda determinada se puede invalidar Cuando se agrega o se modifica una banda mediante la configuración de la \_ marca de colores RBBIM en **fMask** y el establecimiento de **ClrBack** en la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETTEXTCOLOR RB**](rb-gettextcolor.md)
</dt> </dl>

 

