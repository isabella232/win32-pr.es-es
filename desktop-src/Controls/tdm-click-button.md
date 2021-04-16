---
title: Mensaje de TDM_CLICK_BUTTON (commctrl. h)
description: Simula la acción de un clic de botón en un cuadro de diálogo de tarea.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- TDM_CLICK_BUTTON controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658195"
---
# <a name="tdm_click_button-message"></a>Mensaje de botón de \_ clic de TDM \_

Simula la acción de un clic de botón en un cuadro de diálogo de tarea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Valor **int** que especifica el identificador del botón en el que se va a hacer clic.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

El identificador de botón especificado por *wParam* se envía a la función de devolución de llamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte del código de notificación en el que se [ \_ \_ hizo clic en un botón TDN](tdn-button-clicked.md) . Después de que la función de devolución de llamada se devuelva, el cuadro de diálogo de tarea se cierra si \_ se devolvió S OK desde la función de devolución de llamada. Si \_ se devolvió S false desde la función de devolución de llamada, el cuadro de diálogo de tarea permanece activo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

