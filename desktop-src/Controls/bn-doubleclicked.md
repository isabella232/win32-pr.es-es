---
title: Código de notificación de BN_DOUBLECLICKED (Winuser. h)
description: Se envía cuando el usuario hace doble clic en un botón.
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018df4387b026d68e3f4e9a6c259fb19efd4a0f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905108"
---
# <a name="bn_doubleclicked-notification-code"></a>Código de notificación de BN \_

Se envía cuando el usuario hace doble clic en un botón. Este código de notificación se envía automáticamente para los botones [**BS \_ USERBUTTON**](button-styles.md), [**BS \_**](button-styles.md)y [**BS \_**](button-styles.md) . Otros tipos de botón envían BN \_ solo si tienen el estilo de [**\_ notificación BS**](button-styles.md) .

La ventana primaria del botón recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_DOUBLECLICKED

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

BN al \_ es el mismo que el código de notificación [BN \_ DBLCLK](bn-dblclk.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

