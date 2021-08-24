---
title: MCM_HITTEST mensaje (Commctrl.h)
description: Determina qué parte de un control de calendario mensual se encuentra en un punto determinado de la pantalla. Puede enviar este mensaje explícitamente o mediante la macro MonthCal \_ HitTest.
ms.assetid: 51e74b07-4ed7-488d-ad5d-116f046577fc
keywords:
- MCM_HITTEST controles de Windows mensaje
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
ms.openlocfilehash: 3ab43ae76a2e747ff019a5bafa32870a208851a143ad94dd0679e894366c3592
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697195"
---
# <a name="mcm_hittest-message"></a>Mensaje \_ DE MCM HITTEST

Determina qué parte de un control de calendario mensual se encuentra en un punto determinado de la pantalla. Puede enviar este mensaje explícitamente o mediante la macro [**MonthCal \_ HitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura MCHITTESTINFO.**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) Al enviar el mensaje, el **miembro cbSize** debe establecerse en el tamaño de la estructura **MCHITTESTINFO** y **pt** debe establecerse en el punto en el que desea realizar la prueba de acceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Establece los valores de los miembros de



| Código devuelto                                                                                           | Descripción                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CALENDARIO \_ MCHT**</dt> </dl>         | El punto dado estaba dentro del calendario.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**MCHT \_ CALENDARBK**</dt> </dl>       | El punto dado estaba en segundo plano del calendario.<br/>                                                                                                                                                                                                              |
| <dl> <dt>**MCHT \_ CALENDARDATE**</dt> </dl>     | El punto dado estaba en una fecha determinada dentro del calendario. La [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en *lParam->st* se establece en la fecha en el punto dado.<br/>                                                                                    |
| <dl> <dt>**MCHT \_ CALENDARDATENEXT**</dt> </dl> | El punto dado superó una fecha del mes siguiente (se muestra parcialmente al final del mes mostrado actualmente). Si el usuario hace clic aquí, el calendario mensual se desplazará hasta el siguiente mes o conjunto de meses.<br/>                                 |
| <dl> <dt>**MCHT \_ CALENDARDATEPREV**</dt> </dl> | El punto dado superó una fecha del mes anterior (se muestra parcialmente al final del mes mostrado actualmente). Si el usuario hace clic aquí, el calendario mensual se desplazará hasta el mes anterior o el conjunto de meses.<br/>                         |
| <dl> <dt>**MCHT \_ CALENDARDAY**</dt> </dl>      | El punto dado era una abreviatura de día ("Fri", por ejemplo). La [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en *lParam->st* se establece en la fecha correspondiente de la fila superior.<br/>                                                                      |
| <dl> <dt>**MWEEK \_ CALENDARWEEKNUM**</dt> </dl>  | El punto dado era más de un número de semana [**(solo \_ estilo MCS WEEKNUMBERS).**](month-calendar-control-styles.md) La [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en *lParam->st* se establece en la fecha correspondiente en la columna situada más a la izquierda.<br/> |
| <dl> <dt>**MCHT \_ NEXT**</dt> </dl>             | El punto dado está en un área que hará que el calendario mensual se desplace hasta el mes o conjunto de meses siguiente. Esta marca se usa para modificar otras marcas de prueba de acceso.<br/>                                                                                   |
| <dl> <dt>**MCHT \_ LEAL**</dt> </dl>          | El punto dado no estaba en el control de calendario mensual o estaba en una parte inactiva del control.<br/>                                                                                                                                                        |
| <dl> <dt>**MCHT \_ PREV**</dt> </dl>             | El punto dado se encuentra en un área que hará que el calendario mensual se desplace hasta el mes anterior o conjunto de meses. Esta marca se usa para modificar otras marcas de prueba de acceso.<br/>                                                                               |
| <dl> <dt>**TÍTULO \_ DE MCHT**</dt> </dl>            | El punto dado era más de un mes de título.<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**MCHT \_ TITLEBK**</dt> </dl>          | El punto dado estaba sobre el fondo del título de un mes.<br/>                                                                                                                                                                                                    |
| <dl> <dt>**MCHT \_ TITLEBTNNEXT**</dt> </dl>     | El punto dado estaba sobre el botón situado en la esquina superior derecha del control. Si el usuario hace clic aquí, el calendario mensual se desplazará hasta el siguiente mes o conjunto de meses. <br/>                                                                           |
| <dl> <dt>**MCHT \_ TITLEBTNPREV**</dt> </dl>     | El punto dado estaba sobre el botón situado en la esquina superior izquierda del control. Si el usuario hace clic aquí, el calendario mensual se desplazará hasta el mes anterior o el conjunto de meses. <br/>                                                                        |
| <dl> <dt>**MCHT \_ TITLEMONTH**</dt> </dl>       | El punto dado estaba en la barra de título de un mes, más de un nombre de mes.<br/>                                                                                                                                                                                                 |
| <dl> <dt>**MCHT \_ TITLEYEAR**</dt> </dl>        | El punto dado estaba en la barra de título de un mes, a lo largo del valor de año.<br/>                                                                                                                                                                                               |
| <dl> <dt>**MCHT \_ TODAYLINK**</dt> </dl>        | El punto dado estaba en el vínculo "hoy" en la parte inferior del control de calendario del mes.<br/> El **miembro uHit** de la [**estructura MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) en *lParam* será igual al valor devuelto. <br/>                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

