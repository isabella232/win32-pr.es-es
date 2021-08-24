---
title: WM_NEXTDLGCTL mensaje (Winuser.h)
description: Se envía a un procedimiento de cuadro de diálogo para establecer el foco del teclado en un control diferente en el cuadro de diálogo.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- WM_NEXTDLGCTL diálogo de mensaje
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
ms.openlocfilehash: 1a14de889e614aaba28757716326bcd1cf843aed64fe2dc58ca86430d65db628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606225"
---
# <a name="wm_nextdlgctl-message"></a>Mensaje \_ NEXTDLGCTL de WM

Se envía a un procedimiento de cuadro de diálogo para establecer el foco del teclado en un control diferente en el cuadro de diálogo.


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Si *lParam* es **TRUE,** este parámetro identifica el control que recibe el foco. Si *lParam* es **FALSE,** este parámetro indica si el control siguiente o anterior con el estilo **\_ TABSTOP** de WS recibe el foco. Si *wParam* es cero, el siguiente control recibe el foco; De lo contrario, el control anterior con el **estilo \_ TABSTOP** de WS recibe el foco.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo indica cómo usa el sistema *wParam*. Si la palabra de orden bajo es **TRUE,** *wParam* es un identificador asociado al control que recibe el foco; de lo *contrario, wParam* es una marca que indica si el control siguiente o anterior con el estilo **\_ TABSTOP** de WS recibe el foco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una aplicación debe devolver cero si procesa este mensaje.

## <a name="remarks"></a>Comentarios

Este mensaje realiza operaciones de administración de cuadros de diálogo adicionales más allá de las realizadas por la función [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) **WM \_ NEXTDLGCTL** actualiza el borde del botón de inserción predeterminado, establece el identificador de control predeterminado y selecciona automáticamente el texto de un control de edición (si la ventana de destino es un control de edición).

No use la [**función SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para enviar un mensaje **DE WM \_ NEXTDLGCTL** si la aplicación procesará simultáneamente otros mensajes que establecen el foco. Use la [**función PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) en su lugar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**Setfocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Cuadros de diálogo](dialog-boxes.md)
</dt> </dl>

 

