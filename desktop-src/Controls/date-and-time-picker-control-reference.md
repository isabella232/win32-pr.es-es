---
title: Selector de fecha y hora
description: Esta sección contiene información sobre los elementos de API usados con controles de selector de fecha y hora.
ms.assetid: vs|controls|~\controls\datetime\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b29aa1bf7552b87f18a9ded05b67fc8e47770c01431af4da897f2b9733
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929485"
---
# <a name="date-and-time-picker"></a>Selector de fecha y hora

Esta sección contiene información sobre los elementos de API usados con controles de selector de fecha y hora.

### <a name="overviews"></a>Temas de introducción



| Tema                                                                    | Contenido                                                                                                                                                     |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los controles selectores de fecha y hora](date-and-time-picker-controls.md) | Un control selector de fecha y hora *(DTP)* proporciona una interfaz sencilla e intuitiva a través de la cual intercambiar información de fecha y hora con un usuario.<br/> |
| [Usar controles selectores de fecha y hora](using-date-and-time-picker.md)    | En esta sección se proporciona información y código de ejemplo para implementar controles de selector de fecha y hora. <br/>                                                |



 

### <a name="macros"></a>Macros



| Tema                                                                     | Contenido                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DateTime \_ CloseMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)                 | Cierra el control selector de fecha y hora (DTP). Use esta macro o envíe el [**mensaje DTM \_ CLOSEMONTHCAL**](dtm-closemonthcal.md) explícitamente.<br/>                                                                                                                     |
| [**DateTime \_ GetDateTimePickerInfo**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getdatetimepickerinfo) | Obtiene información para un control de selector de fecha y hora (DTP) especificado.<br/>                                                                                                                                                                                              |
| [**DateTime \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)                   | Obtiene el tamaño necesario para mostrar el control sin recorte. Use esta macro o envíe el [**mensaje \_ GETIDEALSIZE**](dtm-getidealsize.md) de DTM explícitamente.<br/>                                                                                                        |
| [**DateTime \_ GetMonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal)                     | Obtiene el identificador del control de calendario del mes secundario del selector de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**\_ GETMONTHCAL**](dtm-getmonthcal.md) de DTM explícitamente. <br/>                                                                               |
| [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor)           | Obtiene el color de una parte determinada del calendario mensual dentro de un control selector de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**\_ GETMCCOLOR de DTM**](dtm-getmccolor.md) explícitamente. <br/>                                                           |
| [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont)             | Obtiene la fuente que está usando actualmente el control de calendario del mes secundario del selector de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**\_ GETMCFONT de DTM**](dtm-getmcfont.md) explícitamente. <br/>                                                      |
| [**DateTime \_ GetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)           | Obtiene el estilo de un control DTP especificado. Use esta macro o envíe el [**mensaje \_ GETMCSTYLE de DTM**](dtm-getmcstyle.md) explícitamente.<br/>                                                                                                                               |
| [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange)                           | Obtiene las horas del sistema mínimas y máximas permitidos actuales para un control selector de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**\_ GETRANGE de DTM**](dtm-getrange.md) explícitamente. <br/>                                                              |
| [**DateTime \_ GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime)                 | Obtiene la hora seleccionada actualmente de un control selector de fecha y hora (DTP) y la coloca en una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) especificada. Puede usar esta macro o enviar el mensaje [**\_ GETSYSTEMTIME de DTM**](dtm-getsystemtime.md) explícitamente. <br/> |
| [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat)                         | Establece la presentación de un control selector de fecha y hora (DTP) basado en una cadena de formato determinada. Puede usar esta macro o enviar el mensaje [**\_ SETFORMAT de DTM**](dtm-setformat.md) explícitamente. <br/>                                                                          |
| [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor)           | Establece el color de una parte determinada del calendario mensual dentro de un control selector de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**\_ SETMCCOLOR**](dtm-setmccolor.md) de DTM explícitamente. <br/>                                                           |
| [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)             | Establece la fuente que va a usar el control de calendario del mes secundario del selector de fecha y hora (DTP). Puede usar esta macro o enviar explícitamente el [**mensaje \_ SETMCFONT de DTM.**](dtm-setmcfont.md) <br/>                                                                |
| [**DateTime \_ SetMonthCalStyle**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)           | Establece el estilo de un control DTP especificado. Use esta macro o envíe el [**mensaje \_ SETMCSTYLE**](dtm-setmcstyle.md) de DTM explícitamente.<br/>                                                                                                                              |
| [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange)                           | Establece las horas del sistema mínimas y máximas permitidos para un control selector de fecha y hora (DTP). Puede usar esta macro o enviar el mensaje [**\_ SETRANGE de DTM**](dtm-setrange.md) explícitamente. <br/>                                                                       |
| [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime)                 | Establece un control selector de fecha y hora (DTP) en una fecha y hora determinadas. Puede usar esta macro o enviar el mensaje [**\_ SETSYSTEMTIME**](dtm-setsystemtime.md) de DTM explícitamente. <br/>                                                                                       |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                           | Contenido                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DTM \_ CLOSEMONTHCAL**](dtm-closemonthcal.md)                 | Cierra un control DTP. Envíe este mensaje explícitamente o mediante la macro [**DateTime \_ CloseMonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal)<br/>                                                                                                                                        |
| [**DTM \_ GETDATETIMEPICKERINFO**](dtm-getdatetimepickerinfo.md) | Obtiene información sobre un control selector de fecha y hora (DTP).<br/>                                                                                                                                                                                                                  |
| [**DTM \_ GETIDEALSIZE**](dtm-getidealsize.md)                   | Obtiene el tamaño necesario para mostrar el control sin recorte. Envíe este mensaje explícitamente o mediante la macro [**DateTime \_ GetIdealSize.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getidealsize)<br/>                                                                                                  |
| [**DTM \_ GETMCCOLOR**](dtm-getmccolor.md)                       | Obtiene el color de una parte determinada del calendario mensual dentro de un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**\_ DateTime GetMonthCalColor.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) <br/>                                              |
| [**DTM \_ GETMCFONT**](dtm-getmcfont.md)                         | Obtiene la fuente que está usando actualmente el control de calendario del mes secundario del selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**\_ DateTime GetMonthCalFont.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) <br/>                                         |
| [**DTM \_ GETMCSTYLE**](dtm-getmcstyle.md)                       | Obtiene el estilo de un control DTP. Envíe este mensaje explícitamente o mediante la macro [**\_ DateTime GetMonthCalStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalstyle)<br/>                                                                                                                       |
| [**DTM \_ GETMONTHCAL**](dtm-getmonthcal.md)                     | Obtiene el identificador del control de calendario del mes secundario del selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**\_ DateTime GetMonthCal.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcal) <br/>                                                                              |
| [**DTM \_ GETRANGE**](dtm-getrange.md)                           | Obtiene las horas del sistema mínimas y máximas permitidos actuales para un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ GetRange.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) <br/>                                                              |
| [**DTM \_ GETSYSTEMTIME**](dtm-getsystemtime.md)                 | Obtiene la hora seleccionada actualmente de un control selector de fecha y hora (DTP) y la coloca en una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) especificada. Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ GetSystemtime.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) <br/> |
| [**DTM \_ SETFORMAT**](dtm-setformat.md)                         | Establece la presentación de un control selector de fecha y hora (DTP) basado en una cadena de formato determinada. Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ SetFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) <br/>                                                                         |
| [**DTM \_ SETMCCOLOR**](dtm-setmccolor.md)                       | Establece el color de una parte determinada del calendario mensual dentro de un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**\_ DateTime SetMonthCalColor.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) <br/>                                              |
| [**DTM \_ SETMCFONT**](dtm-setmcfont.md)                         | Establece la fuente que va a usar el control de calendario del mes secundario del selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**\_ DateTime SetMonthCalFont.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont)<br/>                                                    |
| [**DTM \_ SETMCSTYLE**](dtm-setmcstyle.md)                       | Establece el estilo de un control DTP. Envíe este mensaje explícitamente o mediante la macro [**\_ DateTime SetMonthCalStyle.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalstyle)<br/>                                                                                                                       |
| [**DTM \_ SETRANGE**](dtm-setrange.md)                           | Establece las horas del sistema mínimas y máximas permitidos para un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ SetRange.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) <br/>                                                                      |
| [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md)                 | Establece la hora en un control selector de fecha y hora (DTP). Puede enviar este mensaje explícitamente o usar la macro [**DateTime \_ SetSystemtime.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) <br/>                                                                                                   |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                   | Contenido                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CIERRE DE \_ DTN](dtn-closeup.md)                         | Enviado por un control selector de fecha y hora (DTP) cuando el usuario cierra el calendario de mes desplegable. El calendario mensual se cierra cuando el usuario elige una fecha del calendario mensual o hace clic en la flecha desplegable mientras el calendario está abierto. <br/>                                                                                                      |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md)           | Enviado por un control selector de fecha y hora (DTP) cada vez que se produce un cambio. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                                                                                  |
| [LISTA DESPLEGABLE DE DTN \_](dtn-dropdown.md)                       | Enviado por un control de selector de fecha y hora (DTP) cuando el usuario activa el calendario de mes desplegable. <br/>                                                                                                                                                                                                                                               |
| [FORMATO \_ DTN](dtn-format.md)                           | Enviado por un control selector de fecha y hora (DTP) para solicitar que el texto se muestre en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                                                       |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)                 | Enviado por un control selector de fecha y hora (DTP) para recuperar el tamaño máximo permitido de la cadena que se mostrará en un campo de devolución de llamada. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                           |
| [DTN \_ USERSTRING](dtn-userstring.md)                   | Enviado por un control selector de fecha y hora (DTP) cuando un usuario termina de editar una cadena en el control. Este código de notificación solo lo envían los controles DTP que están establecidos en el estilo [**\_ APPCANPARSE de DTS.**](date-and-time-picker-control-styles.md) Este mensaje se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)                     | Enviado por un control selector de fecha y hora (DTP) cuando el usuario tipos en un campo de devolución de llamada. Este mensaje se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                                                                             |
| [NM \_ KILLFOCUS (fecha y hora)](nm-killfocus-date-time.md) | Notifica a la ventana primaria de un control selector de fecha y hora que el control ha perdido el foco de entrada. [**NM \_ KILLFOCUS (fecha y hora)**](nm-killfocus-date-time.md) se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                 |
| [NM \_ SETFOCUS (fecha y hora)](nm-setfocus-date-time-.md)  | Notifica a la ventana primaria de un control selector de fecha y hora que el control ha recibido el foco de entrada. [NM \_ SETFOCUS (fecha y hora)](nm-setfocus-date-time-.md) se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                  |



 

