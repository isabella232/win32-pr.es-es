---
description: Establece los Estados de ocultación y siempre visible de la barra de tareas de Windows.
title: Mensaje de ABM_SETSTATE (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984382"
---
# <a name="abm_setstate-message"></a>Mensaje de ABN \_ SETSTATE

Establece los Estados de ocultación y siempre visible de la barra de tareas de Windows.


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Debe especificar los miembros **cbSize** y **hWnd** al enviar este mensaje. Los datos para el estado deseado se envían en el miembro **lParam** con uno de los valores siguientes.

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

Ocultar automáticamente y siempre en la parte superior desactivado

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**\_ALWAYSONTOP ABS**


</dt> <dd>

Siempre en la parte superior, ocultar automáticamente desactivado

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**\_Ocultar automáticamente ABS**


</dt> <dd>

Ocultar automáticamente en, siempre en la parte superior

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS \_ AutoHide \| ABS \_ ALWAYSONTOP**


</dt> <dd>

Ocultar automáticamente y siempre visible en

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

 




