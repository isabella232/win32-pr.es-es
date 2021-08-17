---
title: HDN_ITEMSTATEICONCLICK mensaje (Commctrl.h)
description: Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el icono de estado de un elemento. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: a1969579-3a69-49ff-b06e-4b7450146a92
keywords:
- HDN_ITEMSTATEICONCLICK controles de Windows mensaje
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
ms.openlocfilehash: cba2e475ec3037ab00c379cf0c9ea371d5a336b80458c68e974a7122d9a2427a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435255"
---
# <a name="hdn_itemstateiconclick-message"></a>Mensaje \_ ITEMSTATEICONCLICK de HDN

Notifica a la ventana primaria de un control de encabezado que el usuario hizo clic en el icono de estado de un elemento. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





