---
title: Código de notificación de TDN_TIMER (commctrl. h)
description: Enviado por un cuadro de diálogo de tarea aproximadamente cada 200 milisegundos.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658383"
---
# <a name="tdn_timer-notification-code"></a>\_Código de notificación del temporizador de TDN

Enviado por un cuadro de diálogo de tarea aproximadamente cada 200 milisegundos. Este código de notificación se envía cuando se ha \_ establecido la marca de temporizador de devolución de llamada TDF \_ en el miembro **dwFlags** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que se pasó a la función [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método **TaskDialogIndirect** .


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**DWORD** que especifica el número de milisegundos transcurridos desde que se creó el cuadro de diálogo o el código de notificación devolvió **S \_ false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para restablecer el TickCount, la aplicación debe devolver **S \_ false**; de lo contrario, el TickCount seguirá aumentando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





