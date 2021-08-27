---
title: TDM_SET_PROGRESS_BAR_MARQUEE mensaje (Commctrl.h)
description: Inicia y detiene la presentación de marquesina de la barra de progreso en un cuadro de diálogo de tarea y establece la velocidad de la marquesina.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- TDM_SET_PROGRESS_BAR_MARQUEE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b92816b70e683b9f58e0de2247b2710da38bee891caa39d9026fc342168c6be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060655"
---
# <a name="tdm_set_progress_bar_marquee-message"></a>Mensaje \_ \_ MARQUEE DE LA \_ BARRA DE \_ PROGRESO DE TDM SET

Inicia y detiene la presentación de marquesina de la barra de progreso en un cuadro de diálogo de tarea y establece la velocidad de la marquesina.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Un **BOOL** que indica si se debe activar o desactivar la presentación de marquesina. Use **TRUE** para activar la pantalla de marquesina o **FALSE** para desactivarla.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

UINT **que** especifica el tiempo, en milisegundos, entre las actualizaciones de animación de marquesina. Si este parámetro es cero, la animación de marquesina se actualiza cada 30 milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Comentarios

Para obtener información sobre el modo de marquesina, vea [Control de barra de progreso](progress-bar-control.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





