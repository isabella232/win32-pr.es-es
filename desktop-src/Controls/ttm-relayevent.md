---
title: TTM_RELAYEVENT mensaje (Commctrl.h)
description: Pasa un mensaje del mouse a un control de información sobre herramientas para su procesamiento.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- TTM_RELAYEVENT controles de Windows mensaje
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165877"
---
# <a name="ttm_relayevent-message"></a>Mensaje \_ RELAYEVENT de TTM

Pasa un mensaje del mouse a un control de información sobre herramientas para su procesamiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero. **Windows 7 y versiones posteriores:** Si la posición de la información sobre herramientas se desplaza desde la posición del cursor (con el fin de que un dedo o un dispositivo que señala no se obstruya), este parámetro puede contener información adicional tomada del mensaje [**\_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) de WM. Recupere esta información adicional [**con GetMessageExtraInfo.**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo)

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura MSG**](/windows/win32/api/winuser/ns-winuser-msg) que contiene el mensaje que se retransmite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Un control de información sobre herramientas procesa solo los siguientes mensajes pasados por el **mensaje \_ RELAYEVENT de TTM:**

-   WM \_ LBUTTONDOWN
-   WM \_ LBUTTONUP
-   WM \_ MBUTTONDOWN
-   WM \_ MBUTTONUP
-   WM \_ MOUSEMOVE
-   WM \_ NCMOUSEMOVE
-   WM \_ RBUTTONDOWN
-   WM \_ RBUTTONUP

Todos los demás mensajes se omiten.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

