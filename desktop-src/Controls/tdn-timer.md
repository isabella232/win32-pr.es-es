---
title: TDN_TIMER de notificación (Commctrl.h)
description: Enviado por un cuadro de diálogo de tarea aproximadamente cada 200 milisegundos.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER código de notificación Windows controles
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166061"
---
# <a name="tdn_timer-notification-code"></a>Código de notificación del temporizador de TDN \_

Enviado por un cuadro de diálogo de tarea aproximadamente cada 200 milisegundos. Este código de notificación se envía cuando se ha establecido la marca TDF CALLBACK TIMER en el miembro dwFlags de la estructura TASKDIALOGCONFIG que se pasó a la \_ \_ función [**TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)  [](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el **método TaskDialogIndirect.**


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

DWORD **que** especifica el número de milisegundos desde que se creó el cuadro de diálogo o este código de notificación **devolvió S \_ FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Para restablecer el recuento de tics, la aplicación debe devolver **S \_ FALSE;** de lo contrario, el recuento seguirá incrementando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





