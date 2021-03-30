---
title: Selector de fecha y hora
description: Esta sección contiene información sobre los elementos de la API que se usan con los controles de selector de fecha y hora.
ms.assetid: vs|controls|~\controls\datetime\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4e91b325b798ff465d8048cac2f0a9a72e5774
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904863"
---
# <a name="date-and-time-picker"></a>Selector de fecha y hora

Esta sección contiene información sobre los elementos de la API que se usan con los controles de selector de fecha y hora.

### <a name="overviews"></a>Temas de introducción



| Tema                                                                    | Contenido                                                                                                                                                     |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los controles de selector de fecha y hora](date-and-time-picker-controls.md) | Un *control selector de fecha y hora (DTP)* proporciona una interfaz sencilla e intuitiva a través de la cual se va a intercambiar información de fecha y hora con un usuario.<br/> |
| [Usar controles de selector de fecha y hora](using-date-and-time-picker.md)    | En esta sección se proporciona información y código de ejemplo para implementar controles de selector de fecha y hora. <br/>                                                |



 

### <a name="macros"></a>Macros



| Tema                                                                     | Contenido                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_CloseMonthCal DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)                 | Cierra el control selector de fecha y hora (DTP). Use esta macro o envíe el [**mensaje \_ CLOSEMONTHCAL de DTM**](dtm-closemonthcal.md) explícitamente.<br/>                                                                                                                     |
| [**\_GetDateTimePickerInfo DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getdatetimepickerinfo) | Obtiene información para un control de selector de fecha y hora (DTP) especificado.<br/>                                                                                                                                                                                              |
| [**\_GetIdealSize DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)                   | Obtiene el tamaño necesario para mostrar el control sin recorte. Use esta macro o envíe el [**mensaje \_ GETIDEALSIZE de DTM**](dtm-getidealsize.md) explícitamente.<br/>                                                                                                        |
| [**\_GetMonthCal DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal)                     | Obtiene el identificador del control de calendario mensual de un selector de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md) explícitamente. <br/>                                                                               |
| [**\_GetMonthCalColor DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor)           | Obtiene el color para una parte determinada del calendario mensual dentro de un control de selector de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**DTM \_ GETMCCOLOR**](dtm-getmccolor.md) explícitamente. <br/>                                                           |
| [**\_GetMonthCalFont DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)             | Obtiene la fuente que está usando actualmente el control de calendario mensual del control de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**DTM \_ GETMCFONT**](dtm-getmcfont.md) explícitamente. <br/>                                                      |
| [**\_GetMonthCalStyle DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)           | Obtiene el estilo de un control de DTP especificado. Use esta macro o envíe el [**mensaje \_ GETMCSTYLE de DTM**](dtm-getmcstyle.md) explícitamente.<br/>                                                                                                                               |
| [**\_GetRange DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange)                           | Obtiene las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**DTM \_ GETRANGE**](dtm-getrange.md) explícitamente. <br/>                                                              |
| [**Fecha y hora \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime)                 | Obtiene la hora actualmente seleccionada de un control de selector de fecha y hora (DTP) y lo coloca en una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) especificada. Puede usar esta macro o enviar el mensaje [**DTM \_ GETSYSTEMTIME**](dtm-getsystemtime.md) explícitamente. <br/> |
| [**\_SetFormat DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)                         | Establece la presentación de un control de selector de fecha y hora (DTP) basándose en una cadena de formato determinada. Puede usar esta macro o enviar el mensaje [**DTM \_ SETFORMAT**](dtm-setformat.md) explícitamente. <br/>                                                                          |
| [**\_SetMonthCalColor DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor)           | Establece el color de una parte determinada del calendario mensual dentro de un control de selector de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**DTM \_ SETMCCOLOR**](dtm-setmccolor.md) explícitamente. <br/>                                                           |
| [**\_SetMonthCalFont DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)             | Establece la fuente que va a usar el control de calendario mensual del control de fecha y hora (DTP). Puede usar esta macro o enviar explícitamente el mensaje [**DTM \_ SETMCFONT**](dtm-setmcfont.md) . <br/>                                                                |
| [**\_SetMonthCalStyle DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)           | Establece el estilo para un control de DTP especificado. Use esta macro o envíe el [**mensaje \_ SETMCSTYLE de DTM**](dtm-setmcstyle.md) explícitamente.<br/>                                                                                                                              |
| [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange)                           | Establece las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**DTM \_ SetRange**](dtm-setrange.md) explícitamente. <br/>                                                                       |
| [**\_SetSystemtime DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)                 | Establece un control de selector de fecha y hora (DTP) en una fecha y hora determinadas. Puede usar esta macro o enviar el mensaje [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) explícitamente. <br/>                                                                                       |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                           | Contenido                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DTM \_ CLOSEMONTHCAL**](dtm-closemonthcal.md)                 | Cierra un control de DTP. Envíe este mensaje explícitamente o mediante la [**macro \_ CloseMonthCal de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .<br/>                                                                                                                                        |
| [**DTM \_ GETDATETIMEPICKERINFO**](dtm-getdatetimepickerinfo.md) | Obtiene información sobre un control de selector de fecha y hora (DTP).<br/>                                                                                                                                                                                                                  |
| [**DTM \_ GETIDEALSIZE**](dtm-getidealsize.md)                   | Obtiene el tamaño necesario para mostrar el control sin recorte. Envíe este mensaje explícitamente o mediante la [**macro \_ GetIdealSize de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize) .<br/>                                                                                                  |
| [**DTM \_ GETMCCOLOR**](dtm-getmccolor.md)                       | Obtiene el color para una parte determinada del calendario mensual dentro de un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetMonthCalColor de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) . <br/>                                              |
| [**DTM \_ GETMCFONT**](dtm-getmcfont.md)                         | Obtiene la fuente que está usando actualmente el control de calendario mensual del control de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetMonthCalFont de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) . <br/>                                         |
| [**DTM \_ GETMCSTYLE**](dtm-getmcstyle.md)                       | Obtiene el estilo de un control de DTP. Envíe este mensaje explícitamente o mediante la [**macro \_ GetMonthCalStyle de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle) .<br/>                                                                                                                       |
| [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)                     | Obtiene el identificador del control de calendario mensual de un selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetMonthCal de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) . <br/>                                                                              |
| [**DTM \_ GETRANGE**](dtm-getrange.md)                           | Obtiene las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetRange de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) . <br/>                                                              |
| [**DTM \_ GETSYSTEMTIME**](dtm-getsystemtime.md)                 | Obtiene la hora actualmente seleccionada de un control de selector de fecha y hora (DTP) y lo coloca en una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) especificada. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetSystemtime de DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) . <br/> |
| [**DTM \_ SETFORMAT**](dtm-setformat.md)                         | Establece la presentación de un control de selector de fecha y hora (DTP) basándose en una cadena de formato determinada. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetFormat de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) . <br/>                                                                         |
| [**DTM \_ SETMCCOLOR**](dtm-setmccolor.md)                       | Establece el color de una parte determinada del calendario mensual dentro de un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetMonthCalColor de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) . <br/>                                              |
| [**DTM \_ SETMCFONT**](dtm-setmcfont.md)                         | Establece la fuente que va a usar el control de calendario mensual del control de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetMonthCalFont de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .<br/>                                                    |
| [**DTM \_ SETMCSTYLE**](dtm-setmcstyle.md)                       | Establece el estilo de un control de DTP. Envíe este mensaje explícitamente o mediante la [**macro \_ SetMonthCalStyle de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle) .<br/>                                                                                                                       |
| [**DTM \_ SetRange**](dtm-setrange.md)                           | Establece las horas de sistema mínimas y máximas permitidas para un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) . <br/>                                                                      |
| [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md)                 | Establece la hora en un control de selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetSystemtime de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) . <br/>                                                                                                   |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                   | Contenido                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DTN \_ primer plano](dtn-closeup.md)                         | Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario cierra el calendario del mes desplegable. El calendario mensual se cierra cuando el usuario elige una fecha en el calendario mensual o hace clic en la flecha desplegable mientras el calendario está abierto. <br/>                                                                                                      |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md)           | Se envía mediante un control de selector de fecha y hora (DTP) cada vez que se produce un cambio. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                                                                                  |
| [\_lista desplegable DTN](dtn-dropdown.md)                       | Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario activa el calendario del mes desplegable. <br/>                                                                                                                                                                                                                                               |
| [\_formato DTN](dtn-format.md)                           | Enviado por un control de selector de fecha y hora (DTP) para solicitar el texto que se va a mostrar en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                                                       |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)                 | Enviado por un control de selector de fecha y hora (DTP) para recuperar el tamaño máximo permitido de la cadena que se mostrará en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                           |
| [DTN \_ USERSTRING](dtn-userstring.md)                   | Se envía mediante un control de selector de fecha y hora (DTP) cuando un usuario termina de editar una cadena en el control. Este código de notificación solo lo envían los controles de DTP que se establecen en el estilo [**\_ APPCANPARSE de DTS**](date-and-time-picker-control-styles.md) . Este mensaje se envía en forma de un mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/> |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)                     | Se envía mediante un control de selector de fecha y hora (DTP) cuando el usuario escribe en un campo de devolución de llamada. Este mensaje se envía en forma de un mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                                                                             |
| [NM \_ KILLFOCUS (fecha y hora)](nm-killfocus-date-time.md) | Notifica a la ventana primaria de un control de fecha y hora que el control ha perdido el foco de entrada. [**Nm \_ KILLFOCUS (fecha y hora)**](nm-killfocus-date-time.md) se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                 |
| [NM \_ SETFOCUS (fecha y hora)](nm-setfocus-date-time-.md)  | Notifica a la ventana primaria de un control de fecha y hora que el control ha recibido el foco de entrada. [Nm \_ SETFOCUS (fecha y hora)](nm-setfocus-date-time-.md) se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                  |



 

