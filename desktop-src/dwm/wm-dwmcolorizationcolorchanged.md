---
title: Mensaje de WM_DWMCOLORIZATIONCOLORCHANGED (Winuser. h)
description: Informa a todas las ventanas de nivel superior que el color de coloración ha cambiado.
ms.assetid: 6118d41b-f0b4-4034-aa98-d8757f18ca0d
keywords:
- WM_DWMCOLORIZATIONCOLORCHANGED Administrador de ventanas de escritorio de mensaje
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
ms.openlocfilehash: dc99d42fe2d4af77fa4534945a3396dda9c02b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150373"
---
# <a name="wm_dwmcolorizationcolorchanged-message"></a>Mensaje de DWMCOLORIZATIONCOLORCHANGED de WM \_

Informa a todas las ventanas de nivel superior que el color de coloración ha cambiado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el nuevo color de color. El formato de color es 0xAARRGGBB.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica si el nuevo color se mezcla con opacidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

[**DwmGetColorizationColor**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor) se utiliza para determinar el valor de color actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

