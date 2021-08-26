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
ms.openlocfilehash: 493c6813f15baa3ad3b5ceb7050049f620010a9eed12d75d09b3c9f102aa62db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876084"
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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





