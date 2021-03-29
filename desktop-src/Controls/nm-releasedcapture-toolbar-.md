---
title: Código de notificación de NM_RELEASEDCAPTURE (barra de herramientas) (commctrl. h)
description: Notifica a la ventana primaria de un control de la barra de herramientas que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 8d9b637c-710e-4337-9466-8616a93d1c44
keywords:
- Código de notificación de NM_RELEASEDCAPTURE (barra de herramientas) controles de Windows
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d915b3af073ba0c6b5c74a7b13317f7b2d4ab8a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150362"
---
# <a name="nm_releasedcapture-toolbar-notification-code"></a>NM \_ RELEASEDCAPTURE (barra de herramientas) código de notificación

Notifica a la ventana primaria de un control de la barra de herramientas que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información adicional sobre esta notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El control omite el valor devuelto de este código de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





