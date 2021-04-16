---
description: Notifica a la ventana cuando el panel de entrada de texto se está abriendo.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: Mensaje de MICROSOFT_TIP_OPENING_MSG (Peninputpanel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718991"
---
# <a name="microsoft_tip_opening_msg-message"></a>\_Mensaje de \_ mensajes de apertura de propinas de Microsoft \_

Notifica a la ventana cuando el panel de entrada de texto se está abriendo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Actualmente no se usa, debe ser **null**.

</dd> <dt>

*lParam* 
</dt> <dd>

Actualmente no se usa, debe ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Las aplicaciones deben llamar a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) después de controlar este mensaje. Vea **DefWindowProc** para obtener información sobre los valores devueltos.

## <a name="remarks"></a>Observaciones

Esta notificación le permite saber cuándo se abre el panel de entrada. Si desea realizar una acción cuando esto sucede, controle el mensaje, realice la operación en el controlador y, a continuación, pase el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

> [!Note]  
> Este mensaje también se envía cuando el panel de entrada de texto ya está visible y el usuario cambia del teclado a la máscara de escritura a mano.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Remoto<br/> | Windows Vista<br/>                                                                   |
| Encabezado<br/> | <dl> <dt>Peninputpanel. h</dt> </dl> |



 

