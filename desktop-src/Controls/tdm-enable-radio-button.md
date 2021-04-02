---
title: Mensaje de TDM_ENABLE_RADIO_BUTTON (commctrl. h)
description: Habilita o deshabilita un botón de radio en un cuadro de diálogo de tarea.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- TDM_ENABLE_RADIO_BUTTON controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_ENABLE_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a78445158c5edc920eb329cdfc52d44f9cb7d6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997022"
---
# <a name="tdm_enable_radio_button-message"></a>\_Mensaje de \_ botón de radio habilitar TDM \_

Habilita o deshabilita un botón de radio en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Valor **int** que especifica el identificador del botón de radio que se va a habilitar o deshabilitar.

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



 

 





