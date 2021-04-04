---
title: Control de Up-Down
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de flechas.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8364eb44ee01e27439c82d1d77e674bfb9e3165
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075559"
---
# <a name="up-down-control"></a>Control de Up-Down

Esta sección contiene información sobre los elementos de programación utilizados con controles de flechas.

### <a name="overviews"></a>Temas de introducción



| Tema                                    | Contenido                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controles de flechas](up-down-controls.md) | Un control de flechas es un par de botones de flecha en los que el usuario puede hacer clic para aumentar o disminuir un valor, como una posición de desplazamiento o un número mostrado en un control complementario (denominado ventana relacionada).<br/> |



 

### <a name="functions"></a>Functions



| Tema                                              | Contenido                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpDownControl**](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | Crea un control de flechas. Nota: esta función está obsoleta. Es una función de 16 bits y no puede controlar valores de 32 bits para el intervalo y la posición.<br/> |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                 | Contenido                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UDM \_ GETACCEL**](udm-getaccel.md)                 | Recupera información de aceleración de un control de flechas. <br/>                                                                                                                                                                 |
| [**UDM \_ GETBASE**](udm-getbase.md)                   | Recupera la base de base actual (es decir, base 10 o 16) para un control de flechas. <br/>                                                                                                                                   |
| [**UDM \_ GETBUDDY**](udm-getbuddy.md)                 | Recupera el identificador de la ventana relacionada actual. <br/>                                                                                                                                                                          |
| [**UDM \_ GETPOS**](udm-getpos.md)                     | Recupera la posición actual de un control de flechas con una precisión de 16 bits. <br/>                                                                                                                                                |
| [**UDM \_ GETPOS32**](udm-getpos32.md)                 | Devuelve la posición de 32 bits de un control de flechas.<br/>                                                                                                                                                                          |
| [**UDM \_ GETRANGE**](udm-getrange.md)                 | Recupera las posiciones mínima y máxima (intervalo) de un control de flechas. <br/>                                                                                                                                                |
| [**UDM \_ GETRANGE32**](udm-getrange32.md)             | Recupera el intervalo de 32 bits de un control de flechas. <br/>                                                                                                                                                                          |
| [**UDM \_ GETUNICODEFORMAT**](udm-getunicodeformat.md) | Recupera la marca del formato de caracteres Unicode para el control. <br/>                                                                                                                                                               |
| [**UDM \_ SETACCEL**](udm-setaccel.md)                 | Establece la aceleración para un control de flechas. <br/>                                                                                                                                                                              |
| [**UDM \_ SETBASE**](udm-setbase.md)                   | Establece la base de base de un control de flechas. El valor base determina si la ventana relacionada muestra números en dígitos decimales o hexadecimales. Los números hexadecimales siempre están sin signo y los números decimales están firmados. <br/> |
| [**UDM \_ SETBUDDY**](udm-setbuddy.md)                 | Establece la ventana relacionada para un control de flechas. <br/>                                                                                                                                                                              |
| [**UDM \_ SETPOS**](udm-setpos.md)                     | Establece la posición actual de un control de flechas con una precisión de 16 bits. <br/>                                                                                                                                                    |
| [**UDM \_ SETPOS32**](udm-setpos32.md)                 | Establece la posición de un control de flechas con una precisión de 32 bits.<br/>                                                                                                                                                              |
| [**UDM \_ SetRange**](udm-setrange.md)                 | Establece las posiciones mínima y máxima (intervalo) de un control de flechas.<br/>                                                                                                                                                      |
| [**UDM \_ SETRANGE32**](udm-setrange32.md)             | Establece el intervalo de 32 bits de un control de flechas. <br/>                                                                                                                                                                               |
| [**UDM \_ SETUNICODEFORMAT**](udm-setunicodeformat.md) | Establece la marca del formato de caracteres Unicode para el control. Este mensaje permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución, en lugar de tener que volver a crear el control. <br/>                                   |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                            | Contenido                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (arriba-abajo)](nm-releasedcapture-up-down-.md) | Notifica a la ventana primaria de un control de flechas que el control está liberando la captura del mouse. Esta notificación se envía en forma de mensaje de [**\_ notificación de WM**](wm-notify.md) . <br/>                                                                                                                                                                       |
| [UDN \_ DELTAPOS](udn-deltapos.md)                                | Lo envía el sistema operativo a la ventana primaria de un control de flechas cuando la posición del control está a punto de cambiar. Esto sucede cuando el usuario solicita un cambio en el valor presionando la flecha arriba o abajo del control. El mensaje [UDN \_ DELTAPOS](udn-deltapos.md) se envía con el formato de un mensaje de [**\_ notificación de WM**](wm-notify.md) . <br/> |



 

### <a name="structures"></a>Estructuras



| Tema                        | Contenido                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | Contiene información específica de los mensajes de notificación de control de flechas. Es idéntico a y reemplaza a la estructura up de **nm \_** . <br/> |
| [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | Contiene información de aceleración de un control de flechas. <br/>                                                                             |



 

### <a name="constants"></a>Constantes



| Tema                                                | Contenido                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [Estilos de control de flechas](up-down-control-styles.md) | En esta sección se enumeran los estilos usados al crear controles de flechas.<br/> |



 

 

 





