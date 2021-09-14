---
title: TDM_ENABLE_RADIO_BUTTON mensaje (Commctrl.h)
description: Habilita o deshabilita un botón de radio en un cuadro de diálogo de tarea.
ms.assetid: da605ce0-b2d5-481a-a0e1-628ae5b65726
keywords:
- TDM_ENABLE_RADIO_BUTTON controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166145"
---
# <a name="tdm_enable_radio_button-message"></a>Mensaje DEL BOTÓN \_ DE RADIO HABILITAR \_ \_ TDM

Habilita o deshabilita un botón de radio en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Valor **int** que especifica el identificador del botón de radio que se va a habilitar o deshabilitar.

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



 

 





