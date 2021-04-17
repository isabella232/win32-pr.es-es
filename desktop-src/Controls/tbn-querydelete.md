---
title: Código de notificación de TBN_QUERYDELETE (commctrl. h)
description: Notifica a la ventana primaria de la barra de herramientas si se puede eliminar un botón de una barra de herramientas mientras el usuario está personalizando la barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a416545ecf7ad8562c1327160d683a109eccb3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533747"
---
# <a name="tbn_querydelete-notification-code"></a>Código de notificación de QUERYDELETE de TBN \_

Notifica a la ventana primaria de la barra de herramientas si se puede eliminar un botón de una barra de herramientas mientras el usuario está personalizando la barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . El miembro **iItem** contiene el índice basado en cero del botón que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** para permitir que el botón se elimine o **false** para impedir que se elimine el botón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





