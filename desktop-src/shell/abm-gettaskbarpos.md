---
description: Recupera el rectángulo delimitador de la barra de tareas de Windows.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: Mensaje de ABM_GETTASKBARPOS (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540598"
---
# <a name="abm_gettaskbarpos-message"></a>ABN \_ GETTASKBARPOS

Recupera el rectángulo delimitador de la barra de tareas de Windows.


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) cuyo miembro **RC** recibe el rectángulo delimitador, en coordenadas de pantalla, de la barra de tareas. Debe especificar el **cbSize** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true si es** correcto; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

Tenga en cuenta que esto solo se aplica a la barra de tareas del sistema. También pueden estar presentes otros objetos, especialmente las barras de herramientas que se proporcionan con software de terceros. Como resultado, es posible que parte del área de pantalla no incluida en la barra de tareas de Windows no esté visible para el usuario. Para recuperar el área de la pantalla que no está incluida en la barra de tareas y en otras barras de la aplicación, use la función [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

