---
title: Código de notificación de EN_VSCROLL (Winuser. h)
description: Se envía cuando el usuario hace clic en la barra de desplazamiento vertical de un control de edición o cuando el usuario desplaza la rueda del mouse sobre el control de edición.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL controles de código de notificación de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905629"
---
# <a name="en_vscroll-notification-code"></a>\_Código de notificación en VSCROLL

Se envía cuando el usuario hace clic en la barra de desplazamiento vertical de un control de edición o cuando el usuario desplaza la rueda del mouse sobre el control de edición. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) . Se notifica a la ventana primaria antes de que se actualice la pantalla.


```C++
EN_VSCROLL

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control de edición. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control de edición.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este mensaje se envía para los siguientes eventos del mouse en la barra de desplazamiento vertical: al hacer clic en cualquier botón de flecha o hacer clic entre el botón de flecha y el control de posición. Sin embargo, el mensaje no se envía al hacer clic en el propio Mouse de la barra de desplazamiento. El mensaje también se envía cuando un evento de teclado provoca un cambio en el área de vista del control de edición, por ejemplo, al presionar Inicio, fin, Re Pág, Av Pág, flecha arriba o flecha abajo.

La rueda del mouse es un mouse con una rueda central que se desplaza. Para obtener más información, vea "la rueda del mouse" en acerca de la [entrada del mouse](/windows/desktop/inputdev/about-mouse-input).

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para recibir los \_ códigos de notificación en VSCROLL, especifique [**ENM \_ Scroll**](rich-edit-control-event-mask-flags.md) en la máscara enviada con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) . Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[EN \_ HSCROLL](en-hscroll.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Usar controles de edición](using-edit-controls.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

