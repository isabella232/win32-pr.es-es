---
title: Mensaje de MCM_GETCURRENTVIEW (commctrl. h)
description: Obtiene la vista actual del calendario. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ GetCurrentView.
ms.assetid: 9c42ebf6-611e-4e50-9dcc-cf7fd63b32eb
keywords:
- MCM_GETCURRENTVIEW controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492383"
---
# <a name="mcm_getcurrentview-message"></a>Mensaje de MCM \_ GETCURRENTVIEW

Obtiene la vista actual del calendario. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) .

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
| <dl> <dt>**MCMV \_ mes**</dt> </dl>   | Vista mensual.<br/> |
| <dl> <dt>**MCMV \_ año**</dt> </dl>    | Vista anual.<br/>  |
| <dl> <dt>**década de MCMV \_**</dt> </dl>  | Vista de década.<br/>  |
| <dl> <dt>**\_siglo MCMV**</dt> </dl> | Vista de siglo.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





