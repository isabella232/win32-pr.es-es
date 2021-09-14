---
title: EN_PROTECTED de notificación (Richedit.h)
description: Notifica a la ventana primaria de un control de edición enriquecido que el usuario está haciendo una acción que cambiaría un intervalo protegido de texto. Un control de edición enriquecido envía este código de notificación en forma de mensaje WM \_ NOTIFY.
ms.assetid: 29c0cb51-675c-44b1-ad45-5f7140ca5675
keywords:
- EN_PROTECTED código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_PROTECTED
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1475053366a06f46b0c99514ade961f1a2998b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062032"
---
# <a name="en_protected-notification-code"></a>Código de notificación DE EN \_ PROTECTED

Notifica a la ventana primaria de un control de edición enriquecido que el usuario está haciendo una acción que cambiaría un intervalo protegido de texto. Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
EN_PROTECTED

    penProtected = (ENPROTECTED *) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Estructura [**ENPROTECTED que**](/windows/desktop/api/Richedit/ns-richedit-enprotected) contiene información sobre el mensaje que desencadenó el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir la operación.

Devuelve un valor distinto de cero para evitar la operación.

## <a name="remarks"></a>Observaciones

Si se devuelve cero y se cambian los miembros **msg**, **wParam** y **lParam** de la estructura [**ENPROTECTED,**](/windows/desktop/api/Richedit/ns-richedit-enprotected) el control procesa el mensaje revisado en lugar del mensaje original.

Para recibir códigos de notificación EN \_ PROTECTED, especifique [**ENM \_ PROTECTED en**](rich-edit-control-event-mask-flags.md) la máscara enviada con el [**mensaje EM \_ SETEVENTMASK.**](em-seteventmask.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**PROTEGIDO**](/windows/desktop/api/Richedit/ns-richedit-enprotected)
</dt> <dt>

[**WM \_ NOTIFY**](wm-notify.md)
</dt> </dl>

 

 





