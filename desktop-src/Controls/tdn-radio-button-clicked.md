---
title: TDN_RADIO_BUTTON_CLICKED de notificación (Commctrl.h)
description: Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón de radio o un vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: d9a29874-6755-4754-bcaf-94746b218b47
keywords:
- TDN_RADIO_BUTTON_CLICKED código de notificación Windows controles
topic_type:
- apiref
api_name:
- TDN_RADIO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea1917a1523cdc3a106398d07912d3fff5295f7da18a59055f059a13007f98b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875765"
---
# <a name="tdn_radio_button_clicked-notification-code"></a>Código de notificación CLIC EN \_ EL BOTÓN DE RADIO \_ \_ de TDN

Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón de radio o un vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)


```C++
TDN_RADIO_BUTTON_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Un **valor int** que especifica el identificador correspondiente al botón de radio en el que se hizo clic.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





