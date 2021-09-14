---
title: MCM_GETCURRENTVIEW mensaje (Commctrl.h)
description: Obtiene la vista actual del calendario. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- MCM_GETCURRENTVIEW controles de Windows mensaje
topic_type:
- apiref
api_name:
- MCM_GETCURRENTVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eebbd6a2b33043294b64b8b65308520b52dbe449
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362559"
---
# <a name="mcm_getcurrentview-message"></a>Mensaje \_ GETCURRENTVIEW de MCM

Obtiene la vista actual del calendario. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetCurrentView.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Vista actual. Uno de los siguientes valores.



| Código devuelto                                                                                  | Descripción              |
|----------------------------------------------------------------------------------------------|--------------------------|
| <dl> <dt>**MCMV \_ MONTH**</dt> </dl>   | Vista mensual.<br/> |
| <dl> <dt>**MCMV \_ YEAR**</dt> </dl>    | Vista anual.<br/>  |
| <dl> <dt>**MCMV \_ DECADE**</dt> </dl>  | Vista de década.<br/>  |
| <dl> <dt>**MCMV \_ CENTURY**</dt> </dl> | Vista del siglo.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





