---
title: BN_DBLCLK de notificación (Winuser.h)
description: 'BN_DBLCLK de notificación: se envía cuando el usuario hace doble clic en un botón.'
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK código de notificación Windows controles
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
ms.openlocfilehash: fdb403f37b8fee9ea36023a7cd2511bbaaa2af81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062238"
---
# <a name="bn_dblclk-notification-code"></a>Código de notificación \_ DBLCLK de BN

Se envía cuando el usuario hace doble clic en un botón. Este código de notificación se envía automáticamente para los [**botones \_ BS USERBUTTON,**](button-styles.md) [**BS \_ RADIOBUTTON**](button-styles.md)y [**BS \_ OWNERDRAW.**](button-styles.md) Otros tipos de botón envían \_ DBLCLK de BN solo si tienen el [**estilo \_ BS NOTIFY.**](button-styles.md)

La ventana primaria del botón recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Loword [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el identificador de control del botón. [**HIWORD especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del botón.

</dd> </dl>

## <a name="remarks"></a>Observaciones

BN \_ DBLCLK es el mismo que el código [de notificación \_ DOUBLECLICKED de BN.](bn-doubleclicked.md)

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

[BN \_ CLICKED](bn-clicked.md)
</dt> <dt>

[BN \_ DOUBLECLICKED](bn-doubleclicked.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

