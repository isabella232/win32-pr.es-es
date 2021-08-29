---
description: Registra o anula el registro de una barra de aplicaciones de mostrar automáticamente para un borde determinado de la pantalla. Este mensaje amplía ABM SETAUTOHIDEBAR al permitirle especificar un monitor determinado, para su uso \_ en varias situaciones de supervisión.
title: ABM_SETAUTOHIDEBAREX mensaje (Shellapi.h)
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
ms.openlocfilehash: d98bbfe9566aa5edeccb7d340de28b1fa4b249d26b8ad740a718ddc5e6bc6a68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884825"
---
# <a name="abm_setautohidebarex-message"></a>Mensaje \_ SETAUTOHIDEBAREX de ABM

Registra o anula el registro de una barra de aplicaciones de mostrar automáticamente para un borde determinado de la pantalla. Este mensaje amplía [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) al permitirle especificar un monitor determinado, para su uso en varias situaciones de supervisión.


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Establezca el **miembro lParam** en **TRUE para** registrar la barra de aplicaciones o **FALSE** para anular el registro. Debe especificar los **miembros cbSize**, **hWnd,** **uEdge,** **rc** y **lParam** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se realiza correctamente o **FALSE** si se produce un error o si ya se ha registrado una barra de aplicaciones de autohide para el borde dado en el monitor determinado.

## <a name="remarks"></a>Comentarios

El sistema solo permite mostrar automáticamente una barra de aplicaciones para cada borde de cada monitor. El monitor viene determinado por el **miembro rc** y el borde lo determina el **miembro uEdge** de la [**estructura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> </dl>

 

 




