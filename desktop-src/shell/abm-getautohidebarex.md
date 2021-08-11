---
description: Recupera el identificador de la barra de aplicaciones autohide asociada a un borde de la pantalla. Este mensaje amplía ABM GETAUTOHIDEBAR al permitirle especificar un monitor determinado, para su uso \_ en varias situaciones de supervisión.
title: ABM_GETAUTOHIDEBAREX mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9aecbc81e313c3d971b310cc35bd399b93cc18f2ef2a4f02a00d51a16745eb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225244"
---
# <a name="abm_getautohidebarex-message"></a>Mensaje \_ GETAUTOHIDEBAREX de ABM

Recupera el identificador de la barra de aplicaciones autohide asociada a un borde de la pantalla. Este mensaje amplía [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) al permitirle especificar un monitor determinado, para su uso en varias situaciones de supervisión.


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que especifica el borde de la pantalla y el monitor. Debe especificar los **miembros cbSize**, **uEdge** y **rc** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la barra de aplicaciones autohide. El valor devuelto es **NULL si** se produce un error o si no hay ninguna barra de aplicaciones autohide asociada al borde dado del monitor especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Consulta también

<dl> <dt>

[**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




