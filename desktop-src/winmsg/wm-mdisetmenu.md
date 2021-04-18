---
description: Una aplicación envía el \_ mensaje de MDISETMENU de WM a una ventana de cliente de la interfaz de múltiples documentos (MDI) para reemplazar el menú completo de una ventana de marco MDI, para reemplazar el menú ventana de la ventana marco o ambos.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: Mensaje de WM_MDISETMENU (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74b90aed079482e2d2b666432f72c15d6ca27896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720530"
---
# <a name="wm_mdisetmenu-message"></a>Mensaje de MDISETMENU de WM \_

Una aplicación envía el mensaje de **\_ MDISETMENU de WM** a una ventana de cliente de la interfaz de múltiples documentos (MDI) para reemplazar el menú completo de una ventana de marco MDI, para reemplazar el menú ventana de la ventana marco o ambos.


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del nuevo menú de la ventana de marco. Si este parámetro es **null**, el menú de la ventana de marco no cambia.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del menú de nueva ventana. Si este parámetro es **null**, el menú ventana no cambia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HMENU**

Si el mensaje se realiza correctamente, el valor devuelto es el identificador del menú de la ventana de marco anterior.

Si se produce un error en el mensaje, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Después de enviar este mensaje, una aplicación debe llamar a la función [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) para actualizar la barra de menús.

Si este mensaje reemplaza el menú ventana, los elementos de menú de la ventana secundaria MDI se quitan del menú ventana anterior y se agregan al menú nueva ventana.

Si una ventana secundaria MDI está maximizada y este mensaje reemplaza el menú ventana marco MDI, el icono de menú ventana y el icono restaurar se quitan del menú ventana de marco anterior y se agregan al menú nueva ventana marco.

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

[**MDIREFRESHMENU de WM \_**](wm-mdirefreshmenu.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 
