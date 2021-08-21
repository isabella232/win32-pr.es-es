---
title: DTN_FORMATQUERY de notificación (Commctrl.h)
description: Enviado por un control selector de fecha y hora (DTP) para recuperar el tamaño máximo permitido de la cadena que se mostrará en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- DTN_FORMATQUERY código de notificación Windows controles
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14bd1a9efe22251aba71f157dfb2a68e2b0a70385c30564bb7f08e420e0c0cb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019993"
---
# <a name="dtn_formatquery-notification-code"></a>Código de notificación \_ DE DTN FORMATQUERY

Enviado por un control selector de fecha y hora (DTP) para recuperar el tamaño máximo permitido de la cadena que se mostrará en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) que contiene información sobre el campo de devolución de llamada. La estructura contiene una subcadena que define un campo de devolución de llamada y recibe el tamaño máximo permitido de la cadena que se mostrará en el campo de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El propietario del control debe calcular el ancho máximo posible del texto que se mostrará en el campo de devolución de llamada, establecer el miembro **szMax** de la estructura [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) y devolver cero.

## <a name="remarks"></a>Comentarios

El control de este código de notificación prepara el control para ajustarse al tamaño máximo de la cadena que se mostrará en un campo de devolución de llamada determinado. Esto permite que el control muestre correctamente la salida en todo momento, lo que reduce el parpadeo dentro de la presentación del control. (Para obtener información adicional sobre los campos de devolución de llamada, vea [Campos de devolución de llamada).](date-and-time-picker-controls.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DTN \_ FORMATQUERYW** (Unicode) y **DTN \_ FORMATQUERYA** (ANSI)<br/>           |



 

 





