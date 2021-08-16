---
title: PBM_SETBARCOLOR mensaje (Commctrl.h)
description: Establece el color de la barra indicadora de progreso en el control de barra de progreso.
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- PBM_SETBARCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babff5ad74d943d64f5ad61354447498e91e1325c99c82b32183fbc62eabafdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830206"
---
# <a name="pbm_setbarcolor-message"></a>Mensaje \_ SETBARCOLOR de PBM

Establece el color de la barra indicadora de progreso en el control de barra de progreso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **COLORREF que** especifica el nuevo color de la barra del indicador de progreso. La especificación del valor DEFAULT de CLR hace que la barra de progreso use su color de barra de \_ indicador de progreso predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de la barra del indicador de progreso anterior o CLR DEFAULT si el color de la barra del \_ indicador de progreso es el color predeterminado.

## <a name="remarks"></a>Comentarios

Cuando los estilos visuales están habilitados, este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





