---
title: PBM_GETSTATE mensaje (Commctrl.h)
description: Obtiene el estado de la barra de progreso.
ms.assetid: ff240160-7db6-4711-8d4e-25a77dfba118
keywords:
- PBM_GETSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cd157ccb6ab8a1fe4cd4a31bf1f8a033f0e591288338e21cc322a8ac10bfc41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047015"
---
# <a name="pbm_getstate-message"></a>Mensaje \_ GETSTATE de PBM

Obtiene el estado de la barra de progreso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el estado actual de la barra de progreso. Uno de los siguientes valores.



| Código devuelto                                                                                 | Descripción             |
|---------------------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>**PBST \_ NORMAL**</dt> </dl> | En curso.<br/> |
| <dl> <dt>**PBST \_ ERROR**</dt> </dl>  | Error.<br/>       |
| <dl> <dt>**PBST \_ EN PAUSA**</dt> </dl> | En pausa.<br/>      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





