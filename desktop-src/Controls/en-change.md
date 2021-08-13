---
title: EN_CHANGE de notificación (Winuser.h)
description: Se envía cuando el usuario ha realizado una acción que puede haber modificado el texto en un control de edición.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- EN_CHANGE código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86dbfb90376a85df09cad854882fa2616e6b7cb247cab4106850608a4b96ad4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437055"
---
# <a name="en_change-notification-code"></a>Código de notificación DE CAMBIO \_ DE EN

Se envía cuando el usuario ha realizado una acción que puede haber modificado el texto en un control de edición. A diferencia del código de notificación de [EN \_ UPDATE,](en-update.md) este código de notificación se envía después de que el sistema actualice la pantalla. La ventana primaria del control de edición recibe este código de notificación a través de un [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_CHANGE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador del control de edición. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control de edición.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para recibir códigos de notificación EN \_ CHANGE, especifique [**ENM \_ CHANGE**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**\_ EM SETEVENTMASK.**](em-seteventmask.md) Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

El código de notificación EN CHANGE no se envía cuando se usa el estilo \_ [**ES \_ MULTILINE**](edit-control-styles.md) y el texto se envía a través [**de WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[EN \_ UPDATE](en-update.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

