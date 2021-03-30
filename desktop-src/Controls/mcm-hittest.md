---
title: Mensaje de MCM_HITTEST (commctrl. h)
description: Determina qué parte de un control de calendario mensual se encuentra en un punto determinado de la pantalla. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ HitTest.
ms.assetid: 51e74b07-4ed7-488d-ad5d-116f046577fc
keywords:
- MCM_HITTEST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- MCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3670ac8ab663ceda1786f7136a50c4da255a76c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801364"
---
# <a name="mcm_hittest-message"></a>Mensaje de MCM \_ HITTEST

Determina qué parte de un control de calendario mensual se encuentra en un punto determinado de la pantalla. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) . Tras enviar el mensaje, el miembro **cbSize** debe establecerse en el tamaño de la estructura **MCHITTESTINFO** y **PT** debe establecerse en el punto en el que desea realizar la prueba de posicionamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Establece valores en los miembros del



| Código devuelto                                                                                           | Descripción                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_calendario MCHT**</dt> </dl>         | El punto especificado se encontraba en el calendario.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**MCHT \_ CALENDARBK**</dt> </dl>       | El punto especificado estaba en el fondo del calendario.<br/>                                                                                                                                                                                                              |
| <dl> <dt>**MCHT \_ CALENDARDATE**</dt> </dl>     | El punto especificado se encontraba en una fecha determinada del calendario. La estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) de *lParam->St* está establecida en la fecha en el punto especificado.<br/>                                                                                    |
| <dl> <dt>**MCHT \_ CALENDARDATENEXT**</dt> </dl> | El punto especificado se encontraba en una fecha del mes siguiente (que se muestra parcialmente al final del mes que se muestra actualmente). Si el usuario hace clic aquí, el calendario mensual desplazará su presentación al mes o al conjunto de meses siguiente.<br/>                                 |
| <dl> <dt>**MCHT \_ CALENDARDATEPREV**</dt> </dl> | El punto especificado se encontraba en una fecha del mes anterior (mostrado parcialmente al final del mes que se muestra actualmente). Si el usuario hace clic aquí, el calendario mensual desplazará su presentación al mes o al conjunto de meses anterior.<br/>                         |
| <dl> <dt>**MCHT \_ CALENDARDAY**</dt> </dl>      | El punto especificado se encontraba en una abreviatura de día ("vie", por ejemplo). La estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) de *lParam->St* está establecida en la fecha correspondiente en la fila superior.<br/>                                                                      |
| <dl> <dt>**MCHT \_ CALENDARWEEKNUM**</dt> </dl>  | El punto especificado se encontraba en un número de semana (solo en el estilo [**MCS \_ WEEKNUMBERS**](month-calendar-control-styles.md) ). La estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) de *lParam->St* está establecida en la fecha correspondiente en la columna situada más a la izquierda.<br/> |
| <dl> <dt>**MCHT \_ siguiente**</dt> </dl>             | El punto especificado se encuentra en un área que hará que el calendario mensual desplace su presentación al mes o al conjunto de meses siguiente. Esta marca se utiliza para modificar otras marcas de prueba de posicionamiento.<br/>                                                                                   |
| <dl> <dt>**MCHT en \_ ninguna**</dt> </dl>          | El punto especificado no se encontraba en el control de calendario mensual o estaba en una parte inactiva del control.<br/>                                                                                                                                                        |
| <dl> <dt>**MCHT \_ ANT**</dt> </dl>             | El punto especificado se encuentra en un área que hará que el calendario mensual desplace su presentación al mes o al conjunto de meses anterior. Esta marca se utiliza para modificar otras marcas de prueba de posicionamiento.<br/>                                                                               |
| <dl> <dt>**título de MCHT \_**</dt> </dl>            | El punto especificado se encontraba en el título de un mes.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**MCHT \_ TITLEBK**</dt> </dl>          | El punto especificado se encontraba en el fondo del título de un mes.<br/>                                                                                                                                                                                                    |
| <dl> <dt>**MCHT \_ TITLEBTNNEXT**</dt> </dl>     | El punto especificado se encontraba sobre el botón situado en la esquina superior derecha del control. Si el usuario hace clic aquí, el calendario mensual desplazará su presentación al mes o al conjunto de meses siguiente. <br/>                                                                           |
| <dl> <dt>**MCHT \_ TITLEBTNPREV**</dt> </dl>     | El punto especificado se encontraba sobre el botón situado en la esquina superior izquierda del control. Si el usuario hace clic aquí, el calendario mensual desplazará su presentación al mes o al conjunto de meses anterior. <br/>                                                                        |
| <dl> <dt>**MCHT \_ TITLEMONTH**</dt> </dl>       | El punto especificado se encontraba en la barra de título de un mes, en el nombre de un mes.<br/>                                                                                                                                                                                                 |
| <dl> <dt>**MCHT \_ TITLEYEAR**</dt> </dl>        | El punto especificado se encontraba en la barra de título de un mes, en el valor de año.<br/>                                                                                                                                                                                               |
| <dl> <dt>**MCHT \_ TODAYLINK**</dt> </dl>        | El punto especificado se encontraba en el vínculo "hoy" situado en la parte inferior del control de calendario mensual.<br/> El miembro **uHit** de la estructura [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) de *lParam* será igual al valor devuelto. <br/>                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

