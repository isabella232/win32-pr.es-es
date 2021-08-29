---
description: Recupera el rectángulo delimitador de la Windows de tareas.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: ABM_GETTASKBARPOS mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ea826756ea083996ec6de9218cdacad3b99a6aad50d52d5da67fc1908e8efca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884865"
---
# <a name="abm_gettaskbarpos-message"></a>Mensaje \_ GETTASKBARPOS de ABM

Recupera el rectángulo delimitador de la Windows de tareas.


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) cuyo **miembro rc** recibe el rectángulo delimitador, en coordenadas de pantalla, de la barra de tareas. Debe especificar **cbSize al** enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente; de lo contrario, **FALSE**.

## <a name="remarks"></a>Comentarios

Tenga en cuenta que esto solo se aplica a la barra de tareas del sistema. También pueden estar presentes otros objetos, especialmente las barras de herramientas proporcionadas con software de terceros. Como resultado, es posible que parte del área de pantalla que no está cubierta por la barra de Windows de tareas no sea visible para el usuario. Para recuperar el área de la pantalla no cubierta por la barra de tareas y otras barras de aplicaciones del área de trabajo disponible para la aplicación, use la [**función GetMonitorInfo.**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

