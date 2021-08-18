---
title: TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE mensaje (Commctrl.h)
description: Especifica si un botón o vínculo de comando de un cuadro de diálogo de tarea determinado debe tener un icono de escudo de Control de cuentas de usuario (UAC); es decir, si la acción invocada por el botón requiere elevación.
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
ms.openlocfilehash: 2c69998da085a74b144179a0a4244c787cd3a871d63eca1e5df9c4e555b1a7e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104625"
---
# <a name="tdm_set_button_elevation_required_state-message"></a>Mensaje TDM \_ SET BUTTON ELEVATION REQUIRED \_ \_ \_ \_ STATE

Especifica si un botón o vínculo de comando de un cuadro de diálogo de tarea determinado debe tener un icono de escudo de Control de cuentas de usuario (UAC); es decir, si la acción invocada por el botón requiere elevación.

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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





