---
description: Una aplicación envía el mensaje WM MDISETMENU a una ventana cliente de interfaz de múltiples documentos (MDI) para reemplazar todo el menú de una ventana de marco MDI, para reemplazar el menú de ventana de la ventana de marco, o \_ ambos.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: WM_MDISETMENU mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fe87682691c5f113034c20c68cefd81ca3a7018bd44eb868c4f18551cacacd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772075"
---
# <a name="wm_mdisetmenu-message"></a>Mensaje \_ MDISETMENU de WM

Una aplicación envía el mensaje **\_ WM MDISETMENU** a una ventana cliente de interfaz de múltiples documentos (MDI) para reemplazar todo el menú de una ventana de marco MDI, para reemplazar el menú de ventana de la ventana de marco, o ambos.


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del nuevo menú de ventana de marco. Si este parámetro es **NULL,** no se cambia el menú de la ventana de marco.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del nuevo menú de la ventana. Si este parámetro es **NULL,** no se cambia el menú de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HMENU**

Si el mensaje se realiza correctamente, el valor devuelto es el identificador del menú de la ventana de marco anterior.

Si se produce un error en el mensaje, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

Después de enviar este mensaje, una aplicación debe llamar a la [**función DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) para actualizar la barra de menús.

Si este mensaje reemplaza el menú de la ventana, los elementos de menú de la ventana secundaria MDI se quitan del menú de la ventana anterior y se agregan al nuevo menú de ventana.

Si se maximiza una ventana secundaria de MDI y este mensaje reemplaza el menú de la ventana marco MDI, el icono de menú de la ventana y el icono de restauración se quitan del menú anterior de la ventana de marco y se agregan al nuevo menú de ventana de marco.

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

[**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**WM \_ MDIREFRESHMENU**](wm-mdirefreshmenu.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 
