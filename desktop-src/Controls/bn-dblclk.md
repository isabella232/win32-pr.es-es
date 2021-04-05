---
title: Código de notificación de BN_DBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic en un botón.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04c6bf52e213056d85d3a6d038bedb83754a27e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079137"
---
# <a name="bn_dblclk-notification-code"></a>Código de notificación de DBLCLK de BN \_

Se envía cuando el usuario hace doble clic en un botón. Este código de notificación se envía automáticamente para los botones [**BS \_ USERBUTTON**](button-styles.md), [**BS \_**](button-styles.md)y [**BS \_**](button-styles.md) . Otros tipos de botón envían BN \_ DBLCLK solo si tienen el estilo de [**\_ notificación de BS**](button-styles.md) .

La ventana primaria del botón recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del botón. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del botón.

</dd> </dl>

## <a name="remarks"></a>Observaciones

BN \_ DBLCLK es el mismo que el código de notificación de [BN \_ ](bn-doubleclicked.md) .

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

[BN \_ clic](bn-clicked.md)
</dt> <dt>

[BN \_](bn-doubleclicked.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

