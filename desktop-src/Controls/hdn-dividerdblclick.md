---
title: Código de notificación de HDN_DIVIDERDBLCLICK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario hizo doble clic en el área de división del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- HDN_DIVIDERDBLCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129096139a4d698f25de543a2628b473bfd66e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079784"
---
# <a name="hdn_dividerdblclick-notification-code"></a>Código de notificación de DIVIDERDBLCLICK de HDN \_

Notifica a la ventana primaria de un control de encabezado que el usuario hizo doble clic en el área de división del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento cuyo divisor se hizo doble clic.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ DIVIDERDBLCLICKW** (Unicode) y **HDN \_ DIVIDERDBLCLICKA** (ANSI)<br/>   |



 

 





