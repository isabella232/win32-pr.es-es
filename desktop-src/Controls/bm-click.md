---
title: BM_CLICK mensaje (Winuser.h)
description: Simula que el usuario hace clic en un botón. Este mensaje hace que el botón reciba los mensajes WM \_ LBUTTONDOWN y WM LBUTTONUP, y la ventana primaria del botón reciba un código de notificación CLICKED de \_ \_ BN.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- BM_CLICK controles de Windows mensaje
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968732"
---
# <a name="bm_click-message"></a>Mensaje \_ BM CLICK

Simula que el usuario hace clic en un botón. Este mensaje hace que el botón reciba los mensajes [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) y [**WM \_ LBUTTONUP,**](/windows/desktop/inputdev/wm-lbuttonup) y la ventana primaria del botón reciba un código de notificación [ \_ CLICKED de BN.](bn-clicked.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Si el botón está en un cuadro de diálogo y el cuadro de diálogo no está activo, el mensaje **BM \_ CLICK** podría producir un error. Para asegurarse de que esta situación se ha establecido correctamente, llame a la función [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) para activar el cuadro de diálogo antes de enviar el mensaje **BM \_ CLICK** al botón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