### <a name="structures"></a>Estructuras



| Tema                                                  | Contenido                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATETIMEPICKERINFO**](/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo)       | Contiene información sobre un control DTP. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange)           | Contiene información sobre un cambio que ha tenido lugar en un control selector de fecha y hora (DTP). Esta estructura se usa con el código [de notificación \_ DATETIMECHANGE de DTN.](dtn-datetimechange.md) <br/>                                                                                                                                                                                     |
| [**NMDATETIMEFORMAT**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformata)           | Contiene información sobre una parte de la cadena de formato que define un campo de devolución de llamada dentro de un control selector de fecha y hora (DTP). Lleva la subcadena que define el campo de devolución de llamada y contiene un búfer para recibir la cadena que se mostrará en el campo de devolución de llamada. Esta estructura se usa con el código [de notificación \_ DTN FORMAT.](dtn-format.md) <br/>               |
| [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) | Contiene información sobre un campo de devolución de llamada de control selector de fecha y hora (DTP). Contiene una subcadena (tomada de la cadena de formato del control) que define un campo de devolución de llamada. La estructura recibe el tamaño máximo permitido del texto que se mostrará en el campo de devolución de llamada. Esta estructura se usa con el código [de notificación \_ FORMATQUERY de DTN.](dtn-formatquery.md) <br/> |
| [**NMDATETIMESTRING**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimestringa)           | Contiene información específica de una operación de edición que ha tenido lugar en un control selector de fecha y hora (DTP). Este mensaje se usa con el código [de notificación \_ USERSTRING de DTN.](dtn-userstring.md) <br/>                                                                                                                                                                                |
| [**NMDATETIMEWMKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimewmkeydowna)     | Contiene información utilizada para describir y controlar un [código de notificación \_ WMKEYDOWN de DTN.](dtn-wmkeydown.md) <br/>                                                                                                                                                                                                                                                                               |



 

### <a name="constants"></a>Constantes



| Tema                                                                          | Contenido                                                                                |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Estilos de control selector de fecha y hora](date-and-time-picker-control-styles.md) | Los estilos de ventana enumerados aquí son específicos de los controles selectores de fecha y hora.<br/> |



 

 

