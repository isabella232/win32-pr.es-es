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
ms.openlocfilehash: 72cfa7325d1a8e1eab27383d7df918c8896933bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166389"
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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





