---
title: WM_DWMWINDOWMAXIMIZEDCHANGE mensaje (Winuser.h)
description: Se envía cuando se maximiza Administrador de ventanas de escritorio ventana compuesta de Administrador de ventanas de escritorio (DWM).
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- WM_DWMWINDOWMAXIMIZEDCHANGE mensaje Administrador de ventanas de escritorio
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93cfa4ac380b6ff439fb2bf4805846c0b774a90bcfdcd83673ead2334a3c7094
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117755"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a>Mensaje \_ DWMWINDOWMAXIMIZEDCHANGE de WM

Se envía cuando se maximiza Administrador de ventanas de escritorio ventana compuesta de Administrador de ventanas de escritorio (DWM).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Establezca en true para especificar que la ventana se ha maximizado.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

