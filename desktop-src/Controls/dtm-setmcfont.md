---
title: DTM_SETMCFONT mensaje (Commctrl.h)
description: Establece la fuente que va a usar el control de calendario del mes secundario del selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro DateTime \_ SetMonthCalFont.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- DTM_SETMCFONT controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa1b34c1a51e365868cbdae30e46cd299937d3d6fe33bad6c57d630a0b226fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877815"
---
# <a name="dtm_setmcfont-message"></a>Mensaje \_ SETMCFONT de DTM

Establece la fuente que va a usar el control de calendario del mes secundario del selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ SetMonthCalFont.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la fuente que se establecerá.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica si el control se debe volver a dibujar inmediatamente después de establecer la fuente. Si se establece este parámetro **en TRUE,** el control se vuelve a dibujar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





