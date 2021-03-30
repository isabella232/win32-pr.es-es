---
title: Mensaje de BM_CLICK (Winuser. h)
description: Simula que el usuario hace clic en un botón. Este mensaje hace que el botón reciba los mensajes de WM \_ LBUTTONDOWN y WM \_ LBUTTONUP, y la ventana primaria del botón para recibir un código de notificación en el que se ha \_ haga clic en BN.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- BM_CLICK controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079078"
---
# <a name="bm_click-message"></a>Mensaje de clic de BM \_

Simula que el usuario hace clic en un botón. Este mensaje hace que el botón reciba los mensajes de [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) y [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) , y la ventana primaria del botón para recibir un código de notificación en el que se ha [ \_ haga clic en BN](bn-clicked.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el botón está en un cuadro de diálogo y el cuadro de diálogo no está activo, puede producirse un error en el mensaje de **\_ clic de BM** . Para asegurarse de que se ha realizado correctamente en esta situación, llame a la función [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) para activar el cuadro de diálogo antes de enviar el mensaje de **\_ clic de BM** al botón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

