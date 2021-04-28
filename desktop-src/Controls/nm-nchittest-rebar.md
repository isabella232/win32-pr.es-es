---
title: NM_NCHITTEST de notificación (rebar) (Commctrl.h)
description: 'NM_NCHITTEST de notificación (rebar): enviado por un control rebar cuando el control recibe un mensaje \_ WM NCHITTEST. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.'
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- NM_NCHITTEST de notificación (rebar) Controles de Windows
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7935f1b3e990db55518c9d22537e8fb6db97962
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112333"
---
# <a name="nm_nchittest-rebar-notification-code"></a>Código \_ de notificación de NM NCHITTEST (rebar)

Enviado por un control rebar cuando el control recibe un [**mensaje \_ WM NCHITTEST.**](/windows/desktop/inputdev/wm-nchittest) Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre el código de notificación. El **miembro dwItemSpec** contiene el índice de banda sobre el que se produjo el mensaje de la prueba de impacto, y el miembro **pt** contiene las coordenadas del mouse del mensaje de la prueba de impacto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero para permitir que la barra de rebar realice el procesamiento predeterminado del mensaje de la prueba de acceso o devuelva uno de los valores ht documentados en \* [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) para invalidar el procesamiento predeterminado de la prueba de acceso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

