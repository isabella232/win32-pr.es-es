---
title: WM_NEXTMENU mensaje (Winuser.h)
description: Se envía a una aplicación cuando se usa la tecla de flecha derecha o izquierda para cambiar entre la barra de menús y el menú del sistema.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 635ce19efbcfdfd8451f929affbbe0fe2b2c000bc4912977062f3fba2c54e9c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952085"
---
# <a name="wm_nextmenu-message"></a>Mensaje \_ NEXTMENU de WM

Se envía a una aplicación cuando se usa la tecla de flecha derecha o izquierda para cambiar entre la barra de menús y el menú del sistema.


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de clave virtual de la clave. Consulte [**Códigos de clave virtual**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) que contiene información sobre el menú que se va a activar.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al responder a este mensaje, la aplicación puede especificar el menú al que se va a cambiar en el **miembro hmenuNext** de [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) y la ventana para recibir los mensajes de notificación de menú en el **miembro hwndNext** de la estructura **MDINEXTMENU.** Debe establecer ambos miembros para que los cambios sumen efecto (inicialmente son **NULL).**

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

[**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

