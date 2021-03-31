---
title: Mensaje de MCM_GETMAXSELCOUNT (commctrl. h)
description: Recupera el intervalo de fechas máximo que se puede seleccionar en un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetMaxSelCount.
ms.assetid: 34204231-3a3c-4eba-913d-b0c27769c338
keywords:
- MCM_GETMAXSELCOUNT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_GETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bddfdad17cc4a0fd6499514023cb499f55f40d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079526"
---
# <a name="mcm_getmaxselcount-message"></a>Mensaje de MCM \_ GETMAXSELCOUNT

Recupera el intervalo de fechas máximo que se puede seleccionar en un control de calendario mensual. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmaxselcount) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor INT que representa el número total de días que se pueden seleccionar para el control.

## <a name="remarks"></a>Observaciones

Puede cambiar el intervalo de fechas máximo que se puede seleccionar mediante el mensaje de [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





