---
title: Mensaje de WM_CTLCOLORLISTBOX (Winuser. h)
description: Se envía a la ventana primaria de un cuadro de lista antes de que el sistema dibuje el cuadro de lista. Al responder a este mensaje, la ventana primaria puede establecer los colores de texto y de fondo del cuadro de lista utilizando el identificador de contexto de dispositivo de pantalla especificado.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- WM_CTLCOLORLISTBOX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949af76bd05aa9ad3a3e720c89be33cfe76ed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150227"
---
# <a name="wm_ctlcolorlistbox-message"></a>Mensaje de CTLCOLORLISTBOX de WM \_

Se envía a la ventana primaria de un cuadro de lista antes de que el sistema dibuje el cuadro de lista. Al responder a este mensaje, la ventana primaria puede establecer los colores de texto y de fondo del cuadro de lista utilizando el identificador de contexto de dispositivo de pantalla especificado.


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto de dispositivo para el cuadro de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cuadro de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver un identificador a un pincel. El sistema utiliza el pincel para pintar el fondo del cuadro de lista.

## <a name="remarks"></a>Observaciones

De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) selecciona los colores predeterminados del sistema para el cuadro de lista.

El mensaje de **\_ CTLCOLORLISTBOX de WM** nunca se envía entre subprocesos. Solo se envía dentro de un subproceso.

Si un procedimiento de cuadro de diálogo controla este mensaje, debe convertir el valor devuelto deseado a **int \_ ptr** y devolver el valor directamente. Si el procedimiento del cuadro de diálogo devuelve **false**, se realiza el control de mensajes predeterminado. Se omite el valor de **DWL \_ MSGRESULT** establecido por la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Otros recursos**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

