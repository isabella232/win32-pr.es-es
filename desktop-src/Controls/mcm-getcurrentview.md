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
ms.openlocfilehash: 50f7fce3c1a22ec14ec34e849bd2e3fc4634118b11613913da4e6fae0b9b7b51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319685"
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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





