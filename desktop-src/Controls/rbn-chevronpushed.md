---
title: RBN_CHEVRONPUSHED de notificación (Commctrl.h)
description: Enviado por un control rebar cuando se inserta un botón de contenido adicional. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- RBN_CHEVRONPUSHED código de notificación Windows controles
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f5f8d52558251524e9d978c52ae703565a9641febdd53190925cfb8b127160
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985325"
---
# <a name="rbn_chevronpushed-notification-code"></a>Código de notificación \_ RBN CHEVRONPUSHED

Enviado por un control rebar cuando se inserta un botón de contenido adicional. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a la estructura [**NMREBARCHEVRON de la**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) banda.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para esta notificación.

## <a name="remarks"></a>Comentarios

Cuando una aplicación recibe este código de notificación, es responsable de mostrar un menú emergente con elementos para cada herramienta oculta. Use el **miembro rc** de la [**estructura NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) para encontrar la posición correcta para el menú emergente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





