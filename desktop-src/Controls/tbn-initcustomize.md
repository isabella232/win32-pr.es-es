---
title: TBN_INITCUSTOMIZE de notificación (Commctrl.h)
description: Notifica a la ventana primaria de una barra de herramientas que se ha iniciado la personalización. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- TBN_INITCUSTOMIZE de notificación Windows controles
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbf66e9974e444fd8544e20cb4878e662bb94b4b1f958404794783e52664c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876615"
---
# <a name="tbn_initcustomize-notification-code"></a>Código de notificación \_ INITCUSTOMIZE de TBN

Notifica a la ventana primaria de una barra de herramientas que se ha iniciado la personalización. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) de la barra de herramientas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve TBNRF \_ HIDEHELP para suprimir el botón Ayuda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





