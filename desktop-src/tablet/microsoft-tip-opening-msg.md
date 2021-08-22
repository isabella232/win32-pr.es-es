---
description: Notifica a la ventana cuando se abre el Panel de entrada de texto.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: MICROSOFT_TIP_OPENING_MSG mensaje (Peninputpanel.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e183cc426cd5d73e52c6aaef007bc5579ceb3eb0f4ceaf3f9f4084677b7a556
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335905"
---
# <a name="microsoft_tip_opening_msg-message"></a>MICROSOFT \_ TIP OPENING MSG message (MENSAJE DE APERTURA DE \_ \_ SUGERENCIAS DE MICROSOFT)

Notifica a la ventana cuando se abre el Panel de entrada de texto.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Actualmente no se usa, debe ser **NULL.**

</dd> <dt>

*lParam* 
</dt> <dd>

Actualmente no se usa, debe ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Las aplicaciones deben llamar [**a DefWindowProc después**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) de controlar este mensaje. Vea **DefWindowProc para** obtener información sobre sus valores devueltos.

## <a name="remarks"></a>Comentarios

Esta notificación le permite saber cuándo se abre el panel de entrada. Si desea realizar una acción cuando esto sucede, controle el mensaje, realice la operación en el controlador y, a continuación, pase el mensaje [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

> [!Note]  
> Este mensaje también se envía cuando el panel de entrada de texto ya está visible y el usuario cambia del teclado a la máscara de escritura a mano.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|--------------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista<br/>                                                                   |
| Header<br/> | <dl> <dt>Peninputpanel.h</dt> </dl> |



 

