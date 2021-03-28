---
description: Recupera el identificador del Appbar de ocultación automático asociado a un borde de la pantalla. Este mensaje amplía ABN \_ GETAUTOHIDEBAR, ya que permite especificar un monitor determinado para su uso en varias situaciones de supervisión.
title: Mensaje de ABM_GETAUTOHIDEBAREX (ShellAPI. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987517"
---
# <a name="abm_getautohidebarex-message"></a>ABN \_ GETAUTOHIDEBAREX

Recupera el identificador del Appbar de ocultación automático asociado a un borde de la pantalla. Este mensaje amplía [**ABN \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) , ya que permite especificar un monitor determinado para su uso en varias situaciones de supervisión.


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que especifica el borde y el monitor de la pantalla. Debe especificar los miembros **cbSize**, **uEdge** y **RC** al enviar este mensaje. se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador del Appbar de ocultación automáticamente. El valor devuelto es **null** si se produce un error o si no hay ningún Appbar de ocultación automático asociado al borde determinado del monitor determinado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>ShellAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ABN \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABN \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABN \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




