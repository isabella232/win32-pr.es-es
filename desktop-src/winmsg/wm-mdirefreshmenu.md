---
description: Una aplicación envía el mensaje WM MDIREFRESHMENU a una ventana cliente de interfaz de múltiples documentos (MDI) para actualizar el menú de ventana de la \_ ventana marco MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: WM_MDIREFRESHMENU mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4eafa7b84dc9389e57d379a30019505e85fb602
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247455"
---
# <a name="wm_mdirefreshmenu-message"></a>Mensaje \_ MDIREFRESHMENU de WM

Una aplicación envía el **mensaje WM \_ MDIREFRESHMENU** a una ventana cliente de interfaz de múltiples documentos (MDI) para actualizar el menú de ventana de la ventana marco MDI.


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HMENU**

Si el mensaje se realiza correctamente, el valor devuelto es el identificador del menú de ventana de marco.

Si se produce un error en el mensaje, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

Después de enviar este mensaje, una aplicación debe llamar a la [**función DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) para actualizar la barra de menús.

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

[**WM \_ MDISETMENU**](wm-mdisetmenu.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Interfaz de varios documentos](multiple-document-interface.md)
</dt> </dl>

 

 
