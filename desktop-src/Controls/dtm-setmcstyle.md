---
title: DTM_SETMCSTYLE mensaje (Commctrl.h)
description: Establece el estilo de un control selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro \_ DateTime SetMonthCalStyle.
ms.assetid: 6b480a1e-c76e-4026-ab2a-5ec53df6fa28
keywords:
- DTM_SETMCSTYLE controles de Windows mensaje
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
ms.openlocfilehash: 2805f2213bcbb1fa91a10ea80005b8b23bbc7447973bba6930bfdcb1e52a9e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877805"
---
# <a name="dtm_setmcstyle-message"></a>Mensaje \_ SETMCSTYLE de DTM

Establece el estilo de un control selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro [**\_ DateTime SetMonthCalStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>Valor de estilo. Para obtener más información, vea <a href="month-calendar-control-styles.md">Estilos de control de calendario mensual.</a></dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor del estilo anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





