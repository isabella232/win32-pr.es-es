---
title: STN_CLICKED de notificación (Winuser.h)
description: El código de notificación DE STN CLICKED se envía cuando el usuario hace clic en un control estático \_ que tiene el estilo NOTIFY de SS. \_ La ventana primaria del control recibe este código de notificación a través del mensaje \_ WM COMMAND.
ms.assetid: deeac9e9-c23e-4ffb-a1d7-18782efb7a5c
keywords:
- STN_CLICKED código de notificación Windows controles
topic_type:
- apiref
api_name:
- STN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91f63bc496469f6edc26b4f9176f3f9157464bdd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166990"
---
# <a name="stn_clicked-notification-code"></a>Código de notificación CLICKED de STN \_

El código de notificación DE STN CLICKED se envía cuando el usuario hace clic en un control estático \_ que tiene el estilo NOTIFY [**\_ de SS.**](static-control-styles.md) La ventana primaria del control recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
STN_CLICKED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

LOWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador del control estático. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control estático.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[STN \_ DBLCLK](stn-dblclk.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Controles estáticos](static-controls.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

