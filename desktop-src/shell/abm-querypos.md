---
description: Solicita un tamaño y una posición de pantalla para una barra de aplicaciones.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: ABM_QUERYPOS mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f7a5e78b6b040904144a64e1068fea3a3e56c7b42fdfcf314f2ced4bfff9e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225036"
---
# <a name="abm_querypos-message"></a>Mensaje \_ QUERYPOS de ABM

Solicita un tamaño y una posición de pantalla para una barra de aplicaciones. Cuando se realiza la solicitud, el mensaje propone un borde de pantalla y un rectángulo delimitador para la barra de aplicaciones. El sistema ajusta el rectángulo delimitador para que la barra de aplicaciones no interfiera con la Windows de tareas ni con ninguna otra barra de aplicaciones.


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA.**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) El **miembro uEdge** especifica un borde de pantalla y el **miembro rc** contiene el rectángulo delimitador propuesto. Cuando se [**devuelve la función SHAppBarMessage,**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) **rc** contiene el rectángulo delimitador aprobado. Debe especificar los **miembros cbSize**, **hWnd,** **uEdge** y **rc** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **TRUE.**

## <a name="remarks"></a>Comentarios

Una barra de aplicaciones debe enviar este mensaje antes de enviar el [**mensaje \_ SETPOS de ABM.**](abm-setpos.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




