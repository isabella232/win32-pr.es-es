---
title: Código de notificación de TTN_SHOW (commctrl. h)
description: Notifica a la ventana propietaria que un control de información sobre herramientas está a punto de mostrarse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16acb41d1145c176799dd7997b56a850bb45ece7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996460"
---
# <a name="ttn_show-notification-code"></a>TTN \_ Mostrar código de notificación

Notifica a la ventana propietaria que un control de información sobre herramientas está a punto de mostrarse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

[Versión 4,70](common-control-versions.md). Para mostrar la información sobre herramientas en su ubicación predeterminada, devuelva cero. Para personalizar la posición de la información sobre herramientas, cambie la posición de la ventana de información sobre herramientas con la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) y devuelva **true**.

> [!Note]  
> En el caso de las versiones anteriores a 4,70, no hay ningún valor devuelto.

 

## <a name="remarks"></a>Observaciones

Un rectángulo de la ventana de información sobre herramientas es algo más grande que su rectángulo de presentación de texto y su origen está desplazado hacia arriba y hacia la izquierda. Si necesita colocar con precisión el rectángulo de presentación de texto de una información sobre herramientas, el mensaje [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) convierte un rectángulo de presentación de texto en el rectángulo de la ventana de información sobre herramientas correspondiente y viceversa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

