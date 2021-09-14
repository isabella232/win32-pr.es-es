---
title: Control de animación
description: Esta sección contiene información sobre los elementos de programación utilizados con controles de animación.
ms.assetid: 16994f93-e0fd-4c71-9c8a-15642408b8de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2a3fc7377c7258ba49b5a4188e6074270b5862
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170157"
---
# <a name="animation-control"></a>Control de animación

Esta sección contiene información sobre los elementos de programación utilizados con controles de animación.

### <a name="overviews"></a>Temas de introducción



| Tema                                                      | Contenido                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los controles de animación](animation-control-overview.md) | Un *control de* animación es una ventana que muestra Audio-Video clip intercalado (AVI). Un clip AVI es una serie de fotogramas de mapa de bits como una película. Los controles de animación solo pueden mostrar clips AVI que no contengan audio.<br/> |
| [Usar controles de animación](using-animation-control.md)    | En esta sección se proporciona información de implementación y código de ejemplo para controles de animación.<br/>                                                                                                                                      |



 

### <a name="macros"></a>Macros



| Tema                                           | Contenido                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Animar \_ cerrar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)         | Cierra un clip AVI. Puede usar esta macro o enviar el mensaje OPEN de [**ACM \_**](acm-open.md) explícitamente, pasando parámetros **NULL.** <br/>                                                                                                              |
| [**Animar \_ creación**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create)       | Crea un control de animación. [**Animar \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) llama a [**la función CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) para crear el control de animación. <br/>                                                                                   |
| [**Animar \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) | Comprueba si se está reproduciendo un clip AVI. Puede usar esta macro o enviar un [**mensaje \_ ISPLAYING de ACM.**](acm-isplaying.md)<br/>                                                                                                                            |
| [**Animar \_ abrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open)           | Abre un clip AVI y muestra su primer fotograma en un control de animación. Puede usar esta macro o enviar el mensaje OPEN de [**ACM \_**](acm-open.md) explícitamente. <br/>                                                                                          |
| [**Animar \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex)       | Abre un clip AVI desde un recurso de un módulo especificado y muestra su primer fotograma en un control de animación. Puede usar esta macro o enviar el mensaje OPEN de [**ACM \_**](acm-open.md) explícitamente. <br/>                                                    |
| [**Animar \_ reproducción**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)           | Reproduce un clip AVI en un control de animación. El control reproduce el clip en segundo plano mientras el subproceso continúa ejecutándose. Puede usar esta macro o enviar el mensaje [**ACM \_ PLAY**](acm-play.md) explícitamente. <br/>                                    |
| [**Animar \_ búsqueda**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek)           | Dirige un control de animación para mostrar un fotograma determinado de un clip AVI. El control muestra el clip en segundo plano mientras el subproceso continúa ejecutándose. Puede usar esta macro o enviar el mensaje [**ACM \_ PLAY**](acm-play.md) explícitamente. <br/> |
| [**Animar \_ detente**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)           | Detiene la reproducción de un clip AVI en un control de animación. Puede usar esta macro o enviar el mensaje STOP de [**ACM \_**](acm-stop.md) explícitamente. <br/>                                                                                                               |



 

### <a name="messages"></a>error de Hadoop



| Tema                                   | Contenido                                                                                                                                                                                                                                   |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACM \_ ISPLAYING**](acm-isplaying.md) | Comprueba si se está reproduciendo un clip AVI. Puede enviar este mensaje explícitamente o usar la macro [**\_ Animate IsPlaying.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying)<br/>                                                                                   |
| [**ACM \_ OPEN**](acm-open.md)           | Abre un clip AVI y muestra su primer fotograma en un control de animación. Puede enviar este mensaje explícitamente o usar la macro [**Animar \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) [**o Animar \_ OpenEx.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) <br/>              |
| [**ACM \_ PLAY**](acm-play.md)           | Reproduce un clip AVI en un control de animación. El control reproduce el clip en segundo plano mientras el subproceso continúa ejecutándose. Puede enviar este mensaje explícitamente o mediante la macro [**Animar \_ reproducción.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)<br/> |
| [**ACM \_ STOP**](acm-stop.md)           | Detiene la reproducción de un clip AVI en un control de animación. Puede enviar este mensaje explícitamente o mediante la macro [**Animar \_ detener.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)<br/>                                                                            |



 

### <a name="notifications"></a>Notificaciones



| Tema                           | Contenido                                                                                                                                                                                                       |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACN \_ START**](acn-start.md) | Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha empezado a reproducirse. Este código de notificación se envía en forma de mensaje [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) <br/>      |
| [**ACN \_ STOP**](acn-stop.md)   | Notifica a la ventana primaria de un control de animación que el clip AVI asociado ha dejado de reproducirse. Este código de notificación se envía en forma de mensaje [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command) <br/> |



 

### <a name="constants"></a>Constantes



| Tema                                                        | Contenido                                                                      |
|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**Estilos de control de animación**](animation-control-styles.md) | En esta sección se enumeran los estilos de ventana utilizados con controles de animación.<br/> |



 

 

