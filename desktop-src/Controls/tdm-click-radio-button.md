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
ms.openlocfilehash: 80c1eb7e72030a3c2dadc61bfd90027dab032c3342a25c72e4da9dd9a7338142
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104665"
---
# <a name="tdm_click_radio_button-message"></a>TDM \_ HAGA CLIC EN EL MENSAJE DEL BOTÓN DE \_ \_ RADIO

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

## <a name="remarks"></a>Comentarios

El identificador de botón de radio especificado se envía a la función de devolución de llamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte de un código de notificación CLICKED de [ \_ TDN RADIO \_ BUTTON. \_](tdn-radio-button-clicked.md) Una vez que se devuelva la función de devolución de llamada, se seleccionará el botón de radio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

