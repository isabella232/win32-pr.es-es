---
title: Mensaje de HDN_ITEMSTATEICONCLICK (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el icono de estado de un elemento. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- HDN_ITEMSTATEICONCLICK controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMSTATEICONCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e5e162b78c829e60494f6e8ff81af3ca97eee4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493054"
---
# <a name="hdn_itemstateiconclick-message"></a>HDN \_ ITEMSTATEICONCLICK

Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el icono de estado de un elemento. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
HDN_ITEMSTATEICONCLICK

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información adicional sobre el icono de estado en el que se hizo clic.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





