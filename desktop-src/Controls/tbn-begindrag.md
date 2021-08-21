---
title: TBN_BEGINDRAG de notificación (Commctrl.h)
description: Notifica a la ventana primaria de una barra de herramientas que el usuario ha empezado a arrastrar un botón en una barra de herramientas. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 244406e5-e13d-4c80-81fa-81b018b29ec1
keywords:
- TBN_BEGINDRAG código de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5283b2853709742713f79afb761cc39739f6df7467a1de869c545c705c8488ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077979"
---
# <a name="tbn_begindrag-notification-code"></a>Código de notificación \_ BEGINDRAG de TBN

Notifica a la ventana primaria de una barra de herramientas que el usuario ha empezado a arrastrar un botón en una barra de herramientas. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_BEGINDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMTOOLBAR.**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) El **miembro iItem** contiene el identificador de comando del botón que se está arrastrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





