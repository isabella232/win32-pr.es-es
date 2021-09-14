---
title: EN_VSCROLL de notificación (Winuser.h)
description: Se envía cuando el usuario hace clic en la barra de desplazamiento vertical de un control de edición o cuando el usuario desplaza la rueda del mouse sobre el control de edición.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062015"
---
# <a name="en_vscroll-notification-code"></a>Código \_ de notificación de EN VSCROLL

Se envía cuando el usuario hace clic en la barra de desplazamiento vertical de un control de edición o cuando el usuario desplaza la rueda del mouse sobre el control de edición. La ventana primaria del control de edición recibe este código de notificación a través de un [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command) Se notifica a la ventana primaria antes de que se actualice la pantalla.


```C++
EN_VSCROLL

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

Este mensaje se envía para los siguientes eventos del mouse en la barra de desplazamiento vertical: haciendo clic en cualquiera de los botones de flecha o haciendo clic entre el botón de flecha y el control. Sin embargo, el mensaje no se envía al hacer clic en el mouse de la barra de desplazamiento. El mensaje también se envía cuando un evento de teclado provoca un cambio en el área de vista del control de edición, por ejemplo, al presionar INICIO, END, PAGE UP, PAGE DOWN, FLECHA ARRIBA o FLECHA ABAJO.

La rueda del mouse es un mouse que tiene una rueda central que se desplaza. Para obtener más información, vea "La rueda del mouse" en [Acerca de la entrada del mouse](/windows/desktop/inputdev/about-mouse-input).

**Edición enriquecte:** Compatible con Microsoft Rich Edit 1.0 y versiones posteriores. Para recibir códigos de notificación EN VSCROLL, especifique ENM SCROLL en la máscara enviada con el mensaje \_ [**EM \_ SETEVENTMASK.**](em-seteventmask.md) [**\_**](rich-edit-control-event-mask-flags.md) Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[EN \_ HSCROLL](en-hscroll.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Usar controles de edición](using-edit-controls.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

