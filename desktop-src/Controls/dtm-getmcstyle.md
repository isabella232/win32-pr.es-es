---
title: DTM_GETMCSTYLE mensaje (Commctrl.h)
description: Obtiene el estilo de un control selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro \_ DateTime GetMonthCalStyle.
ms.assetid: 8983898f-e23a-4247-838c-56364f695429
keywords:
- DTM_GETMCSTYLE controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_GETMCSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639c573f8a49b0ea2dd4b313b11620fa7fa4bed6c158b85fef3afffcee03bf3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878095"
---
# <a name="dtm_getmcstyle-message"></a>Mensaje \_ GETMCSTYLE de DTM

Obtiene el estilo de un control selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro [**\_ DateTime GetMonthCalStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el valor de estilo del control. Para obtener más información, vea [Estilos de control de calendario mensual.](month-calendar-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





