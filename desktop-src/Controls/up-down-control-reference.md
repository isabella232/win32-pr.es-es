---
title: Up-Down control
description: Esta sección contiene información sobre los elementos de programación usados con controles de arriba a abajo.
ms.assetid: 48c6b4bd-65b4-4388-959e-efffa7658274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2979ac08889761cb7f226b58a9d951d407bc82420957ed9327de1a880d0d9bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018593"
---
# <a name="up-down-control"></a>Up-Down control

Esta sección contiene información sobre los elementos de programación usados con controles de arriba a abajo.

### <a name="overviews"></a>Temas de introducción



| Tema                                    | Contenido                                                                                                                                                                                                            |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controles de arriba a abajo](up-down-controls.md) | Un control de flecha arriba es un par de botones de flecha en los que el usuario puede hacer clic para incrementar o disminuir un valor, como una posición de desplazamiento o un número que se muestra en un control complementario (denominado ventana de compañeros).<br/> |



 

### <a name="functions"></a>Functions



| Tema                                              | Contenido                                                                                                                                                |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateUpDownControl**](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) | Crea un control de flechas. Nota: Esta función está obsoleta. Es una función de 16 bits y no puede controlar valores de 32 bits para el intervalo y la posición.<br/> |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                 | Contenido                                                                                                                                                                                                                               |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UDM \_ GETACCEL**](udm-getaccel.md)                 | Recupera información de aceleración para un control de flechas. <br/>                                                                                                                                                                 |
| [**UDM \_ GETBASE**](udm-getbase.md)                   | Recupera la base base de base actual (es decir, base 10 o 16) para un control de flechas. <br/>                                                                                                                                   |
| [**UDM \_ GETBUDDY**](udm-getbuddy.md)                 | Recupera el identificador en la ventana actual del compañero. <br/>                                                                                                                                                                          |
| [**UDM \_ GETPOS**](udm-getpos.md)                     | Recupera la posición actual de un control hacia abajo con una precisión de 16 bits. <br/>                                                                                                                                                |
| [**UDM \_ GETPOS32**](udm-getpos32.md)                 | Devuelve la posición de 32 bits de un control de arriba a abajo.<br/>                                                                                                                                                                          |
| [**UDM \_ GETRANGE**](udm-getrange.md)                 | Recupera las posiciones mínima y máxima (intervalo) de un control de flechas. <br/>                                                                                                                                                |
| [**UDM \_ GETRANGE32**](udm-getrange32.md)             | Recupera el intervalo de 32 bits de un control de flechas. <br/>                                                                                                                                                                          |
| [**UDM \_ GETUNICODEFORMAT**](udm-getunicodeformat.md) | Recupera la marca de formato de caracteres Unicode para el control . <br/>                                                                                                                                                               |
| [**UDM \_ SETACCEL**](udm-setaccel.md)                 | Establece la aceleración de un control de flechas. <br/>                                                                                                                                                                              |
| [**UDM \_ SETBASE**](udm-setbase.md)                   | Establece la base base de base para un control de flechas. El valor base determina si la ventana de compañeros muestra números en dígitos decimales o hexadecimales. Los números hexadecimales siempre son sin signo y los números decimales están firmados. <br/> |
| [**UDM \_ SETBUDDY**](udm-setbuddy.md)                 | Establece la ventana del compañero para un control de flechas. <br/>                                                                                                                                                                              |
| [**UDM \_ SETPOS**](udm-setpos.md)                     | Establece la posición actual de un control de arriba a abajo con precisión de 16 bits. <br/>                                                                                                                                                    |
| [**UDM \_ SETPOS32**](udm-setpos32.md)                 | Establece la posición de un control hacia abajo con precisión de 32 bits.<br/>                                                                                                                                                              |
| [**UDM \_ SETRANGE**](udm-setrange.md)                 | Establece las posiciones mínima y máxima (intervalo) de un control de flechas.<br/>                                                                                                                                                      |
| [**UDM \_ SETRANGE32**](udm-setrange32.md)             | Establece el intervalo de 32 bits de un control de flechas. <br/>                                                                                                                                                                               |
| [**UDM \_ SETUNICODEFORMAT**](udm-setunicodeformat.md) | Establece la marca de formato de caracteres Unicode para el control. Este mensaje le permite cambiar el juego de caracteres utilizado por el control en tiempo de ejecución en lugar de tener que volver a crear el control. <br/>                                   |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                            | Contenido                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ RELEASEDCAPTURE (arriba abajo)](nm-releasedcapture-up-down-.md) | Notifica a la ventana primaria de un control hacia abajo que el control está liberando la captura del mouse. Esta notificación se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/>                                                                                                                                                                       |
| [UDN \_ DELTAPOS](udn-deltapos.md)                                | Enviado por el sistema operativo a la ventana primaria de un control hacia abajo cuando la posición del control está a punto de cambiar. Esto sucede cuando el usuario solicita un cambio en el valor presionando la flecha arriba o abajo del control. El [mensaje \_ UDN DELTAPOS](udn-deltapos.md) se envía en forma de mensaje [**WM \_ NOTIFY.**](wm-notify.md) <br/> |



 

### <a name="structures"></a>Estructuras



| Tema                        | Contenido                                                                                                                                          |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NMUPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmupdown) | Contiene información específica de los mensajes de notificación de control hacia abajo. Es idéntico a y reemplaza la estructura **\_ UPDOWN de NM.** <br/> |
| [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel)   | Contiene información de aceleración para un control de flechas. <br/>                                                                             |



 

### <a name="constants"></a>Constantes



| Tema                                                | Contenido                                                                      |
|------------------------------------------------------|-------------------------------------------------------------------------------|
| [Estilos de control hacia abajo](up-down-control-styles.md) | En esta sección se enumeran los estilos usados al crear controles de arriba a abajo.<br/> |



 

 

 





