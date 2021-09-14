---
title: DTM_SETSYSTEMTIME mensaje (Commctrl.h)
description: Establece la hora en un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro DateTime \_ SetSystemtime.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- DTM_SETSYSTEMTIME controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062532"
---
# <a name="dtm_setsystemtime-message"></a>Mensaje DTM \_ SETSYSTEMTIME

Establece la hora en un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ SetSystemtime.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica la acción que se debe realizar. Este valor debe establecerse en uno de los siguientes:



| Value                                                                                                                                             | Significado                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <dt>**GDT \_ VÁLIDO**</dt> </dl> | Establezca el control DTP según los datos de la estructura a la que *apunta lParam.* <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <dt>**GDT \_ NONE**</dt> </dl>    | Establezca el control DTP en "sin fecha" y desactive su casilla. Cuando se especifica esta marca, *se omite lParam.* Esta marca solo se aplica a los controles DTP que están establecidos en el [**estilo \_ DTS SHOWNONE.**](date-and-time-picker-control-styles.md) <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contiene la hora del sistema utilizada para establecer el control DTP.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si se realiza correctamente o cero en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

