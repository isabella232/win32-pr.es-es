---
description: Recupera el identificador del Appbar de ocultación automático asociado a un borde de la pantalla. Si el sistema tiene varios monitores, se utiliza el monitor que contiene la barra de tareas principal.
title: Mensaje de ABM_GETAUTOHIDEBAR (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153927"
---
# <a name="abm_getautohidebar-message"></a>ABN \_ GETAUTOHIDEBAR

Recupera el identificador del Appbar de ocultación automático asociado a un borde de la pantalla. Si el sistema tiene varios monitores, se utiliza el monitor que contiene la barra de tareas principal.

> [!Note]  
> Para consultar un Appbar de ocultación automáticamente en un monitor específico, use [**ABN \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md).

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que especifica el borde de la pantalla. Debe especificar los miembros **cbSize** y **uEdge** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del Appbar de ocultación automáticamente. El valor devuelto es **null** si se produce un error o si no hay ningún Appbar de ocultación automático asociado al borde especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ABN \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABN \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABN \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




