---
title: Control estático
description: Esta sección contiene información sobre los elementos de programación utilizados con controles estáticos. Un control estático es un control que permite que una aplicación proporcione al usuario texto informativo y gráficos que normalmente no requieren ninguna respuesta.
ms.assetid: vs|controls|~\controls\staticcontrols\staticcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e14659e769475782b483713f639b5d7f633b9081f678e0d0c50b2842fb781b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797885"
---
# <a name="static-control"></a>Control estático

Esta sección contiene información sobre los elementos de programación utilizados con controles estáticos. Un *control estático* es un control que permite que una aplicación proporcione al usuario texto informativo y gráficos que normalmente no requieren ninguna respuesta.

### <a name="overviews"></a>Temas de introducción



| Tema                                              | Contenido                                                              |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [Acerca de los controles estáticos](about-static-controls.md) | En este tema se describe cómo se usan los controles estáticos.<br/>         |
| [Estilos de control estáticos](static-control-styles.md) |                                                                       |
| [Usar controles estáticos](using-static-controls.md) | En este tema se proporciona un ejemplo que usa un control estático.<br/> |



 

### <a name="messages"></a>error de Hadoop



| Tema                                 | Contenido                                                                                                                                                                        |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**STM \_ GETICON**](stm-geticon.md)   | Una aplicación envía el [**mensaje \_ GETICON de STM**](stm-geticon.md) para recuperar un identificador al icono asociado a un control estático que tiene el estilo SS \_ ICON. <br/> |
| [**STM \_ GETIMAGE**](stm-getimage.md) | Una aplicación envía un mensaje [**\_ GETIMAGE de STM**](stm-getimage.md) para recuperar un identificador de la imagen (icono o mapa de bits) asociado a un control estático. <br/>          |
| [**SETICON de STM \_**](stm-seticon.md)   | Una aplicación envía el [**mensaje \_ SETICON**](stm-seticon.md) de STM para asociar un icono a un control de icono. <br/>                                                     |
| [**STM \_ SETIMAGE**](stm-setimage.md) | Una aplicación envía un [**mensaje \_ SETIMAGE de STM**](stm-setimage.md) para asociar una nueva imagen a un control estático.<br/>                                                |



 

### <a name="notifications"></a>Notificaciones



| Tema                                           | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [STN \_ CLICKED](stn-clicked.md)                 | El [código de notificación \_ CLICKED](stn-clicked.md) de STN se envía cuando el usuario hace clic en un control estático que tiene el estilo NOTIFY [**\_ de SS.**](static-control-styles.md) La ventana primaria del control recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)<br/>                                                                                                                                                                  |
| [STN \_ DBLCLK](stn-dblclk.md)                   | El [código de notificación \_ DBLCLK de STN](stn-dblclk.md) se envía cuando el usuario hace doble clic en un control estático que tiene el estilo NOTIFY **\_ de SS.** La ventana primaria del control recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)<br/>                                                                                                                                                                                          |
| [STN \_ DISABLE](stn-disable.md)                 | El [código de notificación \_ DISABLE](stn-disable.md) de STN se envía cuando se deshabilita un control estático. El control estático debe tener el **estilo \_ NOTIFY de SS** para recibir este código de notificación. La ventana primaria del control recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)<br/>                                                                                                                                            |
| [STN \_ ENABLE](stn-enable.md)                   | El [código de notificación \_ ENABLE](stn-enable.md) de STN se envía cuando se habilita un control estático. El control estático debe tener el **estilo \_ NOTIFY de SS** para recibir este código de notificación. La ventana primaria del control recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)<br/>                                                                                                                                               |
| [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) | Un control estático, o un control de edición que es de solo lectura o deshabilitado, envía el mensaje [**\_ WM CTLCOLORSTATIC**](wm-ctlcolorstatic.md) a su ventana primaria cuando el control está a punto de dibujarse. Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de dispositivo especificado para establecer el texto y los colores de fondo del control estático. <br/> Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) <br/> |



 

 

