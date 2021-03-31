---
title: Mensaje de TDM_CLICK_VERIFICATION (commctrl. h)
description: Simula un clic en la casilla de verificación de un cuadro de diálogo de tarea, si existe.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- TDM_CLICK_VERIFICATION controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149879"
---
# <a name="tdm_click_verification-message"></a>TDM- \_ hacer clic en \_ mensaje de comprobación

Simula un clic en la casilla de verificación de un cuadro de diálogo de tarea, si existe.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

**True** para establecer el estado de la casilla que se va a comprobar; **False** para establecer que esté desactivada.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

**True** para establecer el foco de teclado en la casilla; De lo contrario, **false** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





