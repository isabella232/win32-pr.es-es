---
title: Mensaje de WM_CTLCOLORDLG (Winuser. h)
description: Se envía a un cuadro de diálogo antes de que el sistema dibuje el cuadro de diálogo. Al responder a este mensaje, el cuadro de diálogo puede establecer sus colores de texto y de fondo mediante el identificador de contexto de dispositivo de pantalla especificado.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- WM_CTLCOLORDLG cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833d3894a85342b0f26323ceed0f4fb3356c48ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801267"
---
# <a name="wm_ctlcolordlg-message"></a>Mensaje de CTLCOLORDLG de WM \_

Se envía a un cuadro de diálogo antes de que el sistema dibuje el cuadro de diálogo. Al responder a este mensaje, el cuadro de diálogo puede establecer sus colores de texto y de fondo mediante el identificador de contexto de dispositivo de pantalla especificado.


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto de dispositivo para el cuadro de diálogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver un identificador a un pincel. El sistema utiliza el pincel para pintar el fondo del cuadro de diálogo.

## <a name="remarks"></a>Observaciones

De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el cuadro de diálogo.

El sistema no destruye automáticamente el pincel devuelto. Es responsabilidad de la aplicación destruir el pincel cuando ya no se necesita.

El mensaje de **\_ CTLCOLORDLG de WM** nunca se envía entre subprocesos. Solo se envía dentro de un subproceso.

Tenga en cuenta que el mensaje de **\_ CTLCOLORDLG de WM** se envía al propio cuadro de diálogo; todos los demás mensajes **WM \_ CTLCOLOR \** _ se envían al propietario del control.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado en un _ *int \_ ptr** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado. Se omite el valor de **DWL \_ MSGRESULT** establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Vista**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

