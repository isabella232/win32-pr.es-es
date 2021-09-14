---
title: TDN_BUTTON_CLICKED de notificación (Commctrl.h)
description: Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón o un vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método TaskDialogIndirect.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- TDN_BUTTON_CLICKED código de notificación Windows controles
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166098"
---
# <a name="tdn_button_clicked-notification-code"></a>Código de notificación \_ CLICKED DEL \_ BOTÓN TDN

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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





