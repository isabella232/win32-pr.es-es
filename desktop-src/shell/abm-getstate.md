---
description: Recupera los estados autohide y always-on-top de la Windows de tareas.
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
ms.openlocfilehash: 1ced01e3f8186a82e99f408f91546ebcbb117ed9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574581"
---
# <a name="abm_getstate-message"></a>Mensaje \_ GETSTATE de ABM

Recupera los estados autohide y always-on-top de la Windows de tareas.


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




| Código devuelto | Descripción | 
|-------------|-------------|
| <dl><dt><strong>ABS_ALWAYSONTOP</strong></dt></dl> | La barra de tareas está en el estado siempre en la parte superior. <br /><blockquote>[!Note]<br />A partir Windows 7, ABS_ALWAYSONTOP ya no se devuelve porque la barra de tareas siempre está en ese estado. El código anterior debe actualizarse para omitir la ausencia de este valor en no suponer que el valor devuelto significa que la barra de tareas no está en el estado siempre en la parte superior.</blockquote><br /> | 
| <dl><dt><strong>ABS_AUTOHIDE</strong></dt></dl> | La barra de tareas está en estado de autohide.<br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




