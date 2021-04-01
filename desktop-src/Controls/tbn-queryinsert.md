---
title: Código de notificación de TBN_QUERYINSERT (commctrl. h)
description: Notifica a la ventana primaria de la barra de herramientas si se puede insertar un botón a la izquierda del botón especificado mientras el usuario está personalizando una barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997025"
---
# <a name="tbn_queryinsert-notification-code"></a>Código de notificación de QUERYINSERT de TBN \_

Notifica a la ventana primaria de la barra de herramientas si se puede insertar un botón a la izquierda del botón especificado mientras el usuario está personalizando una barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . El miembro **iItem** contiene el índice basado en cero del botón que se va a insertar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva **true** para permitir que un botón se inserte delante del botón especificado o **false** para impedir que se inserte el botón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





