---
title: Código de notificación de RBN_MINMAX (commctrl. h)
description: Se envía por un control rebar antes de maximizar o minimizar una banda. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- RBN_MINMAX controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658219"
---
# <a name="rbn_minmax-notification-code"></a>Código de notificación de MinMax de RBN \_

Se envía por un control rebar antes de maximizar o minimizar una banda. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .


```C++
RBN_MINMAX
```



## <a name="parameters"></a>Parámetros

Este código de notificación no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero para evitar que la operación tenga lugar, cero para permitir que continúe.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





