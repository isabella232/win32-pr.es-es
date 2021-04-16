---
title: Mensaje de TDM_ENABLE_BUTTON (commctrl. h)
description: Habilita o deshabilita un botón de reenvío en un cuadro de diálogo de tarea.
ms.assetid: 133fe4ac-4e2d-4826-8510-c0d9f88b5b37
keywords:
- TDM_ENABLE_BUTTON controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658369"
---
# <a name="tdm_enable_button-message"></a>\_Mensaje de \_ botón Habilitar TDM

Habilita o deshabilita un botón de reenvío en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Valor **int** que especifica el identificador del botón de la tecla que se va a habilitar o deshabilitar.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Especifica el estado del botón. Establézcalo en 0 para deshabilitar el botón; se establece en un valor distinto de cero para habilitar el botón.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





