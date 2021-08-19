---
title: TBN_DRAGOUT de notificación (Commctrl.h)
description: Enviado por un control de barra de herramientas cuando el usuario hace clic en un botón y, a continuación, mueve el cursor fuera del botón. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- TBN_DRAGOUT código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad707fa357a487e271bbe03039745b97521542a1305f9745a71a56044060c950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077949"
---
# <a name="tbn_dragout-notification-code"></a>Código de notificación DRAGOUT de TBN \_

Enviado por un control de barra de herramientas cuando el usuario hace clic en un botón y, a continuación, mueve el cursor fuera del botón. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) que contiene información sobre este código de notificación. Para este código de notificación, solo son válidos los miembros **hdr** **e iItem** de esta estructura. El **miembro iItem** de esta estructura contiene el identificador de comando del botón que se está arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Comentarios

Este código de notificación permite a una aplicación implementar la funcionalidad de arrastrar y colocar para los botones de la barra de herramientas. Al procesar este código de notificación, la aplicación iniciará la operación de arrastrar y colocar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





