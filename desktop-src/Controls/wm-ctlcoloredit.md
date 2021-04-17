---
title: Mensaje de WM_CTLCOLOREDIT (Winuser. h)
description: Un control de edición que no es de solo lectura o está deshabilitado envía el mensaje de CTLCOLOREDIT de WM \_ a su ventana primaria cuando el control está a punto de dibujarse.
ms.assetid: 2294e3b8-00a7-43ef-b20a-fe0e46764055
keywords:
- WM_CTLCOLOREDIT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLOREDIT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e100367f37018424fad33dc7cea30700183a0a2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489004"
---
# <a name="wm_ctlcoloredit-message"></a>Mensaje de CTLCOLOREDIT de WM \_

Un control de edición que no es de solo lectura o está deshabilitado envía el mensaje de **\_ CTLCOLOREDIT de WM** a su ventana primaria cuando el control está a punto de dibujarse. Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de dispositivo especificado para establecer los colores de texto y de fondo del control de edición.


```C++
WM_CTLCOLOREDIT

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto de dispositivo para la ventana de control de edición.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del control de edición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver el identificador de un pincel. El sistema utiliza el pincel para pintar el fondo del control de edición.

## <a name="remarks"></a>Observaciones

Si la aplicación devuelve un pincel que creó (por ejemplo, mediante la función [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) o [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), la aplicación debe liberar el pincel. Si la aplicación devuelve un pincel del sistema (por ejemplo, uno recuperado por la función [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) o [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), no es necesario que la aplicación libere el pincel.

De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el control de edición.

Los controles de edición de solo lectura o deshabilitados no envían el mensaje de **\_ CTLCOLOREDIT de WM** ; en su lugar, envían el mensaje de [**\_ CTLCOLORSTATIC de WM**](wm-ctlcolorstatic.md) .

El mensaje de **\_ CTLCOLOREDIT de WM** nunca se envía entre subprocesos, solo se envía dentro del mismo subproceso.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado a **int \_ ptr** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado. \_Se omite el valor de DWL MSGRESULT establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

**Edición enriquecida:** Este mensaje no se admite. Para establecer el color de fondo de un control Rich Edit, utilice el mensaje [**\_ SETBKGNDCOLOR em**](em-setbkgndcolor.md) .

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

[**\_SETBKGNDCOLOR em**](em-setbkgndcolor.md)
</dt> <dt>

[**CTLCOLORSTATIC de WM \_**](wm-ctlcolorstatic.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

