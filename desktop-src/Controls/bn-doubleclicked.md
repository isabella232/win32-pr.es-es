---
title: BN_DOUBLECLICKED de notificación (Winuser.h)
description: 'BN_DOUBLECLICKED de notificación: se envía cuando el usuario hace doble clic en un botón.'
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED código de notificación Windows controles
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
ms.openlocfilehash: 64a11a4dec91a7a2f1d200c4c86c6989d846604a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062237"
---
# <a name="bn_doubleclicked-notification-code"></a>Código de notificación \_ DOUBLECLICKED de BN

Se envía cuando el usuario hace doble clic en un botón. Este código de notificación se envía automáticamente para los [**botones \_ BS USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)y [**BS \_ OWNERDRAW.**](button-styles.md) Otros tipos de botón envían BN \_ DOUBLECLICKED solo si tienen el [**estilo \_ NOTIFY de BS.**](button-styles.md)

La ventana primaria del botón recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_DOUBLECLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

LOWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador de control del botón. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del botón.

</dd> </dl>

## <a name="remarks"></a>Observaciones

BN \_ DOUBLECLICKED es igual que el código de [notificación \_ DBLCLK de BN.](bn-dblclk.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



 

