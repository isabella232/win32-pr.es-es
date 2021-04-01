---
title: Mensaje de TDM_CLICK_RADIO_BUTTON (commctrl. h)
description: Simula la acción de un clic de botón de radio en un cuadro de diálogo de tarea.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- TDM_CLICK_RADIO_BUTTON controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997023"
---
# <a name="tdm_click_radio_button-message"></a>\_Mensaje de \_ botón de radio haga clic en TDM \_

Simula la acción de un clic de botón de radio en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Valor **int** que especifica el identificador del botón de radio en el que se va a hacer clic.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

El identificador de botón de radio especificado se envía a la función de devolución de llamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte del código de notificación de un [clic del \_ \_ botón \_ de radio TDN](tdn-radio-button-clicked.md) . Después de que la función de devolución de llamada vuelva, se seleccionará el botón de radio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

