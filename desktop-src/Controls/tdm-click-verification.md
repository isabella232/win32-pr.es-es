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
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166149"
---
# <a name="tdm_click_verification-message"></a>Mensaje TDM \_ CLICK \_ VERIFICATION

Simula un clic en la casilla de verificación de un cuadro de diálogo de tarea, si existe.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

**TRUE** para establecer el estado de la casilla que se va a activar; **FALSE** para que se desactive.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

**TRUE** para establecer el foco del teclado en la casilla; **False en** caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





