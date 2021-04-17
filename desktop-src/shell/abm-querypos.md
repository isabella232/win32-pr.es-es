---
description: Solicita un tamaño y una posición en la pantalla para un Appbar.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: Mensaje de ABM_QUERYPOS (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360172"
---
# <a name="abm_querypos-message"></a>ABN \_ QUERYPOS

Solicita un tamaño y una posición en la pantalla para un Appbar. Cuando se realiza la solicitud, el mensaje propone un borde de pantalla y un rectángulo delimitador para el Appbar. El sistema ajusta el rectángulo delimitador para que el Appbar no interfiera con la barra de tareas de Windows ni con ningún otro appbars.


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . El miembro **uEdge** especifica un borde de pantalla y el miembro **RC** contiene el rectángulo delimitador propuesto. Cuando la función [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) devuelve, **RC** contiene el rectángulo delimitador aprobado. Debe especificar los miembros **cbSize**, **hWnd**, **uEdge** y **RC** al enviar este mensaje. se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **true**.

## <a name="remarks"></a>Observaciones

Un Appbar debe enviar este mensaje antes de enviar el mensaje [**\_ SETPOS de ABN**](abm-setpos.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

 




