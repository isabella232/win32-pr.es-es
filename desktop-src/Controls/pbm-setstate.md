---
title: PBM_SETSTATE mensaje (Commctrl.h)
description: Establece el estado de la barra de progreso.
ms.assetid: 4626f334-db74-4618-8fc7-e6f21c88ca19
keywords:
- PBM_SETSTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_SETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794006517eaa23789f3a25425b1213fede7f8dde9893587def02ebc9605b28f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986065"
---
# <a name="pbm_setstate-message"></a>Mensaje \_ SETSTATE de PBM

Establece el estado de la barra de progreso.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Estado de la barra de progreso que se establece. Uno de los siguientes valores.



| Valor                                                                                                                                                   | Significado                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="PBST_NORMAL"></span><span id="pbst_normal"></span><dl> <dt>**PBST \_ NORMAL**</dt> </dl> | En curso.<br/> |
| <span id="PBST_ERROR"></span><span id="pbst_error"></span><dl> <dt>**PBST \_ ERROR**</dt> </dl>    | Error.<br/>       |
| <span id="PBST_PAUSED"></span><span id="pbst_paused"></span><dl> <dt>**PBST \_ EN PAUSA**</dt> </dl> | En pausa.<br/>      |



 

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el estado anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





