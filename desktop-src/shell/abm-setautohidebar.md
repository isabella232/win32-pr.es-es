---
description: Registra o anula el registro de un Appbar de ocultación para un borde determinado de la pantalla. Si el sistema tiene varios monitores, se utiliza el monitor que contiene la barra de tareas principal.
title: Mensaje de ABM_SETAUTOHIDEBAR (ShellAPI. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984386"
---
# <a name="abm_setautohidebar-message"></a>ABN \_ SETAUTOHIDEBAR

Registra o anula el registro de un Appbar de ocultación para un borde determinado de la pantalla. Si el sistema tiene varios monitores, se utiliza el monitor que contiene la barra de tareas principal.

> [!Note]  
> Para registrar o anular el registro de un Appbar de ocultación automáticamente en un monitor específico, use [**ABN \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md).

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Establezca el miembro **lParam** en **true** para registrar el Appbar o **false** para anular su registro. Debe especificar los miembros **cbSize**, **hWnd**, **uEdge** y **lParam** al enviar este mensaje. se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** si se produce un error o si ya se ha registrado un Appbar de ocultación para el borde especificado.

## <a name="remarks"></a>Observaciones

El sistema solo permite un Appbar de ocultación automáticamente para cada borde de la pantalla. Esto se determina cuando se establece el miembro **uEdge** de la estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ABN \_ SETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABN \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABN \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




