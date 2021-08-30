---
title: EN_SAVECLIPBOARD de notificación (Richedit.h)
description: Notifica a la ventana primaria del control de edición enriquecido que el control se está cerrando y que el Portapapeles contiene información. Un control de edición enriquecido envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- EN_SAVECLIPBOARD código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33337dffee30deb70833d9ac9e0e3a28b58c4e607de1211c4c8a21a805fb013b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047595"
---
# <a name="en_saveclipboard-notification-code"></a>Código de notificación DE EN \_ SAVECLIPBOARD

Notifica a la ventana primaria del control de edición enriquecido que el control se está cerrando y que el Portapapeles contiene información. Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**ENSAVECLIPBOARD que**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) contiene información sobre la información del Portapapeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si el Portapapeles debe estar disponible para otras aplicaciones.

Devuelve un valor distinto de cero si no se debe guardar el Portapapeles.

## <a name="remarks"></a>Comentarios

La ventana primaria siempre recibirá un mensaje [**WM \_ NOTIFY**](wm-notify.md) para este evento, no requiere una máscara de notificación enviada con [**EM \_ SETEVENTMASK**](em-seteventmask.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





