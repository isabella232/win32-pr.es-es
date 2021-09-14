---
title: DTM_GETMCFONT mensaje (Commctrl.h)
description: Obtiene la fuente que está usando actualmente el control de calendario del mes secundario del selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la \_ macro DateTime GetMonthCalFont.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- DTM_GETMCFONT controles de Windows mensaje
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892329"
---
# <a name="dtm_getmcfont-message"></a>Mensaje \_ GETMCFONT de DTM

Obtiene la fuente que está usando actualmente el control de calendario del mes secundario del selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**\_ DateTime GetMonthCalFont.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor HFONT que es el identificador de la fuente actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





