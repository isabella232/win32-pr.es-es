---
title: Mensaje de DTM_SETSYSTEMTIME (commctrl. h)
description: Establece la hora en un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la macro SetSystemtime de fecha y hora \_ .
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- DTM_SETSYSTEMTIME controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b2a3c625ad4ff02bed138a8086ca0da984de35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996864"
---
# <a name="dtm_setsystemtime-message"></a>DTM \_ SETSYSTEMTIME

Establece la hora en un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetSystemtime de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica la acción que se debe realizar. Este valor debe establecerse en uno de los siguientes valores:



| Value                                                                                                                                             | Significado                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <dt>**GDT \_ válido**</dt> </dl> | Establezca el control de DTP según los datos de la estructura a la que se dirige *lParam* . <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <dt>**GDT \_ ninguno**</dt> </dl>    | Establezca el control de DTP en "sin fecha" y desactive su casilla. Cuando se especifica esta marca, se omite *lParam* . Esta marca solo se aplica a los controles de DTP que se establecen en el estilo [**\_ SHOWNONE de DTS**](date-and-time-picker-control-styles.md) . <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contiene la hora del sistema utilizada para establecer el control de DTP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

