---
title: MCM_SETCURRENTVIEW mensaje (Commctrl.h)
description: Establece la vista actual del calendario. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ SetCurrentView.
ms.assetid: 26ccbb80-0dba-4241-a2eb-b79000fc3618
keywords:
- MCM_SETCURRENTVIEW controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_SETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33cf7206fb7e778c0ab7d28ee8947b9327e8cc98bd8ae8c9063213814676a77e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019043"
---
# <a name="mcm_setcurrentview-message"></a>Mensaje \_ SETCURRENTVIEW de MCM

Establece la vista actual del calendario. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ SetCurrentView.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcurrentview)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Nueva vista. Una de las siguientes constantes.



| Value                                                                                                                                                      | Significado                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="MCMV_MONTH"></span><span id="mcmv_month"></span><dl> <dt>**MES DE \_ MCMV**</dt> </dl>       | Vista mensual.<br/> |
| <span id="MCMV_YEAR"></span><span id="mcmv_year"></span><dl> <dt>**MCMV \_ YEAR**</dt> </dl>          | Vista anual.<br/>  |
| <span id="MCMV_DECADE"></span><span id="mcmv_decade"></span><dl> <dt>**MCMV \_ DECADE**</dt> </dl>    | Vista de década.<br/>  |
| <span id="MCMV_CENTURY"></span><span id="mcmv_century"></span><dl> <dt>**MCMV \_ CENTURY**</dt> </dl> | Vista del siglo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





