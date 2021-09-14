---
title: TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE mensaje (Commctrl.h)
description: Especifica si un botón de diálogo de tarea determinado o un vínculo de comando debe tener un icono de escudo de Control de cuentas de usuario (UAC); es decir, si la acción invocada por el botón requiere elevación.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef5f8479e88a3b63cbd5fab6a5686913864fd9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166134"
---
# <a name="tdm_set_button_elevation_required_state-message"></a>TDM \_ SET BUTTON ELEVATION REQUIRED STATE \_ \_ \_ \_ message

Especifica si un botón de diálogo de tarea determinado o un vínculo de comando debe tener un icono de escudo de Control de cuentas de usuario (UAC); es decir, si la acción invocada por el botón requiere elevación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Identificador del botón de inserción o del vínculo de comando que se va a actualizar.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Establezca en 0 para designar que la acción invocada por el botón no requiere elevación. Establezca en distinto de cero para designar que la acción requiere elevación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





