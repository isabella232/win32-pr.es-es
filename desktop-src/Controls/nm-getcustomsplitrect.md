---
title: Código de notificación de NM_GETCUSTOMSPLITRECT (commctrl. h)
description: Enviado por un control de botón a su elemento primario para obtener medidas para los dos rectángulos del botón de expansión. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- NM_GETCUSTOMSPLITRECT controles de código de notificación de Windows
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
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149893"
---
# <a name="nm_getcustomsplitrect-notification-code"></a>Código de notificación de NM \_ GETCUSTOMSPLITRECT

Enviado por un control de botón a su elemento primario para obtener medidas para los dos rectángulos del botón de expansión. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Un puntero a un [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) para recibir información de rectángulos delimitadores. La estructura **NMCUSTOMSPLITRECTINFO** se envía con el código de notificación como una solicitud para que el elemento primario proporcione medidas para los rectángulos del botón de expansión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md) para indicar al control de botón que use los valores devueltos en la estructura [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) ; de lo contrario, devuelve [**CDRF de \_ forma predeterminada**](cdrf-constants.md).

## <a name="remarks"></a>Observaciones

Este código de notificación se envía por un control de botón antes de dibujarse. El botón debe tener el estilo [**BS \_ SPLITBUTTON**](button-styles.md) o [**BS \_ DEFSPLITBUTTON**](button-styles.md). Si los rectángulos devueltos al control en *lParam* no son válidos, se omiten.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





