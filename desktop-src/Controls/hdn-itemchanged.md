---
title: Código de notificación de HDN_ITEMCHANGED (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que los atributos de un elemento de encabezado han cambiado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ab707010-8ed2-4575-8233-8a1f5656e498
keywords:
- HDN_ITEMCHANGED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGED
- HDN_ITEMCHANGEDA
- HDN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67157ff7f775c124236b7a77a1051b7644758c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078944"
---
# <a name="hdn_itemchanged-notification-code"></a>Código de notificación de HDN \_ ITEMCHANGED

Notifica a la ventana primaria de un control de encabezado que los atributos de un elemento de encabezado han cambiado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
HDN_ITEMCHANGED

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado, incluidos los atributos que han cambiado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ ITEMCHANGEDW** (Unicode) y **HDN \_ ITEMCHANGEDA** (ANSI)<br/>           |



 

 





