---
title: Código de notificación de LVN_GETEMPTYMARKUP (commctrl. h)
description: Lo envía el control de vista de lista a su ventana primaria cuando el control no tiene elementos. El \_ código de notificación de GETEMPTYMARKUP de LVN es una solicitud para que la ventana primaria proporcione texto de marcado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- LVN_GETEMPTYMARKUP controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905696"
---
# <a name="lvn_getemptymarkup-notification-code"></a>Código de notificación de GETEMPTYMARKUP de LVN \_

Lo envía el control de vista de lista a su ventana primaria cuando el control no tiene elementos. El \_ código de notificación de GETEMPTYMARKUP de LVN es una solicitud para que la ventana primaria proporcione texto de marcado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . Establezca los miembros de esta estructura para proporcionar texto de marcado para el control de vista de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelva **true** para establecer el texto de marcado en el control de vista de lista o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

El receptor de notificaciones convierte *lParam* para recuperar la estructura [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) . El parámetro *wParam* contiene el identificador del control que envía este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





