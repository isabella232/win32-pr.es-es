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
ms.openlocfilehash: 35586d3483d1d487f740a1a3d991c884c814f452
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167782"
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

## <a name="remarks"></a>Observaciones

Este es el color establecido por el [**mensaje \_ SETBARCOLOR de PBM.**](pbm-setbarcolor.md) El valor predeterminado es CLR \_ DEFAULT, que se define en commctrl.h.

Esta función solo afecta al modo clásico, no a ningún estilo visual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





