---
title: TrackBar
description: Esta sección contiene información sobre los elementos de programación que se utilizan con los controles TrackBar.
ms.assetid: vs|controls|~\controls\trackbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe8e58cd8db9c2811f31cac92ee3d1d31c2c02d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656279"
---
# <a name="trackbar"></a>TrackBar

Esta sección contiene información sobre los elementos de programación que se utilizan con los controles TrackBar.

### <a name="overviews"></a>Temas de introducción



| Tema                                                  | Contenido                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los controles TrackBar](trackbar-controls.md)       | Una barra de desplazamiento es una ventana que contiene un control deslizante (a veces denominado control de posición) en un canal y marcas de graduación opcionales. Cuando el usuario mueve el control deslizante, con el mouse o con las teclas de dirección, la barra de desplazamiento envía mensajes de notificación para indicar el cambio.<br/> |
| [Usar controles TrackBar](using-trackbar-controls.md) | En esta sección se proporcionan detalles y ejemplos de implementación de los controles TrackBar.<br/>                                                                                                                                                                               |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                 | Contenido                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TBM \_ CLEARSEL**](tbm-clearsel.md)                 | Borra el intervalo de selección actual en una barra de nivel. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ CLEARTICS**](tbm-cleartics.md)               | Quita las marcas de graduación actuales de una barra de aumento. Este mensaje no quita la primera y última marca de graduación, creadas automáticamente por la barra de aumento. <br/>                                                                                                                                           |
| [**TBM \_ GETBUDDY**](tbm-getbuddy.md)                 | Recupera el identificador de una ventana relacionada del control TrackBar en una ubicación determinada. La ubicación especificada es relativa a la orientación del control (horizontal o vertical). <br/>                                                                                                                                 |
| [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md)     | Recupera el tamaño y la posición del rectángulo delimitador del canal de una barra de posición. (El canal es el área sobre la que se mueve el control deslizante. Contiene el resaltado cuando se selecciona un intervalo). <br/>                                                                                                         |
| [**TBM \_ GETLINESIZE**](tbm-getlinesize.md)           | Recupera el número de posiciones lógicas que el control deslizante de la barra de desplazamiento se mueve en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo. <br/>                                         |
| [**TBM \_ GETNUMTICS**](tbm-getnumtics.md)             | Recupera el número de marcas de graduación en una barra de aumento. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)           | Recupera el número de posiciones lógicas que el control deslizante de la barra de desplazamiento se mueve en respuesta a la entrada del teclado, como las teclas o, o la entrada del mouse, como los clics en el canal de la barra de desplazamiento. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo. <br/>   |
| [**TBM \_ GETPOS**](tbm-getpos.md)                     | Recupera la posición lógica actual del control deslizante en una barra de desplazamiento. Las posiciones lógicas son los valores enteros en el intervalo de la barra de desplazamiento mínimo al máximo. <br/>                                                                                                                       |
| [**TBM \_ GETPTICS**](tbm-getptics.md)                 | Recupera la dirección de una matriz que contiene las posiciones de las marcas de paso de una barra de aumento. <br/>                                                                                                                                                                                                        |
| [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md)           | Recupera la posición máxima del control deslizante en una barra de desplazamiento. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md)           | Recupera la posición mínima del control deslizante en una barra de desplazamiento. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETSELEND**](tbm-getselend.md)               | Recupera la posición final del intervalo de selección actual en una barra de nivel. <br/>                                                                                                                                                                                                                            |
| [**TBM \_ GETSELSTART**](tbm-getselstart.md)           | Recupera la posición inicial del intervalo de selección actual en una barra de inicio. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)     | Recupera la longitud del control deslizante en una barra de desplazamiento. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md)         | Recupera el tamaño y la posición del rectángulo delimitador del control deslizante en una barra de desplazamiento. <br/>                                                                                                                                                                                                                |
| [**TBM \_ GETTIC**](tbm-gettic.md)                     | Recupera la posición lógica de una marca de graduación en una barra de aumento. La posición lógica puede ser cualquiera de los valores enteros en el intervalo de la barra de desplazamiento mínimo y máximo de posiciones de control deslizante. <br/>                                                                                                                     |
| [**TBM \_ GETTICPOS**](tbm-getticpos.md)               | Recupera la posición física actual de una marca de graduación en una barra de aumento.<br/>                                                                                                                                                                                                                                   |
| [**TBM \_ GETTOOLTIPS**](tbm-gettooltips.md)           | Recupera el identificador del control de información sobre herramientas asignado a TrackBar, si existe. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md) | Recupera la marca del formato de caracteres Unicode para el control. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ SETBUDDY**](tbm-setbuddy.md)                 | Asigna una ventana como la ventana relacionada para un control TrackBar. Las ventanas de amigos de la barra de desplazamiento se muestran automáticamente en una ubicación relativa a la orientación del control (horizontal o vertical). <br/>                                                                                                          |
| [**TBM \_ SETLINESIZE**](tbm-setlinesize.md)           | Establece el número de posiciones lógicas que se mueve el control deslizante de la barra de desplazamiento en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo. <br/>                                              |
| [**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)           | Establece el número de posiciones lógicas que se mueve el control deslizante de la barra de desplazamiento en respuesta a la entrada del teclado, como las teclas o, o la entrada del mouse, como los clics en el canal de la barra de desplazamiento. Las posiciones lógicas son los incrementos enteros en el intervalo de la barra de desplazamiento mínimo al máximo. <br/>        |
| [**TBM \_ SETPOS**](tbm-setpos.md)                     | Establece la posición lógica actual del control deslizante en una barra de desplazamiento. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETPOSNOTIFY**](tbm-setposnotify.md)         | Establece la posición lógica actual del control deslizante en una barra de desplazamiento. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SetRange**](tbm-setrange.md)                 | Establece el intervalo de posiciones lógicas mínima y máxima para el control deslizante en una barra de desplazamiento. <br/>                                                                                                                                                                                                                  |
| [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)           | Establece la posición lógica máxima para el control deslizante en una barra de desplazamiento. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)           | Establece la posición lógica mínima para el control deslizante en una barra de desplazamiento. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETSEL**](tbm-setsel.md)                     | Establece las posiciones inicial y final para el intervalo de selección disponible en una barra de inicio. <br/>                                                                                                                                                                                                                |
| [**TBM \_ SETSELEND**](tbm-setselend.md)               | Establece la posición lógica final del intervalo de selección actual en una barra de nivel. Este mensaje se omite si TrackBar no tiene el estilo [**\_ ENABLESELRANGE de TBS**](trackbar-control-styles.md) . <br/>                                                                              |
| [**TBM \_ SETSELSTART**](tbm-setselstart.md)           | Establece la posición lógica inicial del intervalo de selección actual en una barra de inicio. Este mensaje se omite si TrackBar no tiene el estilo [**\_ ENABLESELRANGE de TBS**](trackbar-control-styles.md) . <br/>                                                                            |
| [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md)     | Establece la longitud del control deslizante en una barra de desplazamiento. Este mensaje se omite si TrackBar no tiene el estilo [**\_ FIXEDLENGTH de TBS**](trackbar-control-styles.md) . <br/>                                                                                                                      |
| [**TBM \_ SETTIC**](tbm-settic.md)                     | Establece una marca de graduación en una barra de aumento en la posición lógica especificada. <br/>                                                                                                                                                                                                                                      |
| [**TBM \_ SETTICFREQ**](tbm-setticfreq.md)             | Establece la frecuencia de intervalo para las marcas de graduación en una barra de aumento. Por ejemplo, si la frecuencia se establece en dos, se muestra una marca de graduación para cada incremento en el intervalo de la barra de aumento. El valor predeterminado de la frecuencia es uno; es decir, cada incremento del intervalo está asociado a una marca de graduación. <br/> |
| [**TBM \_ SETTIPSIDE**](tbm-settipside.md)             | Coloca un control ToolTip utilizado por un control TrackBar. Los controles de barra de control que usan el estilo [**\_ información**](trackbar-control-styles.md) sobre herramientas de TBS muestran información sobre herramientas. <br/>                                                                                                                           |
| [**TBM \_ SETTOOLTIPS**](tbm-settooltips.md)           | Asigna un control ToolTip a un control TrackBar. <br/>                                                                                                                                                                                                                                                       |
| [**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md) | Establece la marca del formato de caracteres Unicode para el control. Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control. <br/>                                                                                                               |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                              | Contenido                                                                                                                                                                                      |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (TrackBar)](nm-customdraw-trackbar.md)            | Enviado por un control TrackBar para notificar a sus ventanas principales las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/>        |
| [NM \_ RELEASEDCAPTURE (TrackBar)](nm-releasedcapture-trackbar-.md) | Notifica a la ventana primaria de un control TrackBar que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) . <br/> |
| [TRBN \_ THUMBPOSCHANGING](trbn-thumbposchanging.md)                | Notifica que la posición del control en una barra de desplazamiento está cambiando. Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .<br/>                               |



 

### <a name="constants"></a>Constantes



| Tema                                                  | Contenido                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Valores de dibujo personalizados](custom-draw-values.md)           | En esta sección se enumeran los valores que se usan para identificar las partes de un control TrackBar. <br/>      |
| [Estilos del control TrackBar](trackbar-control-styles.md) | Esta sección contiene información sobre los estilos usados con los controles TrackBar. <br/> |



 

 

 





