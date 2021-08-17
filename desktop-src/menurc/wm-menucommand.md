---
title: WM_MENUCOMMAND mensaje (Winuser.h)
description: Se envía cuando el usuario realiza una selección desde un menú.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d97f629b5d4b0c245606b36efea9ebcb230c4c9fd14d837e18949880a7e7e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971814"
---
# <a name="wm_menucommand-message"></a>Mensaje \_ MENUCOMMAND de WM

Se envía cuando el usuario realiza una selección desde un menú.


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero del elemento seleccionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del menú del elemento seleccionado.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **mensaje \_ MENUCOMMAND** de WM proporciona un identificador al menú para que pueda acceder a los datos del menú en la estructura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) y también proporciona el índice del elemento seleccionado, que normalmente es lo que necesitan las aplicaciones. Por el contrario, el [**mensaje \_ WM COMMAND**](wm-command.md) proporciona el identificador del elemento de menú.

El **mensaje \_ MENUCOMMAND de WM** solo se envía para los menús definidos con la marca **MNS \_ NOTIFYBYPOS** establecida en el miembro **dwStyle** de la [**estructura MENUINFO.**](/windows/win32/api/winuser/ns-winuser-menuinfo)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción a los menús](menus.md)
</dt> </dl>

 

 





