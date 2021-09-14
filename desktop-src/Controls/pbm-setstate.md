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
ms.openlocfilehash: 5c91e94bcc909957264eff776e56d3580b2c36ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167738"
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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





