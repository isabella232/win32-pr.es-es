---
title: Mensaje de TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE (commctrl. h)
description: Especifica si un botón de cuadro de diálogo de tarea o vínculo de comando determinado debe tener un icono de escudo de control de cuentas de usuario (UAC). es decir, si la acción invocada por el botón requiere elevación.
ms.assetid: c4321fdb-3ea9-49bf-b53d-eb73d5b11084
keywords:
- TDM_SET_BUTTON_ELEVATION_REQUIRED_STATE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151050"
---
# <a name="tdm_set_button_elevation_required_state-message"></a>\_Mensaje de \_ \_ Estado de elevación \_ requerida del botón \_ de configuración de TDM

Especifica si un botón de cuadro de diálogo de tarea o vínculo de comando determinado debe tener un icono de escudo de control de cuentas de usuario (UAC). es decir, si la acción invocada por el botón requiere elevación.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

IDENTIFICADOR del botón de comando o vínculo de comando que se va a actualizar.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Establézcalo en 0 para indicar que la acción invocada por el botón no requiere elevación. Se establece en un valor distinto de cero para indicar que la acción requiere elevación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





