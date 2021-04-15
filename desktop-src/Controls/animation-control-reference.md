---
title: Animation (control)
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de animación.
ms.assetid: 16994f93-e0fd-4c71-9c8a-15642408b8de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2a3fc7377c7258ba49b5a4188e6074270b5862
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488370"
---
# <a name="animation-control"></a>Animation (control)

Esta sección contiene información sobre los elementos de programación utilizados con controles de animación.

### <a name="overviews"></a>Temas de introducción



| Tema                                                      | Contenido                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los controles de animación](animation-control-overview.md) | Un *control de animación* es una ventana que muestra un Audio-Video clip intercalado (AVI). Un clip AVI es una serie de fotogramas de mapa de bits como una película. Los controles de animación solo pueden mostrar clips AVI que no contienen audio.<br/> |
| [Usar controles de animación](using-animation-control.md)    | En esta sección se proporcionan detalles de implementación y código de ejemplo para los controles de animación.<br/>                                                                                                                                      |



 

### <a name="macros"></a>Macros



| Tema                                           | Contenido                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Animar \_ cerrar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)         | Cierra un clip AVI. Puede usar esta macro o enviar el mensaje [**\_ abierto de ACM**](acm-open.md) explícitamente, pasando parámetros **null** . <br/>                                                                                                              |
| [**Animar \_ crear**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create)       | Crea un control de animación. [**Animar \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) llama a la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) para crear el control Animation. <br/>                                                                                   |
| [**Animar \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) | Comprueba si se está reproduciendo un clip AVI. Puede usar esta macro o enviar un mensaje [**ACM \_ ISPLAYING**](acm-isplaying.md) .<br/>                                                                                                                            |
| [**Animar \_ abierto**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open)           | Abre un clip AVI y muestra su primer fotograma en un control Animation. Puede usar esta macro o enviar el mensaje [**\_ abierto ACM**](acm-open.md) explícitamente. <br/>                                                                                          |
| [**Animar \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex)       | Abre un clip AVI desde un recurso de un módulo especificado y muestra su primer fotograma en un control Animation. Puede usar esta macro o enviar el mensaje [**\_ abierto ACM**](acm-open.md) explícitamente. <br/>                                                    |
| [**Animar \_ reproducción**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)           | Reproduce un clip AVI en un control Animation. El control reproduce el clip en segundo plano mientras se sigue ejecutando el subproceso. Puede usar esta macro o enviar el mensaje [**de \_ reproducción ACM**](acm-play.md) explícitamente. <br/>                                    |
| [**Animar \_ búsqueda**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek)           | Dirige un control de animación para mostrar un fotograma determinado de un clip AVI. El control muestra el clip en segundo plano mientras se sigue ejecutando el subproceso. Puede usar esta macro o enviar el mensaje [**de \_ reproducción ACM**](acm-play.md) explícitamente. <br/> |
| [**Animar \_ detener**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)           | Detiene la reproducción de un clip AVI en un control Animation. Puede usar esta macro o enviar el mensaje [**de \_ detención de ACM**](acm-stop.md) explícitamente. <br/>                                                                                                               |



 

### <a name="messages"></a>error de Hadoop



| Tema                                   | Contenido                                                                                                                                                                                                                                   |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACM \_ ISPLAYING**](acm-isplaying.md) | Comprueba si se está reproduciendo un clip AVI. Puede enviar este mensaje explícitamente o utilizar la macro [**Animate \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .<br/>                                                                                   |
| [**ACM \_ abierto**](acm-open.md)           | Abre un clip AVI y muestra su primer fotograma en un control Animation. Puede enviar este mensaje explícitamente o utilizar la macro de [**animación \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) o [**Animate \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) . <br/>              |
| [**reproducción de ACM \_**](acm-play.md)           | Reproduce un clip AVI en un control Animation. El control reproduce el clip en segundo plano mientras se sigue ejecutando el subproceso. Puede enviar este mensaje explícitamente o mediante el uso de la macro [**Animate \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .<br/> |
| [**detención de ACM \_**](acm-stop.md)           | Detiene la reproducción de un clip AVI en un control Animation. Puede enviar este mensaje explícitamente o mediante la macro [**Animate \_ Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .<br/>                                                                            |



 

### <a name="notifications"></a>Notificaciones



| Tema                           | Contenido                                                                                                                                                                                                       |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inicio de ACN \_**](acn-start.md) | Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha empezado a reproducirse. Este código de notificación se envía en forma de mensaje [**de \_ comando de WM**](/windows/desktop/menurc/wm-command) . <br/>      |
| [**ACN \_ detener**](acn-stop.md)   | Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha dejado de reproducirse. Este código de notificación se envía en forma de mensaje [**de \_ comando de WM**](/windows/desktop/menurc/wm-command) . <br/> |



 

### <a name="constants"></a>Constantes



| Tema                                                        | Contenido                                                                      |
|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**Estilos de control de animación**](animation-control-styles.md) | En esta sección se enumeran los estilos de ventana utilizados con los controles de animación.<br/> |



 

 

