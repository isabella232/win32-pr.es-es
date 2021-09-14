---
description: Recupera el identificador de la barra de aplicaciones de autohide asociada a un borde de la pantalla. Este mensaje extiende ABM GETAUTOHIDEBAR al permitirle especificar un monitor determinado, para su uso \_ en varias situaciones de supervisión.
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
ms.openlocfilehash: 2ef95739a1031efb199e6acd99686e0858a9630e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361069"
---
# <a name="abm_getautohidebarex-message"></a>Mensaje \_ GETAUTOHIDEBAREX de ABM

Recupera el identificador de la barra de aplicaciones de autohide asociada a un borde de la pantalla. Este mensaje extiende [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) al permitirle especificar un monitor determinado, para su uso en varias situaciones de supervisión.


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que especifica el borde de la pantalla y el monitor. Debe especificar los **miembros cbSize**, **uEdge** **y rc** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la barra de aplicaciones autohide. El valor devuelto es **NULL** si se produce un error o si no hay ninguna barra de aplicaciones autohide asociada al borde dado del monitor especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




