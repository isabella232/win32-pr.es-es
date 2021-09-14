---
title: Control estático
description: Esta sección contiene información sobre los elementos de programación utilizados con controles estáticos. Un control estático es un control que permite que una aplicación proporcione al usuario texto informativo y gráficos que normalmente no requieren ninguna respuesta.
ms.assetid: vs|controls|~\controls\staticcontrols\staticcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c8c5b554dad8c6f3c18d0c1ceb9300dde57b20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167026"
---
# <a name="static-control"></a>Control estático

Esta sección contiene información sobre los elementos de programación utilizados con controles estáticos. Un *control estático* es un control que permite que una aplicación proporcione al usuario texto informativo y gráficos que normalmente no requieren respuesta.

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
| [**SETICON de STM \_**](stm-seticon.md)   | Una aplicación envía el [**mensaje \_ SETICON de STM**](stm-seticon.md) para asociar un icono a un control de icono. <br/>                                                     |
| [**STM \_ SETIMAGE**](stm-setimage.md) | Una aplicación envía un [**mensaje \_ SETIMAGE de STM**](stm-setimage.md) para asociar una nueva imagen a un control estático.<br/>                                                |



 

### <a name="notifications"></a>Notificaciones



| Tema                                           | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [STN \_ CLICKED](stn-clicked.md)                 | El [código de notificación DE \_ STN CLICKED](stn-clicked.md) se envía cuando el usuario hace clic en un control estático que tiene el [**estilo NOTIFY \_ de SS.**](static-control-styles.md) La ventana primaria del control recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)<br/>                                                                                                                                                                  |
| [STN \_ DBLCLK](stn-dblclk.md)                   | El [código de notificación \_ DBLCLK de STN](stn-dblclk.md) se envía cuando el usuario hace doble clic en un control estático que tiene el estilo NOTIFY **\_ de SS.** La ventana primaria del control recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)<br/>                                                                                                                                                                                          |
| [STN \_ DISABLE](stn-disable.md)                 | El [código de notificación \_ DISABLE](stn-disable.md) de STN se envía cuando se deshabilita un control estático. El control estático debe tener el **estilo \_ NOTIFY de SS** para recibir este código de notificación. La ventana primaria del control recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)<br/>                                                                                                                                            |
| [STN \_ ENABLE](stn-enable.md)                   | El [código de notificación \_ ENABLE](stn-enable.md) de STN se envía cuando se habilita un control estático. El control estático debe tener el **estilo \_ NOTIFY de SS** para recibir este código de notificación. La ventana primaria del control recibe este código de notificación a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command)<br/>                                                                                                                                               |
| [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) | Un control estático, o un control de edición que es de solo lectura o deshabilitado, envía el mensaje [**\_ WM CTLCOLORSTATIC**](wm-ctlcolorstatic.md) a su ventana primaria cuando el control está a punto de dibujarse. Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de dispositivo especificado para establecer el texto y los colores de fondo del control estático. <br/> Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) <br/> |



 

 

