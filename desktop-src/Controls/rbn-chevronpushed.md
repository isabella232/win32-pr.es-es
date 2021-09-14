---
title: RBN_CHEVRONPUSHED de notificación (Commctrl.h)
description: Enviado por un control rebar cuando se inserta un botón de contenido adicional. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- RBN_CHEVRONPUSHED código de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28d992b6d4a617b7aa7ee144eb50aef3b0e834
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167234"
---
# <a name="rbn_chevronpushed-notification-code"></a>Código de notificación \_ RBN CHEVRONPUSHED

Enviado por un control rebar cuando se inserta un botón de contenido adicional. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a la estructura [**NMREBARCHEVRON de la**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="remarks"></a>Observaciones

Cuando una aplicación recibe este código de notificación, es responsable de mostrar un menú emergente con elementos para cada herramienta oculta. Use el **miembro rc** de la [**estructura NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) para encontrar la posición correcta para el menú emergente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





