---
title: Código de notificación de EN_ERRSPACE (Winuser. h)
description: Se envía cuando un control de edición no puede asignar suficiente memoria para satisfacer una solicitud concreta. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de comando de WM \_ .
ms.assetid: 23a6eb10-a9d7-4fd5-9176-407c35e6f492
keywords:
- EN_ERRSPACE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- EN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05b100811741ee5c5f6bf53eb49ff05b118de3c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905037"
---
# <a name="en_errspace-notification-code"></a>\_Código de notificación en ERRSPACE

Se envía cuando un control de edición no puede asignar suficiente memoria para satisfacer una solicitud concreta. La ventana primaria del control de edición recibe este código de notificación a través de un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ERRSPACE

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

La ventana primaria siempre obtendrá un mensaje [**de \_ comando de WM**](/windows/desktop/menurc/wm-command) para este evento; no requiere que se envíe una máscara de notificación con el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

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

 

