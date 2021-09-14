---
title: Barra de seguimiento
description: Esta sección contiene información sobre los elementos de programación utilizados con controles trackbar.
ms.assetid: vs|controls|~\controls\trackbar\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe8e58cd8db9c2811f31cac92ee3d1d31c2c02d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165990"
---
# <a name="trackbar"></a>Barra de seguimiento

Esta sección contiene información sobre los elementos de programación utilizados con controles trackbar.

### <a name="overviews"></a>Temas de introducción



| Tema                                                  | Contenido                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los controles trackbar](trackbar-controls.md)       | Una barra de seguimiento es una ventana que contiene un control deslizante (a veces denominado thumb) en un canal y marcas de graduación opcionales. Cuando el usuario mueve el control deslizante, con el mouse o las teclas de dirección, la barra de seguimiento envía mensajes de notificación para indicar el cambio.<br/> |
| [Usar controles trackbar](using-trackbar-controls.md) | En esta sección se proporcionan detalles de implementación y ejemplos para los controles trackbar.<br/>                                                                                                                                                                               |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                 | Contenido                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TBM \_ CLEARSEL**](tbm-clearsel.md)                 | Borra el intervalo de selección actual en una barra de seguimiento. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ CLEARTICS**](tbm-cleartics.md)               | Quita las marcas de graduación actuales de una barra de seguimiento. Este mensaje no quita la primera y la última marca de graduación, que la barra de seguimiento crea automáticamente. <br/>                                                                                                                                           |
| [**TBM \_ GETBUDDY**](tbm-getbuddy.md)                 | Recupera el identificador en una ventana de compañeros de control de la barra de seguimiento en una ubicación determinada. La ubicación especificada es relativa a la orientación del control (horizontal o vertical). <br/>                                                                                                                                 |
| [**TBM \_ GETCHANNELRECT**](tbm-getchannelrect.md)     | Recupera el tamaño y la posición del rectángulo delimitador para el canal de una barra de seguimiento. (El canal es el área sobre la que se mueve el control deslizante. Contiene el resaltado cuando se selecciona un intervalo). <br/>                                                                                                         |
| [**TBM \_ GETLINESIZE**](tbm-getlinesize.md)           | Recupera el número de posiciones lógicas que el control deslizante de la barra de seguimiento mueve en respuesta a la entrada del teclado de las teclas de dirección, como las teclas o . Las posiciones lógicas son los incrementos enteros en el intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento. <br/>                                         |
| [**TBM \_ GETNUMTICS**](tbm-getnumtics.md)             | Recupera el número de marcas de graduación de una barra de seguimiento. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)           | Recupera el número de posiciones lógicas que el control deslizante de la barra de seguimiento mueve en respuesta a la entrada del teclado, como las teclas o o la entrada del mouse, como los clics en el canal de la barra de seguimiento. Las posiciones lógicas son los incrementos enteros en el intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento. <br/>   |
| [**TBM \_ GETPOS**](tbm-getpos.md)                     | Recupera la posición lógica actual del control deslizante en una barra de seguimiento. Las posiciones lógicas son los valores enteros del intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento. <br/>                                                                                                                       |
| [**TBM \_ GETPTICS**](tbm-getptics.md)                 | Recupera la dirección de una matriz que contiene las posiciones de las marcas de graduación de una barra de seguimiento. <br/>                                                                                                                                                                                                        |
| [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md)           | Recupera la posición máxima del control deslizante en una barra de seguimiento. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETRANGEMIN**](tbm-getrangemin.md)           | Recupera la posición mínima del control deslizante en una barra de seguimiento. <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ GETSELEND**](tbm-getselend.md)               | Recupera la posición final del intervalo de selección actual en una barra de seguimiento. <br/>                                                                                                                                                                                                                            |
| [**TBM \_ GETSELSTART**](tbm-getselstart.md)           | Recupera la posición inicial del intervalo de selección actual en una barra de seguimiento. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)     | Recupera la longitud del control deslizante en una barra de seguimiento. <br/>                                                                                                                                                                                                                                                      |
| [**TBM \_ GETTHUMBRECT**](tbm-getthumbrect.md)         | Recupera el tamaño y la posición del rectángulo delimitador para el control deslizante en una barra de seguimiento. <br/>                                                                                                                                                                                                                |
| [**TBM \_ GETTIC**](tbm-gettic.md)                     | Recupera la posición lógica de una marca de graduación en una barra de seguimiento. La posición lógica puede ser cualquiera de los valores enteros del intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento. <br/>                                                                                                                     |
| [**TBM \_ GETTICPOS**](tbm-getticpos.md)               | Recupera la posición física actual de una marca de graduación en una barra de seguimiento.<br/>                                                                                                                                                                                                                                   |
| [**TBM \_ GETTOOLTIPS**](tbm-gettooltips.md)           | Recupera el identificador del control de información sobre herramientas asignado a la barra de seguimiento, si lo hay. <br/>                                                                                                                                                                                                                          |
| [**TBM \_ GETUNICODEFORMAT**](tbm-getunicodeformat.md) | Recupera la marca de formato de caracteres Unicode para el control . <br/>                                                                                                                                                                                                                                           |
| [**TBM \_ SETBUDDY**](tbm-setbuddy.md)                 | Asigna una ventana como ventana de compañeros para un control de barra de seguimiento. Las ventanas de compañeros de barra de seguimiento se muestran automáticamente en una ubicación relativa a la orientación del control (horizontal o vertical). <br/>                                                                                                          |
| [**TBM \_ SETLINESIZE**](tbm-setlinesize.md)           | Establece el número de posiciones lógicas que se mueve el control deslizante de la barra de seguimiento en respuesta a la entrada del teclado desde las teclas de dirección, como las teclas o . Las posiciones lógicas son los incrementos enteros en el intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento. <br/>                                              |
| [**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)           | Establece el número de posiciones lógicas que el control deslizante de la barra de seguimiento se mueve en respuesta a la entrada del teclado, como las teclas o o la entrada del mouse, como los clics en el canal de la barra de seguimiento. Las posiciones lógicas son los incrementos enteros en el intervalo de posiciones del control deslizante mínimo a máximo de la barra de seguimiento. <br/>        |
| [**TBM \_ SETPOS**](tbm-setpos.md)                     | Establece la posición lógica actual del control deslizante en una barra de seguimiento. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETPOSNOTIFY**](tbm-setposnotify.md)         | Establece la posición lógica actual del control deslizante en una barra de seguimiento. <br/>                                                                                                                                                                                                                                         |
| [**TBM \_ SETRANGE**](tbm-setrange.md)                 | Establece el intervalo de posiciones lógicas mínimas y máximas para el control deslizante en una barra de seguimiento. <br/>                                                                                                                                                                                                                  |
| [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md)           | Establece la posición lógica máxima del control deslizante en una barra de seguimiento. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md)           | Establece la posición lógica mínima del control deslizante en una barra de seguimiento. <br/>                                                                                                                                                                                                                                        |
| [**TBM \_ SETSEL**](tbm-setsel.md)                     | Establece las posiciones inicial y final del intervalo de selección disponible en una barra de seguimiento. <br/>                                                                                                                                                                                                                |
| [**TBM \_ SETSELEND**](tbm-setselend.md)               | Establece la posición lógica final del intervalo de selección actual en una barra de seguimiento. Este mensaje se omite si la barra de seguimiento no tiene el [**estilo \_ ENABLESELRANGE de TBS.**](trackbar-control-styles.md) <br/>                                                                              |
| [**TBM \_ SETSELSTART**](tbm-setselstart.md)           | Establece la posición lógica inicial del intervalo de selección actual en una barra de seguimiento. Este mensaje se omite si la barra de seguimiento no tiene el [**estilo \_ ENABLESELRANGE de TBS.**](trackbar-control-styles.md) <br/>                                                                            |
| [**TBM \_ SETTHUMBLENGTH**](tbm-setthumblength.md)     | Establece la longitud del control deslizante en una barra de seguimiento. Este mensaje se omite si la barra de seguimiento no tiene el [**\_ estilo FIXEDLENGTH de TBS.**](trackbar-control-styles.md) <br/>                                                                                                                      |
| [**TBM \_ SETTIC**](tbm-settic.md)                     | Establece una marca de graduación en una barra de seguimiento en la posición lógica especificada. <br/>                                                                                                                                                                                                                                      |
| [**TBM \_ SETTICFREQ**](tbm-setticfreq.md)             | Establece la frecuencia de intervalo de las marcas de graduación en una barra de seguimiento. Por ejemplo, si la frecuencia se establece en dos, se muestra una marca de graduación para cada otro incremento en el intervalo de la barra de seguimiento. El valor predeterminado para la frecuencia es uno; Es decir, cada incremento del intervalo está asociado a una marca de graduación. <br/> |
| [**TBM \_ SETTIPSIDE**](tbm-settipside.md)             | Coloca un control de información sobre herramientas utilizado por un control trackbar. Los controles de barra de seguimiento que usan el estilo [**TBS \_ TOOLTIPS**](trackbar-control-styles.md) muestran información sobre herramientas. <br/>                                                                                                                           |
| [**TBM \_ SETTOOLTIPS**](tbm-settooltips.md)           | Asigna un control de información sobre herramientas a un control trackbar. <br/>                                                                                                                                                                                                                                                       |
| [**TBM \_ SETUNICODEFORMAT**](tbm-setunicodeformat.md) | Establece la marca de formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control. <br/>                                                                                                               |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                              | Contenido                                                                                                                                                                                      |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW (barra de seguimiento)](nm-customdraw-trackbar.md)            | Enviado por un control trackbar para notificar a sus ventanas primarias sobre las operaciones de dibujo. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>        |
| [NM \_ RELEASEDCAPTURE (barra de seguimiento)](nm-releasedcapture-trackbar-.md) | Notifica a la ventana primaria de un control trackbar que el control está liberando la captura del mouse. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/> |
| [TRBN \_ THUMBPOSCHANGING](trbn-thumbposchanging.md)                | Notifica que la posición del control en una barra de seguimiento está cambiando. Este código de notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md)<br/>                               |



 

### <a name="constants"></a>Constantes



| Tema                                                  | Contenido                                                                                    |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Valores de dibujo personalizados](custom-draw-values.md)           | En esta sección se enumeran los valores usados para identificar las partes de un control trackbar. <br/>      |
| [Estilos de control de la barra de seguimiento](trackbar-control-styles.md) | Esta sección contiene información sobre los estilos usados con controles de barra de seguimiento. <br/> |



 

 

 





