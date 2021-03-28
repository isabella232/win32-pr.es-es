---
description: Establece el tamaño y la posición de la pantalla de un control Appbar.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: Mensaje de ABM_SETPOS (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6886249f42638745ca038aa1f216ddc995f0e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540595"
---
# <a name="abm_setpos-message"></a>ABN \_ SETPOS

Establece el tamaño y la posición de la pantalla de un control Appbar. El mensaje especifica un borde de pantalla y el rectángulo delimitador del Appbar. El sistema puede ajustar el rectángulo delimitador para que el Appbar no interfiera con la barra de tareas de Windows ni con ningún otro appbars.


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . El miembro **uEdge** especifica un borde de pantalla y el miembro **RC** contiene el rectángulo delimitador. Cuando la función [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) devuelve, **RC** contiene el rectángulo delimitador aprobado. Debe especificar los miembros **cbSize**, **hWnd**, **uEdge** y **RC** al enviar este mensaje. se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **true**.

## <a name="remarks"></a>Observaciones

Este mensaje hace que el sistema envíe el mensaje de notificación [**ABN \_ POSCHANGED**](abn-poschanged.md) a todos los appbars.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

 




