---
title: Mensaje de WM_NEXTDLGCTL (Winuser. h)
description: Se envía a un procedimiento de cuadro de diálogo para establecer el foco de teclado en un control diferente en el cuadro de diálogo.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- WM_NEXTDLGCTL cuadros de diálogo de mensaje
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534731"
---
# <a name="wm_nextdlgctl-message"></a>Mensaje de NEXTDLGCTL de WM \_

Se envía a un procedimiento de cuadro de diálogo para establecer el foco de teclado en un control diferente en el cuadro de diálogo.


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Si *lParam* es **true**, este parámetro identifica el control que recibe el foco. Si *lParam* es **false**, este parámetro indica si el control siguiente o anterior con el estilo **WS \_ TABSTOP** recibe el foco. Si *wParam* es cero, el control siguiente recibe el foco; de lo contrario, el control anterior con el estilo **WS \_ TABSTOP** recibe el foco.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior indica el modo en que el sistema utiliza *wParam*. Si la palabra de orden inferior es **true**, *wParam* es un identificador asociado al control que recibe el foco. de lo contrario, *wParam* es una marca que indica si el control siguiente o anterior con el estilo **WS \_ TABSTOP** recibe el foco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Este mensaje realiza operaciones adicionales de administración de cuadros de diálogo más allá de las realizadas por la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) **\_ NEXTDLGCTL** actualiza el borde de pulsador predeterminado, establece el identificador de control predeterminado y selecciona automáticamente el texto de un control de edición (si la ventana de destino es un control de edición).

No use la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para enviar un mensaje **de \_ NEXTDLGCTL de WM** si la aplicación va a procesar simultáneamente otros mensajes que establecieron el foco. En su lugar, use la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .

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

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Vista**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> </dl>

 

