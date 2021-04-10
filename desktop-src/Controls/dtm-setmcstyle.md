---
title: Mensaje de DTM_SETMCSTYLE (commctrl. h)
description: Establece el estilo de un control de selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro SetMonthCalStyle de fecha y hora \_ .
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- DTM_SETMCSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_SETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150672"
---
# <a name="dtm_setmcstyle-message"></a>DTM \_ SETMCSTYLE

Establece el estilo de un control de selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la [**macro \_ SetMonthCalStyle de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>Valor de estilo. Para obtener más información, vea <a href="month-calendar-control-styles.md">estilos de control de calendario mensual</a>.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor del estilo anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





