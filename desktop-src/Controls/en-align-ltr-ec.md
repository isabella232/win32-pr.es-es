---
title: Código de notificación de EN_ALIGN_LTR_EC (Winuser. h)
description: Se envía cuando el usuario ha cambiado la dirección del control de edición de izquierda a derecha. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de comando de WM \_ .
ms.assetid: 231f9d00-c5a5-445e-9176-201fe1c14a0e
keywords:
- EN_ALIGN_LTR_EC controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_ALIGN_LTR_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4886c68a024005c4b2fddd71e1480b0a3545bdf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801892"
---
# <a name="en_align_ltr_ec-notification-code"></a>EN \_ el \_ código de notificación de EC de alineación LTR \_

Se envía cuando el usuario ha cambiado la dirección del control de edición de izquierda a derecha. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ALIGN_LTR_EC

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

Identificador del control de edición que envía el código de notificación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si hay un idioma bidireccional instalado en el sistema, por ejemplo, el árabe o el hebreo, puede cambiar la dirección del control de edición mediante CTRL + LSHIFT (de izquierda a derecha) y CTRL + RSHIFT (de derecha a izquierda).

**Edición enriquecida:** No se admite este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

