---
title: Control estático
description: Esta sección contiene información sobre los elementos de programación utilizados con controles estáticos. Un control estático es un control que permite a una aplicación proporcionar al usuario texto informativo y gráficos que normalmente no requiere ninguna respuesta.
ms.assetid: vs|controls|~\controls\staticcontrols\staticcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c8c5b554dad8c6f3c18d0c1ceb9300dde57b20
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078454"
---
# <a name="static-control"></a>Control estático

Esta sección contiene información sobre los elementos de programación utilizados con controles estáticos. Un *control estático* es un control que permite a una aplicación proporcionar al usuario texto informativo y gráficos que normalmente no requiere ninguna respuesta.

### <a name="overviews"></a>Temas de introducción



| Tema                                              | Contenido                                                              |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [Acerca de los controles estáticos](about-static-controls.md) | En este tema se describe cómo se usan los controles estáticos.<br/>         |
| [Estilos de control estáticos](static-control-styles.md) |                                                                       |
| [Usar controles estáticos](using-static-controls.md) | En este tema se proporciona un ejemplo que usa un control estático.<br/> |



 

### <a name="messages"></a>error de Hadoop



| Tema                                 | Contenido                                                                                                                                                                        |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**STM \_ GETICON**](stm-geticon.md)   | Una aplicación envía el mensaje [**STM \_ GETICON**](stm-geticon.md) para recuperar un identificador del icono asociado a un control estático que tiene el estilo de \_ icono SS. <br/> |
| [**STM \_ GetImage**](stm-getimage.md) | Una aplicación envía un mensaje de [**STM \_ GetImage**](stm-getimage.md) para recuperar un identificador de la imagen (icono o mapa de bits) asociado a un control estático. <br/>          |
| [**STM \_ SETICON**](stm-seticon.md)   | Una aplicación envía el mensaje [**STM \_ SETICON**](stm-seticon.md) para asociar un icono a un control de icono. <br/>                                                     |
| [**STM \_ SETIMAGE**](stm-setimage.md) | Una aplicación envía un mensaje [**STM \_ SETIMAGE**](stm-setimage.md) para asociar una nueva imagen con un control estático.<br/>                                                |



 

### <a name="notifications"></a>Notificaciones



| Tema                                           | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [STN \_ clic](stn-clicked.md)                 | El código de notificación en el que se [ \_ hace clic en STN](stn-clicked.md) se envía cuando el usuario hace clic en un control estático que tenga el estilo [**SS \_ Notify**](static-control-styles.md) . La ventana primaria del control recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                                                  |
| [STN \_ DBLCLK](stn-dblclk.md)                   | El código de notificación [STN \_ DBLCLK](stn-dblclk.md) se envía cuando el usuario hace doble clic en un control estático que tenga el estilo **SS \_ Notify** . La ventana primaria del control recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                                                                          |
| [Deshabilitación de STN \_](stn-disable.md)                 | Se envía el código de notificación de [ \_ deshabilitación de STN](stn-disable.md) cuando se deshabilita un control estático. El control estático debe tener el estilo **SS \_ Notify** para recibir este código de notificación. La ventana primaria del control recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                            |
| [\_habilitación de STN](stn-enable.md)                   | El código de notificación de [ \_ habilitación de STN](stn-enable.md) se envía cuando se habilita un control estático. El control estático debe tener el estilo **SS \_ Notify** para recibir este código de notificación. La ventana primaria del control recibe este código de notificación a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                               |
| [**CTLCOLORSTATIC de WM \_**](wm-ctlcolorstatic.md) | Un control estático o un control de edición que sea de solo lectura o deshabilitado, envía el mensaje de [**\_ CTLCOLORSTATIC de WM**](wm-ctlcolorstatic.md) a su ventana primaria cuando el control está a punto de dibujarse. Al responder a este mensaje, la ventana primaria puede usar el identificador de contexto de dispositivo especificado para establecer los colores de texto y de fondo del control estático. <br/> Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |



 

 

