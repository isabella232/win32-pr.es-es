---
title: Código de notificación de TDN_BUTTON_CLICKED (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón o vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- TDN_BUTTON_CLICKED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997106"
---
# <a name="tdn_button_clicked-notification-code"></a>\_Código de notificación de clic del botón TDN \_

Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón o vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Un valor **int** que especifica el identificador del botón o vínculo de la selección que se ha seleccionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para evitar que se cierre el cuadro de diálogo de tarea, la aplicación debe devolver **S \_ false**; de lo contrario, se cerrará el cuadro de diálogo de tarea y se devolverá el identificador de botón a través de la llamada de aplicación original.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





