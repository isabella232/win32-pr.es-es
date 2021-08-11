---
description: Recupera los estados autohide y always-on-top de la barra de Windows tareas.
title: ABM_GETSTATE mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 18e16752-16be-492b-a4fa-c951e18dc86c
api_name:
- ABM_GETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b1a3618be793f4728dc6184b50b7a4e0e57c3ffd2c4d2cd8acde17372aa031f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225234"
---
# <a name="abm_getstate-message"></a>Mensaje \_ GETSTATE de ABM

Recupera los estados autohide y always-on-top de la barra de Windows tareas.


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) Debe especificar el **miembro cbSize** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si la barra de tareas no está en el estado autohide ni always-on-top. De lo contrario, el valor devuelto es uno o ambos de los siguientes:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código devuelto</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>ABS_ALWAYSONTOP</strong></dt> </dl></td>
<td>La barra de tareas está en estado siempre en la parte superior. <br/>
<blockquote>
[!Note]<br />
A partir Windows 7, ABS_ALWAYSONTOP ya no se devuelve porque la barra de tareas siempre está en ese estado. El código anterior debe actualizarse para omitir la ausencia de este valor en no suponer que el valor devuelto significa que la barra de tareas no está en el estado siempre en la parte superior.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>ABS_AUTOHIDE</strong></dt> </dl></td>
<td>La barra de tareas está en estado de autohide.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




