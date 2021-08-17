---
title: WM_DWMCOMPOSITIONCHANGED mensaje (Winuser.h)
description: Informa a todas las ventanas de nivel superior Administrador de ventanas de escritorio (DWM) se ha habilitado o deshabilitado.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- WM_DWMCOMPOSITIONCHANGED mensaje Administrador de ventanas de escritorio
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973c69e114882041fc300ca6dee9c96efe121ee7bbf10875ed58ed3c269772c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118799"
---
# <a name="wm_dwmcompositionchanged-message"></a>Mensaje \_ DWMCOMPOSITIONCHANGED de WM

Informa a todas las ventanas de nivel superior Administrador de ventanas de escritorio (DWM) se ha habilitado o deshabilitado.

> [!Note]  
> A Windows 8, la composición de DWM siempre está habilitada, por lo que este mensaje no se envía independientemente de los cambios en el modo de vídeo.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

La [**función DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) se puede usar para determinar el estado de composición actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

