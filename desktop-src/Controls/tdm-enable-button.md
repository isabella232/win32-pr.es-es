---
title: TDM_ENABLE_BUTTON mensaje (Commctrl.h)
description: Habilita o deshabilita un botón de inserción en un cuadro de diálogo de tarea.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- TDM_ENABLE_BUTTON controles de Windows mensaje
topic_type:
- apiref
api_name:
- TDM_ENABLE_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db10d616b4d07adcdc8c97495f7d12c89e603a7a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166146"
---
# <a name="tdm_enable_button-message"></a>Mensaje TDM \_ ENABLE \_ BUTTON

Habilita o deshabilita un botón de inserción en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Valor **int** que especifica el identificador del botón de inserción que se va a habilitar o deshabilitar.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Especifica el estado del botón. Establezca en 0 para deshabilitar el botón; se establece en distinto de cero para habilitar el botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





