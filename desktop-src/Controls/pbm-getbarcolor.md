---
title: PBM_GETBARCOLOR mensaje (Commctrl.h)
description: Obtiene el color de la barra de progreso.
ms.assetid: d046f7e4-e21e-4dd9-a7be-2bf820c3c492
keywords:
- PBM_GETBARCOLOR controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_GETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb42d878840ad05f0854ec7ca9cb50dc1b3be2a55b3b65ddf652d961b6d818b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119312445"
---
# <a name="pbm_getbarcolor-message"></a>Mensaje \_ GETBARCOLOR de PBM

Obtiene el color de la barra de progreso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el color de la barra de progreso.

## <a name="remarks"></a>Comentarios

Este es el color establecido por el [**mensaje \_ SETBARCOLOR de PBM.**](pbm-setbarcolor.md) El valor predeterminado es CLR \_ DEFAULT, que se define en commctrl.h.

Esta función solo afecta al modo clásico, no a ningún estilo visual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





