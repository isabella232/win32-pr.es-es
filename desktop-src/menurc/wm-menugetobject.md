---
title: Mensaje de WM_MENUGETOBJECT (Winuser. h)
description: Se envía al propietario de un menú de arrastrar y colocar cuando el cursor del Mouse entra en un elemento de menú o se mueve desde el centro del elemento hasta la parte superior o inferior del elemento.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535553"
---
# <a name="wm_menugetobject-message"></a>Mensaje de MENUGETOBJECT de WM \_

Se envía al propietario de un menú de arrastrar y colocar cuando el cursor del Mouse entra en un elemento de menú o se mueve desde el centro del elemento hasta la parte superior o inferior del elemento.


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La aplicación debe devolver uno de los valores siguientes.



| Código o valor devuelto                                                                                                                                                | Descripción                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNGO \_ NoError**</dt> <dt>0x00000001</dt> </dl>     | Se devolvió un puntero de interfaz en el miembro **pvObj** de [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)<br/> |
| <dl> <dt>**MNGO \_ Nointerface**</dt> <dt>0x00000000</dt> </dl> | No se admite la interfaz.<br/>                                                                             |



 

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

 

 





