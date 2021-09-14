---
title: TDM_SET_PROGRESS_BAR_RANGE mensaje (Commctrl.h)
description: Establece los valores mínimo y máximo de la barra de progreso en un cuadro de diálogo de tarea.
ms.assetid: ca8b48bc-cf56-4678-bb3d-7c730a96d98c
keywords:
- TDM_SET_PROGRESS_BAR_RANGE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_RANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17ebb6caa2c33282dccbb117980fc970cd45477
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166113"
---
# <a name="tdm_set_progress_bar_range-message"></a>Mensaje TDM \_ SET \_ PROGRESS BAR \_ \_ RANGE

Establece los valores mínimo y máximo de la barra de progreso en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el valor mínimo. De forma predeterminada, el valor mínimo es cero. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el valor máximo. De forma predeterminada, el valor máximo es 100.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve los valores mínimo y máximo anteriores, si se realiza correctamente, o cero en caso contrario. LOWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el valor mínimo y [**hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene el valor máximo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

