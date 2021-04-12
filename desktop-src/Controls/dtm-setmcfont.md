---
title: Mensaje de DTM_SETMCFONT (commctrl. h)
description: Establece la fuente que va a usar el control de calendario mensual del control de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la macro SetMonthCalFont de fecha y hora \_ .
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- DTM_SETMCFONT controles de mensajes de Windows
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
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491824"
---
# <a name="dtm_setmcfont-message"></a>DTM \_ SETMCFONT

Establece la fuente que va a usar el control de calendario mensual del control de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetMonthCalFont de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la fuente que se va a establecer.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica si el control debe volver a dibujarse inmediatamente después de establecer la fuente. Establecer este parámetro en **true** hace que el control se vuelva a dibujar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto para este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





