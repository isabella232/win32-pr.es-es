---
description: Recupera el identificador de la barra de aplicaciones de autohide asociada a un borde de la pantalla. Si el sistema tiene varios monitores, se usa el monitor que contiene la barra de tareas principal.
title: ABM_GETAUTOHIDEBAR mensaje (Shellapi.h)
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
ms.openlocfilehash: 5ce38caf8cc1ad39e682aa8650e08e4860a3406e33669008d6ceee65e0416149
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051157"
---
# <a name="abm_getautohidebar-message"></a>Mensaje \_ GETAUTOHIDEBAR de ABM

Recupera el identificador de la barra de aplicaciones de autohide asociada a un borde de la pantalla. Si el sistema tiene varios monitores, se usa el monitor que contiene la barra de tareas principal.

> [!Note]  
> Para consultar una barra de aplicaciones de autohide en un monitor específico, use [**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md).

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que especifica el borde de la pantalla. Debe especificar los **miembros cbSize** **y uEdge** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la barra de aplicaciones autohide. El valor devuelto es **NULL** si se produce un error o si no hay ninguna barra de aplicaciones autohide asociada al borde especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




