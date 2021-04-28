---
title: NM_NCHITTEST de notificación (Commctrl.h)
description: 'NM_NCHITTEST de notificación: se envía mediante un control rebar cuando el control recibe un mensaje \_ WM NCHITTEST. Este código de notificación se envía en forma de mensaje WM \_ NOTIFY.'
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST código de notificación controles de Windows
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
ms.openlocfilehash: 68ede0ac017fbe5146cd68e51e2a38c7f66c7898
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112323"
---
# <a name="nm_nchittest-notification-code"></a>Código de \_ notificación de NM NCHITTEST

Enviado por un control rebar cuando el control recibe un [**mensaje \_ WM NCHITTEST.**](/windows/desktop/inputdev/wm-nchittest) Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contiene información sobre el código de notificación. El *miembro pt* contiene las coordenadas del mouse del mensaje de la prueba de impacto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

A menos que se especifique lo contrario, devuelva cero para permitir que el control realice el procesamiento predeterminado del mensaje de la prueba de acceso o devuelva uno de los valores ht documentados en \* [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) para invalidar el procesamiento predeterminado de la prueba de acceso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

