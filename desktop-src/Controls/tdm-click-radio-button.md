---
title: TDM_CLICK_RADIO_BUTTON mensaje (Commctrl.h)
description: Simula la acción de hacer clic en un botón de radio en un cuadro de diálogo de tarea.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- TDM_CLICK_RADIO_BUTTON controles de Windows mensaje
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76d465b1b937359a3d312a401914d497f9c9b22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166158"
---
# <a name="tdm_click_radio_button-message"></a>Mensaje TDM \_ CLICK \_ RADIO \_ BUTTON

Simula la acción de hacer clic en un botón de radio en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Valor **int** que especifica el identificador del botón de radio en el que se va a hacer clic.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

El identificador de botón de radio especificado se envía a la función de devolución de llamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte de un código de notificación [ \_ \_ \_ CLICKED de TDN RADIO BUTTON.](tdn-radio-button-clicked.md) Una vez que se devuelva la función de devolución de llamada, se seleccionará el botón de radio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

