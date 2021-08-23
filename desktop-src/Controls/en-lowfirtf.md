---
title: EN_LOWFIRTF de notificación (Richedit.h)
description: Notifica a la ventana primaria de un control Edición enriquecible de Microsoft que se ha recibido una palabra clave de formato de texto enriquecido (RTF) no admitida. Un control Rich Edit envía este código de notificación en forma de mensaje \_ WM NOTIFY.
ms.assetid: 3b18320b-ebc3-44f2-a93c-e967a028c522
keywords:
- EN_LOWFIRTF de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_LOWFIRTF
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffafccf7fc52506ce72c6591ae9d4b5e3f5ee8855788267fbfae98497165e4ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576325"
---
# <a name="en_lowfirtf-notification-code"></a>Código de notificación DE EN \_ LOWFIRTF

Notifica a la ventana primaria de un control Edición enriquecible de Microsoft que se ha recibido una palabra clave de formato de texto enriquecido (RTF) no admitida. Un control Rich Edit envía este código de notificación en forma de mensaje [**\_ WM NOTIFY.**](wm-notify.md)


```C++
EN_LOWFIRTF

    penLowfiRTF = (ENLOWFIRTF *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**ENLOWFIRTF.**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este código de notificación no devuelve un valor.

## <a name="remarks"></a>Comentarios

Para recibir una notificación EN LOWFIRTF, especifique la marca ENM LOWFIRTF en la máscara enviada con el \_ \_ mensaje EM [**\_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp1\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**ENLOWFIRTF**](/windows/desktop/api/Richedit/ns-richedit-enlowfirtf)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





