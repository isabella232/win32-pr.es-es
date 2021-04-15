---
title: Mensaje de WM_MENUCOMMAND (Winuser. h)
description: Se envía cuando el usuario realiza una selección en un menú.
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
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422623"
---
# <a name="wm_menucommand-message"></a>\_Mensaje MENUCOMMAND de WM

Se envía cuando el usuario realiza una selección en un menú.


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

Identificador del menú para el elemento seleccionado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **mensaje \_ MENUCOMMAND de WM** le proporciona un identificador para el menú, de modo que pueda tener acceso a los datos de menú en la estructura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) y también le proporcionará el índice del elemento seleccionado, que es normalmente lo que necesitan las aplicaciones. En cambio, el mensaje de [**\_ comando de WM**](wm-command.md) le proporciona el identificador del elemento de menú.

El **mensaje \_ MENUCOMMAND de WM** solo se envía para los menús que se definen con la marca **mns \_ NOTIFYBYPOS** establecida en el miembro **dwStyle** de la estructura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general sobre menús](menus.md)
</dt> </dl>

 

 





