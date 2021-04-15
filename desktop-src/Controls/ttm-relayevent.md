---
title: Mensaje de TTM_RELAYEVENT (commctrl. h)
description: Pasa un mensaje del mouse a un control ToolTip para su procesamiento.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- TTM_RELAYEVENT controles de mensajes de Windows
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
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362249"
---
# <a name="ttm_relayevent-message"></a>TTM \_ RELAYEVENT

Pasa un mensaje del mouse a un control ToolTip para su procesamiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero. **Windows 7 y versiones posteriores:** Si la posición de la información sobre herramientas se desplaza desde la posición del cursor (para que no esté obstruida por un dedo o un dispositivo señalador), este parámetro puede contener información adicional tomada del mensaje de [**\_ MOUSEMOVE de WM**](/windows/desktop/inputdev/wm-mousemove) . Recupere esta información adicional con [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) que contiene el mensaje que se va a retransmitir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Un control ToolTip solo procesa los mensajes siguientes que le pasa el mensaje **\_ RELAYEVENT de TTM** :

-   LBUTTONDOWN de WM \_
-   LBUTTONUP de WM \_
-   MBUTTONDOWN de WM \_
-   MBUTTONUP de WM \_
-   MOUSEMOVE de WM \_
-   NCMOUSEMOVE de WM \_
-   RBUTTONDOWN de WM \_
-   RBUTTONUP de WM \_

El resto de los mensajes se omiten.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

