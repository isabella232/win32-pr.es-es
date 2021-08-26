---
title: TDM_CLICK_VERIFICATION mensaje (Commctrl.h)
description: Simula un clic en la casilla de verificación de un cuadro de diálogo de tarea, si existe.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- TDM_CLICK_VERIFICATION controles de Windows mensaje
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3cda5e85b138225d69e159792cbe641122e91bf9602b3e0f5edafa419edc3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876095"
---
# <a name="tdm_click_verification-message"></a>Mensaje DE \_ COMPROBACIÓN DE CLIC DE TDM \_

Simula un clic en la casilla de verificación de un cuadro de diálogo de tarea, si existe.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

**TRUE** para establecer el estado de la casilla que se va a activar; **FALSE** para establecer que se desactive.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

**TRUE** para establecer el foco del teclado en la casilla; **FALSE en** caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