### <a name="structures"></a>Estructuras



| Tema                                                  | Contenido                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATETIMEPICKERINFO**](/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo)       | Contiene información sobre un control de DTP. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange)           | Contiene información sobre un cambio que se ha producido en un control de selector de fecha y hora (DTP). Esta estructura se usa con el código de notificación [ \_ DATETIMECHANGE de DTN](dtn-datetimechange.md) . <br/>                                                                                                                                                                                     |
| [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata)           | Contiene información sobre una parte de la cadena de formato que define un campo de devolución de llamada en un control de selector de fecha y hora (DTP). Incluye la subcadena que define el campo de devolución de llamada y contiene un búfer para recibir la cadena que se mostrará en el campo de devolución de llamada. Esta estructura se usa con el código de notificación de [ \_ formato DTN](dtn-format.md) . <br/>               |
| [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) | Contiene información sobre un campo de devolución de llamada del control selector de fecha y hora (DTP). Contiene una subcadena (tomada de la cadena de formato del control) que define un campo de devolución de llamada. La estructura recibe el tamaño máximo permitido del texto que se mostrará en el campo de devolución de llamada. Esta estructura se usa con el código de notificación de [DTN \_ FORMATQUERY](dtn-formatquery.md) . <br/> |
| [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa)           | Contiene información específica de una operación de edición que ha tenido lugar en un control de selector de fecha y hora (DTP). Este mensaje se usa con el código de notificación de [DTN \_ USERSTRING](dtn-userstring.md) . <br/>                                                                                                                                                                                |
| [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna)     | Incluye información que se usa para describir y controlar un código de notificación [ \_ WMKEYDOWN de DTN](dtn-wmkeydown.md) . <br/>                                                                                                                                                                                                                                                                               |



 

### <a name="constants"></a>Constantes



| Tema                                                                          | Contenido                                                                                |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Estilos de control de selector de fecha y hora](date-and-time-picker-control-styles.md) | Los estilos de ventana que se enumeran aquí son específicos de los controles de selector de fecha y hora.<br/> |



 

 

