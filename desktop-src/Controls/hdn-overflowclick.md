---
title: Código de notificación de HDN_OVERFLOWCLICK (commctrl. h)
description: Lo envía un control de encabezado a su elemento primario cuando se hace clic en el botón de desbordamiento del encabezado. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- HDN_OVERFLOWCLICK controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905293"
---
# <a name="hdn_overflowclick-notification-code"></a>Código de notificación de OVERFLOWCLICK de HDN \_

Lo envía un control de encabezado a su elemento primario cuando se hace clic en el botón de desbordamiento del encabezado. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* \[ de\]
</dt> <dd>

Puntero a una estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que describe el código de notificación. El proceso de llamada es responsable de la asignación de esta estructura, incluida la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenida. Establezca los miembros de la estructura **NMHDR** , incluido el miembro de *código* que se debe establecer en HDN \_ OVERFLOWCLICK.

Establezca el miembro **iItem** de la estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) en el índice del primer elemento de encabezado que no esté visible y, por lo tanto, debería mostrarse en un desbordamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El receptor de notificaciones convierte **lParam** para recuperar la estructura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) . **WParam** contiene el identificador del control que envía la notificación.

Este mensaje se envía solo cuando se establece el [**\_ desbordamiento de HDS**](header-control-styles.md) de estilo en el control de encabezado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





