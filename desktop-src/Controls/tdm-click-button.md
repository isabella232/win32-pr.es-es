---
title: TDM_CLICK_BUTTON mensaje (Commctrl.h)
description: Simula la acción de un clic de botón en un cuadro de diálogo de tarea.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- TDM_CLICK_BUTTON controles de Windows mensaje
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7758385699a0d280f808a21db4c56487c466c716b3ae0236f77130847cea3aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876175"
---
# <a name="tdm_click_button-message"></a>Mensaje DEL BOTÓN CLIC DE TDM \_ \_

Simula la acción de un clic de botón en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Un **valor int** que especifica el identificador del botón en el que se va a hacer clic.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Comentarios

El identificador de botón especificado por *wParam* se envía a la función de devolución de llamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte de un código [de notificación \_ \_ CLICKED de TDN BUTTON.](tdn-button-clicked.md) Una vez devuelta la función de devolución de llamada, el cuadro de diálogo de tarea se cierra si S \_ OK se devolvió desde la función de devolución de llamada. Si S \_ FALSE se devolvió desde la función de devolución de llamada, el cuadro de diálogo de tarea permanece activo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

