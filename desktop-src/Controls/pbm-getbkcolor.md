---
title: Mensaje de PBM_GETBKCOLOR (commctrl. h)
description: Obtiene el color de fondo de la barra de progreso.
ms.assetid: 9526ed78-08d9-468f-831b-72bb7c8c92d1
keywords:
- PBM_GETBKCOLOR controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905424"
---
# <a name="pbm_getbkcolor-message"></a>Mensaje de GETBKCOLOR de PBM \_

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

Este es el color establecido por el mensaje de [**\_ SETBKCOLOR de PBM**](pbm-setbkcolor.md) . El valor predeterminado es CLR \_ predeterminado, que se define en commctrl. h.

Esta función solo afecta al modo clásico, no a cualquier estilo visual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





