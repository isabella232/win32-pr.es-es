---
title: Código de notificación de EN_SAVECLIPBOARD (RichEdit. h)
description: Notifica a la ventana primaria del control Rich Edit que el control se está cerrando y el Portapapeles contiene información. Un control Rich Edit envía este código de notificación en forma de mensaje de \_ notificación de WM.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- EN_SAVECLIPBOARD controles de código de notificación de Windows
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
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905176"
---
# <a name="en_saveclipboard-notification-code"></a>\_Código de notificación en SAVECLIPBOARD

Notifica a la ventana primaria del control Rich Edit que el control se está cerrando y el Portapapeles contiene información. Un control Rich Edit envía este código de notificación en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) que contiene información sobre la información del portapapeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si el portapapeles debe ponerse a disposición de otras aplicaciones.

Devuelve un valor distinto de cero si no se debe guardar el portapapeles.

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

[**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





