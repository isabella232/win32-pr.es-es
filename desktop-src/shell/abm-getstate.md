---
description: Recupera los Estados de ocultación y siempre visible de la barra de tareas de Windows.
title: Mensaje de ABM_GETSTATE (ShellAPI. h)
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
ms.openlocfilehash: 71225cd8d93de09a07cb0049066e52be08c18a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360173"
---
# <a name="abm_getstate-message"></a>ABN \_ GETSTATE

Recupera los Estados de ocultación y siempre visible de la barra de tareas de Windows.


```C++
uState = (UINT) SHAppBarMessage(ABM_GETSTATE, pabd);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Debe especificar el miembro **cbSize** al enviar este mensaje. se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si la barra de tareas no está en el estado de ocultar automáticamente ni siempre visible. De lo contrario, el valor devuelto es uno de los siguientes:



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
<td>La barra de tareas está en el estado siempre visible. <br/>
<blockquote>
[!Note]<br />
A partir de Windows 7, ya no se devuelve ABS_ALWAYSONTOP porque la barra de tareas siempre está en ese estado. El código anterior debe actualizarse para omitir la ausencia de este valor en no suponer que el valor devuelto para significa que la barra de tareas no está en el estado siempre visible.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>ABS_AUTOHIDE</strong></dt> </dl></td>
<td>La barra de tareas se encuentra en el estado de ocultar automáticamente.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

 




