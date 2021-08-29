---
title: TDN_BUTTON_CLICKED de notificación (Commctrl.h)
description: Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón o un vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- TDN_BUTTON_CLICKED de notificación Windows controles
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
ms.openlocfilehash: 9d8491117e7bed636edc7fe1e1075b5c61489735ed7b46d649520d4173a8c536
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875825"
---
# <a name="tdn_button_clicked-notification-code"></a>Código de notificación \_ CLICKED del botón \_ TDN

Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón o un vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Un **valor int** que especifica el identificador del botón o vínculo de comand seleccionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para evitar que el cuadro de diálogo de tarea se cierre, la aplicación debe devolver **S \_ FALSE;** de lo contrario, el cuadro de diálogo de tarea se cierra y el identificador del botón se devuelve a través de la llamada de aplicación original.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





