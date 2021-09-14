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
ms.openlocfilehash: e3691dfbd62847bc490c3a45e1d640d19b09cca6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892332"
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
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





