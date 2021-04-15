---
description: Registra o anula el registro de un Appbar de ocultación para un borde determinado de la pantalla. Este mensaje amplía ABN \_ SETAUTOHIDEBAR, ya que permite especificar un monitor determinado para su uso en varias situaciones de supervisión.
title: Mensaje de ABM_SETAUTOHIDEBAREX (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104998887"
---
# <a name="abm_setautohidebarex-message"></a>ABN \_ SETAUTOHIDEBAREX

Registra o anula el registro de un Appbar de ocultación para un borde determinado de la pantalla. Este mensaje amplía [**ABN \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) , ya que permite especificar un monitor determinado para su uso en varias situaciones de supervisión.


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Establezca el miembro **lParam** en **true** para registrar el Appbar o **false** para anular su registro. Debe especificar los miembros **cbSize**, **hWnd**, **uEdge**, **RC** y **lParam** al enviar este mensaje. se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** si se produce un error o si ya se ha registrado un Appbar de ocultación para el borde dado en el monitor determinado.

## <a name="remarks"></a>Observaciones

El sistema solo permite un Appbar de ocultación automáticamente para cada borde de cada monitor. El monitor viene determinado por el miembro **RC** y el límite viene determinado por el miembro **uEdge** de la estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>ShellAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ABN \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABN \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABN \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> </dl>

 

 




