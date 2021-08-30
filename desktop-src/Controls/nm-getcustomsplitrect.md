---
title: NM_GETCUSTOMSPLITRECT de notificación (Commctrl.h)
description: Enviado por un control de botón a su elemento primario para obtener medidas para los dos rectángulos del botón de división. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- NM_GETCUSTOMSPLITRECT código de notificación Windows controles
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ab55083b830ef3ba8a0e22250d4048134fdda100bf798a8b567c13c8a949e57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088765"
---
# <a name="nm_getcustomsplitrect-notification-code"></a>Código \_ de notificación NM GETCUSTOMSPLITRECT

Enviado por un control de botón a su elemento primario para obtener medidas para los dos rectángulos del botón de división. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a [**NMCUSTOMSPLITRECTINFO para**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) recibir información de rectángulos delimitadores. La **estructura NMCUSTOMSPLITRECTINFO** se envía con el código de notificación como una solicitud para que el elemento primario proporcione medidas para los rectángulos del botón de división.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md) para que indique al control de botón que use los valores devueltos en la estructura [**NMCUSTOMSPLITRECTINFO; de**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) lo contrario, devuelve [**CDRF \_ DODEFAULT.**](cdrf-constants.md)

## <a name="remarks"></a>Comentarios

Un control de botón envía este código de notificación antes de dibujarlo. El botón debe ser de estilo [**BS \_ SPLITBUTTON**](button-styles.md) o [**BS \_ DEFSPLITBUTTON**](button-styles.md). Si los rectángulos devueltos al control *en lParam* no son válidos, se omiten.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





