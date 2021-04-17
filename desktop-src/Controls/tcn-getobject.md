---
title: Código de notificación de TCN_GETOBJECT (commctrl. h)
description: Se envía por un control de pestaña cuando tiene el \_ \_ estilo extendido TCS ex REGISTERDROP y se arrastra un objeto sobre un elemento de ficha del control. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 0beddabe-0e97-4fe7-bcf7-adaba0d72dfe
keywords:
- TCN_GETOBJECT controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TCN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e442a122397db717b25e71b17487866227476ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656454"
---
# <a name="tcn_getobject-notification-code"></a>TCN \_ código de notificación GETOBJECT

Se envía por un control de pestaña cuando tiene el estilo extendido [**TCS \_ ex \_ REGISTERDROP**](tab-control-extended-styles.md) y se arrastra un objeto sobre un elemento de ficha del control. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TCN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contiene información sobre el elemento de ficha al que se arrastra el objeto y recibe los datos que devuelve la aplicación en respuesta a este mensaje.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El procesamiento de la aplicación en este código de notificación debe devolver cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





