---
title: WM_DWMNCRENDERINGCHANGED mensaje (Winuser.h)
description: Se envía cuando ha cambiado la directiva de representación del área que no es de cliente.
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- WM_DWMNCRENDERINGCHANGED mensaje Administrador de ventanas de escritorio
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac32704ea240ccfc4d4de913b940e098ff8f4de4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072657"
---
# <a name="wm_dwmncrenderingchanged-message"></a>Mensaje \_ WM DWMNCRENDERINGCHANGED

Se envía cuando ha cambiado la directiva de representación del área que no es de cliente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si la representación de DWM está habilitada para el área no cliente de la ventana. **TRUE** si está habilitado; de lo contrario, **FALSE**.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

Las [**funciones DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) y [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) se usan para obtener o establecer la directiva de representación que no es de cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser.h</dt> </dl> |



 

