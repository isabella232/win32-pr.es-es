---
title: EN_IMECHANGE de notificación (Richedit.h)
description: Notifica al elemento primario de un control de edición enriquecido que el estado de conversión de IME ha cambiado.
ms.assetid: 2893e4ef-5904-4a57-95c5-3f6cfbb60d90
keywords:
- EN_IMECHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_IMECHANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fa0e0c8fe4e7d6d8de876a5d1a1fb7a10754096
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062039"
---
# <a name="en_imechange-notification-code"></a>Código de notificación de EN \_ IMECHANGE

Notifica al elemento primario de un control de edición enriquecido que el estado de conversión de IME ha cambiado. Este código de notificación solo *está disponible* para las versiones en idioma asiático del sistema operativo. Un control de edición enriquecido envía este código de notificación en forma de mensaje [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_IMECHANGE

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador del control de edición enriquecido. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Controlar el control de edición enriquecido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este código de notificación devuelve cero.

## <a name="remarks"></a>Observaciones

Para recibir los códigos de notificación EN \_ IMECHANGE, especifique [**ENM \_ IMECHANGE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**EM \_ SETEVENTMASK.**](em-seteventmask.md)

> [!Note]  
> Este código de notificación solo se admite en la versión de Asia de Rich Edit 1.0. No se admite en versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

