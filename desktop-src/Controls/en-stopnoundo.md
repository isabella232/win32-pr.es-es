---
title: Código de notificación de EN_STOPNOUNDO (RichEdit. h)
description: Notifica a la ventana primaria de un control Rich Edit que se ha producido una acción para la que el control no puede asignar memoria suficiente para mantener el estado de deshacer. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- EN_STOPNOUNDO controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150908"
---
# <a name="en_stopnoundo-notification-code"></a>\_Código de notificación en STOPNOUNDO

Notifica a la ventana primaria de un control Rich Edit que se ha producido una acción para la que el control no puede asignar memoria suficiente para mantener el estado de deshacer. Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para continuar con la operación de **Deshacer** .

Devuelve un valor distinto de cero para detener la operación de **Deshacer** .

## <a name="remarks"></a>Observaciones

La ventana primaria siempre obtendrá un mensaje [**de \_ notificación de WM**](wm-notify.md) para este evento, pero no requiere que se envíe una máscara de notificación con [**em \_**](em-seteventmask.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[**\_notificaciones de WM**](wm-notify.md)
</dt> </dl>

 

 





