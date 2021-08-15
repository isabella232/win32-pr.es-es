---
title: TBM_SETPOS mensaje (Commctrl.h)
description: 'TBM_SETPOS mensaje: establece la posición lógica actual del control deslizante en una barra de seguimiento.'
ms.assetid: df6c4e5d-2847-419d-82b5-334d53bb6ba1
keywords:
- TBM_SETPOS controles de Windows mensaje
topic_type:
- apiref
api_name:
- TBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ccd1cb35f8cde672c51baafe5623291e5449f90aa118eb36cb12152fe155385
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078049"
---
# <a name="tbm_setpos-message"></a>Mensaje TBM \_ SETPOS

Establece la posición lógica actual del control deslizante en una barra de seguimiento.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Volver a dibujar la marca. Si este parámetro es **TRUE,** el mensaje vuelve a dibujar el control con el control deslizante en la posición dada por *lParam*. Si este parámetro es **FALSE,** el mensaje no vuelve a dibujar el control deslizante en la nueva posición. Tenga en cuenta que el mensaje establece el valor de la posición del control deslizante (tal como lo devuelve el mensaje [**\_ GETPOS de TBM)**](tbm-getpos.md) independientemente del *parámetro wParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

Nueva posición lógica del control deslizante. Las posiciones lógicas válidas son los valores enteros del intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento. Si este valor está fuera del intervalo máximo y mínimo del control, la posición se establece en el valor máximo o mínimo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





