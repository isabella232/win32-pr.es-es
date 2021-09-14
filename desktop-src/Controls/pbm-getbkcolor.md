---
title: PBM_GETBKCOLOR mensaje (Commctrl.h)
description: Obtiene el color de fondo de la barra de progreso.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- PBM_GETBKCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2240025629bbcc242ea7ed47be2e3db42ae73b15
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167781"
---
# <a name="pbm_getbkcolor-message"></a>Mensaje \_ GETBKCOLOR de PBM

Obtiene el color de fondo de la barra de progreso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de fondo de la barra de progreso.

## <a name="remarks"></a>Observaciones

Este es el color establecido por el [**mensaje \_ SETBKCOLOR de PBM.**](pbm-setbkcolor.md) El valor predeterminado es CLR \_ DEFAULT, que se define en commctrl.h.

Esta función solo afecta al modo clásico, no a ningún estilo visual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





