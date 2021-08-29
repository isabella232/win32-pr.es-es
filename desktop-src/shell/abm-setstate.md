---
description: Establece los estados mostrar automáticamente y siempre en la parte superior de la Windows de tareas.
title: ABM_SETSTATE mensaje (Shellapi.h)
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
ms.openlocfilehash: 1a50671a750f8ca1800cea200c2c58828803bc8a45ae055082c5b6d78959dd12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710875"
---
# <a name="abm_setstate-message"></a>Mensaje \_ SETSTATE de ABM

Establece los estados mostrar automáticamente y siempre en la parte superior de la Windows de tareas.


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Debe especificar los **miembros cbSize** y **hWnd** al enviar este mensaje. Los datos para el estado deseado se envían en el **miembro lParam** mediante uno de los valores siguientes.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Mostrar automáticamente y siempre en la parte superior, ambos desactivados

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS \_ ALWAYSONTOP**


</dt> <dd>

Always-on-top on, autohide off

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS \_ AUTOHIDE**


</dt> <dd>

Autohide on, always-on-top off

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS \_ AUTOHIDE \| ABS \_ ALWAYSONTOP**


</dt> <dd>

Mostrar automáticamente y siempre en la parte superior

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




