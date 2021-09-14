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
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166165"
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

## <a name="remarks"></a>Observaciones

El identificador de botón especificado por *wParam* se envía a la función de devolución de llamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte de un código [de notificación \_ \_ CLICKED de TDN BUTTON.](tdn-button-clicked.md) Una vez devuelta la función de devolución de llamada, el cuadro de diálogo de tarea se cierra si S \_ OK se devolvió desde la función de devolución de llamada. Si S \_ FALSE se devolvió desde la función de devolución de llamada, el cuadro de diálogo de tarea permanece activo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

