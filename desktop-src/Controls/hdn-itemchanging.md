---
title: Código de notificación de HDN_ITEMCHANGING (commctrl. h)
description: Notifica a la ventana primaria de un control de encabezado que los atributos de un elemento de encabezado están a punto de cambiar. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- HDN_ITEMCHANGING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905032"
---
# <a name="hdn_itemchanging-notification-code"></a>Código de notificación de ITEMCHANGING de HDN \_

Notifica a la ventana primaria de un control de encabezado que los atributos de un elemento de encabezado están a punto de cambiar. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contiene información sobre el control de encabezado y el elemento de encabezado, incluidos los atributos que están a punto de cambiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **false** para permitir los cambios o **true** para evitarlos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **HDN \_ ITEMCHANGINGW** (Unicode) y **HDN \_ ITEMCHANGINGA** (ANSI)<br/>         |



 

 





