---
title: Mensaje de WM_NEXTMENU (Winuser. h)
description: Se envía a una aplicación cuando se usa la tecla de dirección derecha o izquierda para cambiar entre la barra de menús y el menú del sistema.
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
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997142"
---
# <a name="wm_nextmenu-message"></a>Mensaje de NEXTMENU de WM \_

Se envía a una aplicación cuando se usa la tecla de dirección derecha o izquierda para cambiar entre la barra de menús y el menú del sistema.


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Código de la clave virtual de la clave. Consulte [**códigos de tecla virtual**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) que contiene información sobre el menú que se va a activar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al responder a este mensaje, la aplicación puede especificar el menú al que se va a cambiar en el miembro **hmenuNext** de [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) y la ventana para recibir los mensajes de notificación de menú en el miembro **hwndNext** de la estructura **MDINEXTMENU** . Debe establecer ambos miembros para que los cambios surtan efecto (son inicialmente **null**).

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

[**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

**Vista**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

