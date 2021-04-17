---
description: Una aplicación envía el \_ mensaje de MDIREFRESHMENU de WM a una ventana de cliente de la interfaz de múltiples documentos (MDI) para actualizar el menú ventana de la ventana de marco MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: Mensaje de WM_MDIREFRESHMENU (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677919"
---
# <a name="wm_mdirefreshmenu-message"></a>Mensaje de MDIREFRESHMENU de WM \_

Una aplicación envía el mensaje de **\_ MDIREFRESHMENU de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para actualizar el menú ventana de la ventana de marco MDI.


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HMENU**

Si el mensaje se realiza correctamente, el valor devuelto es el identificador del menú de la ventana de marco.

Si se produce un error en el mensaje, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

Después de enviar este mensaje, una aplicación debe llamar a la función [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) para actualizar la barra de menús.

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

[**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**MDISETMENU de WM \_**](wm-mdisetmenu.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 
