---
title: EN_CORRECTTEXT de notificación (Richedit.h)
description: Notifica a una ventana primaria del control de edición enriquecido que se ha producido un gesto CORRECTO de SYV, lo que da a la ventana primaria la oportunidad de cancelar \_ la corrección del texto. Un control de edición enriquecido envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- EN_CORRECTTEXT de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f03bf0d1bd31cc1f4139c24c6b0efa904f013231af4e108b0f97ef7f308bbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019423"
---
# <a name="en_correcttext-notification-code"></a>Código de notificación EN \_ CORRECTTEXT

Notifica a una ventana primaria del control de edición enriquecido que se ha producido un gesto CORRECTO de SYV, lo que da a la ventana primaria la oportunidad de cancelar \_ la corrección del texto. Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) que especifica la selección que se va a corregir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para omitir la acción.

Devuelve un valor distinto de cero para procesar la acción.

## <a name="remarks"></a>Comentarios

Este código de notificación solo se envía si hay funcionalidades de lápiz disponibles.

Para recibir códigos de notificación EN \_ CORRECTTEXT, especifique [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el [**mensaje EM \_ SETEVENTMASK.**](em-seteventmask.md)

> [!Note]  
> El código de notificación EN \_ CORRECTTEXT solo se admite en la edición enriquección versión 1.0. No se admite en versiones posteriores de edición enriquección. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

 

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

[**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





