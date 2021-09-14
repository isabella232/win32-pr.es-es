---
title: WM_DWMCOMPOSITIONCHANGED mensaje (Winuser.h)
description: Informa a todas las ventanas de nivel superior de que Administrador de ventanas de escritorio (DWM) se ha habilitado o deshabilitado.
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
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072658"
---
# <a name="wm_dwmcompositionchanged-message"></a>Mensaje \_ DWMCOMPOSITIONCHANGED de WM

Informa a todas las ventanas de nivel superior de que Administrador de ventanas de escritorio (DWM) se ha habilitado o deshabilitado.

> [!Note]  
> A Windows 8, la composición de DWM siempre está habilitada, por lo que este mensaje no se envía independientemente de los cambios en el modo de vídeo.

 

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

La [**función DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) se puede usar para determinar el estado de composición actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

