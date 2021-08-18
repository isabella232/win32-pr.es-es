---
title: EN_ALIGN_RTL_EC de notificación (Winuser.h)
description: Se envía cuando el usuario ha cambiado la dirección del control de edición a de derecha a izquierda. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje \_ WM COMMAND.
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- EN_ALIGN_RTL_EC código de notificación Windows controles
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16b44ecd143715eb5c1bc895ca5c20fa066b17b71ab31ee667e2d6b2b6a0852
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437095"
---
# <a name="en_align_rtl_ec-notification-code"></a>Código de notificación EC DE EN \_ ALIGN \_ RTL \_

Se envía cuando el usuario ha cambiado la dirección del control de edición a de derecha a izquierda. La ventana primaria del control de edición recibe este código de notificación a través de un [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

LOWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador del control de edición. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control de edición que envía el código de notificación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si hay un idioma bidireccional instalado en el sistema, por ejemplo, árabe o hebreo, puede cambiar la dirección del control de edición mediante CTRL+LSHIFT (de izquierda a derecha) y CTRL+RSHIFT (de derecha a izquierda).

**Edición enriquecte:** No se admite este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

