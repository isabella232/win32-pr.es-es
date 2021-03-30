---
title: Código de notificación de STN_DBLCLK (Winuser. h)
description: El \_ código de notificación STN DBLCLK se envía cuando el usuario hace doble clic en un control estático que tenga el \_ estilo SS Notify. La ventana primaria del control recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- STN_DBLCLK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 853ed5142de99dc85b729b4c4ea208273d4ace1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079073"
---
# <a name="stn_dblclk-notification-code"></a>Código de notificación de DBLCLK de STN \_

El \_ código de notificación STN DBLCLK se envía cuando el usuario hace doble clic en un control estático que tenga el estilo [**SS \_ Notify**](static-control-styles.md) . La ventana primaria del control recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
STN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador del control estático. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control estático.

</dd> </dl>

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

[STN \_ clic](stn-clicked.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Controles estáticos](static-controls.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

