---
title: EN_HSCROLL de notificación (Winuser.h)
description: Se envía cuando el usuario hace clic en la barra de desplazamiento horizontal de un control de edición. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje \_ WM COMMAND. Se notifica a la ventana primaria antes de que se actualice la pantalla.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- EN_HSCROLL código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e5b0f42d08977f7a1be68a5010aa7403b10fc2e5a126aa542bb25a644a7b70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436775"
---
# <a name="en_hscroll-notification-code"></a>Código de notificación DE EN \_ HSCROLL

Se envía cuando el usuario hace clic en la barra de desplazamiento horizontal de un control de edición. La ventana primaria del control de edición recibe este código de notificación a través de un [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command) Se notifica a la ventana primaria antes de que se actualice la pantalla.


```C++
EN_HSCROLL

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

Este código de notificación se envía para los siguientes eventos del mouse en la barra de desplazamiento horizontal: haciendo clic en cualquiera de los botones de flecha o entre el botón de flecha y el control. Sin embargo, el código de notificación no se envía al hacer clic en el propio control de la barra de desplazamiento. El código de notificación también se envía cuando un evento de teclado provoca un cambio en el área de vista del control de edición, por ejemplo, al presionar INICIO, FIN, FLECHA IZQUIERDA o FLECHA DERECHA.

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para recibir **códigos de notificación EN \_ HSCROLL,** especifique [**ENM \_ SCROLL**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el [**mensaje EM \_ SETEVENTMASK.**](em-seteventmask.md) Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

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

[EN \_ VSCROLL](en-vscroll.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

