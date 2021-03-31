---
title: Código de notificación de TBN_BEGINADJUST (commctrl. h)
description: Notifica a la ventana primaria de una barra de herramientas que el usuario ha empezado a personalizar una barra de herramientas. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 689aeda3-5051-4422-9e66-64557b263943
keywords:
- TBN_BEGINADJUST controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TBN_BEGINADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4708cd205461e3117432cec25e0e4256a6b0d87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905105"
---
# <a name="tbn_beginadjust-notification-code"></a>Código de notificación de BEGINADJUST de TBN \_

Notifica a la ventana primaria de una barra de herramientas que el usuario ha empezado a personalizar una barra de herramientas. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TBN_BEGINADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene información sobre el código de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





