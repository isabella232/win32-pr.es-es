---
title: WM_DWMCOLORIZATIONCOLORCHANGED mensaje (Winuser.h)
description: Informa a todas las ventanas de nivel superior de que el color de color ha cambiado.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- WM_DWMCOLORIZATIONCOLORCHANGED mensaje Administrador de ventanas de escritorio
topic_type:
- apiref
api_name:
- WM_DWMCOLORIZATIONCOLORCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdbb854821f2a25565241700d28964b2d32319bccb8226c3d7d789c0e457fff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094595"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a>Mensaje \_ DWMCOLORIZATIONCOLORCHANGED de WM

Informa a todas las ventanas de nivel superior de que el color de color ha cambiado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el nuevo color de coloración. El formato de color es 0xAARRGGBB.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica si el nuevo color se combina con opacidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) se usa para determinar el valor de color actual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

