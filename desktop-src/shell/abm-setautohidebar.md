---
description: Registra o anula el registro de una barra de aplicaciones de mostrar automáticamente para un borde determinado de la pantalla. Si el sistema tiene varios monitores, se usa el monitor que contiene la barra de tareas principal.
title: ABM_SETAUTOHIDEBAR mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267943"
---
# <a name="abm_setautohidebar-message"></a>Mensaje \_ SETAUTOHIDEBAR de ABM

Registra o anula el registro de una barra de aplicaciones de mostrar automáticamente para un borde determinado de la pantalla. Si el sistema tiene varios monitores, se usa el monitor que contiene la barra de tareas principal.

> [!Note]  
> Para registrar o anular el registro de una barra de aplicaciones de mostrar automáticamente en un monitor específico, use [**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md).

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Establezca el **miembro lParam** **en TRUE para** registrar la barra de aplicaciones o **FALSE** para anular el registro. Debe especificar los **miembros cbSize**, **hWnd,** **uEdge** y **lParam** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se realiza correctamente o **FALSE** si se produce un error o si ya se ha registrado una barra de aplicaciones autohide para el borde determinado.

## <a name="remarks"></a>Observaciones

El sistema solo permite mostrar automáticamente una barra de aplicaciones para cada borde de la pantalla. Esto se determina cuando se establece **el miembro uEdge** de la [**estructura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




