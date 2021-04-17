---
title: Código de notificación de CBN_DROPDOWN (Winuser. h)
description: Se envía cuando el cuadro de lista de un cuadro combinado está a punto de hacerse visible. La ventana primaria del cuadro combinado recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: 2ee9bb19-951b-46bb-a90d-1ade92c2d76c
keywords:
- CBN_DROPDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018dac2a17a656c11ac697836390ee64e55875db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658239"
---
# <a name="cbn_dropdown-notification-code"></a>\_Código de notificación de desplegable CBN

Se envía cuando el cuadro de lista de un cuadro combinado está a punto de hacerse visible. La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_DROPDOWN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene el identificador de control del cuadro combinado. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el código de notificación.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro combinado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este código de notificación solo se envía si el cuadro combinado tiene el estilo de la [**\_ lista desplegable CBS**](combo-box-styles.md) o [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) .

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

[CBN \_ primer plano](cbn-closeup.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

