---
title: Código de notificación de HDN_ITEMKEYDOWN (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que se ha presionado una tecla con un elemento seleccionado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- HDN_ITEMKEYDOWN controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079757"
---
# <a name="hdn_itemkeydown-notification-code"></a>Código de notificación de ITEMKEYDOWN de HDN \_

Notifica a la ventana primaria de un control de encabezado que se ha presionado una tecla con un elemento seleccionado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información adicional sobre la tecla que se va a presionar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





