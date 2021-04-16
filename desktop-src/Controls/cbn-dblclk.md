---
title: Código de notificación de CBN_DBLCLK (Winuser. h)
description: Se envía cuando el usuario hace doble clic en una cadena en el cuadro de lista de un cuadro combinado. La ventana primaria del cuadro combinado recibe este código de notificación a través del \_ mensaje de comando de WM.
ms.assetid: 79ca3fd3-4a71-4bd5-be68-efc867a4ad22
keywords:
- CBN_DBLCLK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- CBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841c68079572e1740f074034c1a8097ba6a86253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658401"
---
# <a name="cbn_dblclk-notification-code"></a>Código de notificación de DBLCLK de CBN \_

Se envía cuando el usuario hace doble clic en una cadena en el cuadro de lista de un cuadro combinado. La ventana primaria del cuadro combinado recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_DBLCLK

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

Este código de notificación solo se produce para un cuadro combinado con el estilo [**\_ simple CBS**](combo-box-styles.md) . En un cuadro combinado con la [**lista \_ desplegable CBS**](combo-box-styles.md) o el estilo de [**\_ DROPDOWNLIST de CBS**](combo-box-styles.md) , no se puede producir un doble clic porque un solo clic cierra el cuadro de lista.

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

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando de WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

