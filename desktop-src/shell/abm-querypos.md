---
description: Solicita un tamaño y una posición de pantalla para una barra de aplicaciones.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: ABM_QUERYPOS mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363198"
---
# <a name="abm_querypos-message"></a>Mensaje de ABM \_ QUERYPOS

Solicita un tamaño y una posición de pantalla para una barra de aplicaciones. Cuando se realiza la solicitud, el mensaje propone un borde de pantalla y un rectángulo delimitador para la barra de aplicaciones. El sistema ajusta el rectángulo delimitador para que la barra de aplicaciones no interfiera con la Windows de tareas ni con ninguna otra barra de aplicaciones.


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) El **miembro uEdge** especifica un borde de la pantalla y el miembro **rc** contiene el rectángulo delimitador propuesto. Cuando se [**devuelve la función SHAppBarMessage,**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) **rc** contiene el rectángulo delimitador aprobado. Debe especificar los **miembros cbSize**, **hWnd,** **uEdge** y **rc** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **TRUE.**

## <a name="remarks"></a>Observaciones

Una barra de aplicaciones debe enviar este mensaje antes de enviar el [**mensaje \_ setpos de ABM.**](abm-setpos.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




