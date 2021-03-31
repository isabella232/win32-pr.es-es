---
title: Cuadro de diálogo tarea
description: Esta sección contiene información sobre los elementos de programación utilizados con un cuadro de diálogo de tarea. Un cuadro de diálogo de tarea es similar a, aunque es mucho más flexible que un cuadro de mensaje básico.
ms.assetid: vs|controls|~\controls\taskdialogs\taskdialogs.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4f115531b9f872c824e9d1822be07777b2bc439
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/24/2020
ms.locfileid: "103904898"
---
# <a name="task-dialog"></a>Cuadro de diálogo tarea

Esta sección contiene información sobre los elementos de programación utilizados con un cuadro de diálogo de tarea. Un cuadro de *diálogo de tarea* es similar a, aunque es mucho más flexible que un cuadro de mensaje básico.

### <a name="overviews"></a>Temas de introducción



| Tema                                           | Contenido                                            |
|-------------------------------------------------|-----------------------------------------------------|
| [Acerca de los cuadros de diálogo de tareas](task-dialogs-overview.md) | Describe los elementos de un cuadro de diálogo de tarea.<br/> |



 

### <a name="functions"></a>Functions



| Tema                                                  | Contenido                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog)                       | Crea, muestra y opera un cuadro de diálogo de tarea. El cuadro de diálogo tarea contiene el texto del mensaje definido por la aplicación y el título, los iconos y cualquier combinación de botones de predefinido. Esta función no admite el registro de una función de devolución de llamada para recibir notificaciones.<br/>                                                                                                                |
| [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) | Una función definida por la aplicación que se usa con la función [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Recibe mensajes del cuadro de diálogo de tarea cuando se producen varios eventos.<br/> El tipo **PFTASKDIALOGCALLBACK** define un puntero a esta función de devolución de llamada. [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) es un marcador de posición para el nombre de la función definida por la aplicación.<br/> |
| [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)       | Crea, muestra y opera un cuadro de diálogo de tarea. El cuadro de diálogo tarea contiene iconos definidos por la aplicación, mensajes, título, casilla de verificación, vínculos de comandos, botones de comando y botones de radio. Esta función puede registrar una función de devolución de llamada para recibir mensajes de notificación.<br/>                                                                                                               |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                                                           | Contenido                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_botón de clic de TDM \_**](tdm-click-button.md)                                                  | Simula la acción de un clic de botón en un cuadro de diálogo de tarea.<br/>                                                                                                                                  |
| [**\_botón de \_ radio haga clic en TDM \_**](tdm-click-radio-button.md)                                     | Simula la acción de un clic de botón de radio en un cuadro de diálogo de tarea.<br/>                                                                                                                            |
| [**TDM- \_ clic en \_ comprobación**](tdm-click-verification.md)                                      | Simula la acción de una casilla de verificación de comprobación haga clic en un cuadro de diálogo de tarea.<br/>                                                                                                                   |
| [**\_botón habilitar \_ TDM**](tdm-enable-button.md)                                                | Habilita o deshabilita un botón de reenvío en un cuadro de diálogo de tarea.<br/>                                                                                                                                       |
| [**\_botón de \_ radio \_ Habilitar TDM**](tdm-enable-radio-button.md)                                   | Habilita o deshabilita un botón de radio en un cuadro de diálogo de tarea.<br/>                                                                                                                                      |
| [**\_Página de navegación de TDM \_**](tdm-navigate-page.md)                                                | Vuelve a crear un cuadro de diálogo de tarea con contenido nuevo, simulando la funcionalidad de un asistente de varias páginas.<br/>                                                                                           |
| [**\_ \_ \_ estado obligatorio de elevación de botón \_ de \_ TDM**](tdm-set-button-elevation-required-state.md) | Especifica si un botón de cuadro de diálogo de tarea o vínculo de comando determinado debe tener un icono de escudo de control de cuentas de usuario (UAC). es decir, si la acción invocada por el botón requiere elevación. <br/> |
| [**\_texto del \_ elemento de conjunto de TDM \_**](tdm-set-element-text.md)                                         | Actualiza un elemento de texto en un cuadro de diálogo de tarea.<br/>                                                                                                                                                  |
| [**\_barra de \_ progreso del \_ conjunto de TDM \_**](tdm-set-marquee-progress-bar.md)                        | Indica si la barra de progreso hospedada debe mostrarse en el modo de marquesina.<br/>                                                                                                            |
| [**cuadro de la barra de progreso de \_ configuración de TDM \_ \_ \_**](tdm-set-progress-bar-marquee.md)                        | Inicia y detiene la presentación de la marquesina de la barra de progreso, y establece la velocidad del marco.<br/>                                                                                              |
| [**PDV de la \_ \_ barra de progreso set \_ de TDM \_**](tdm-set-progress-bar-pos.md)                                | Establece la posición actual de una barra de progreso.<br/>                                                                                                                                             |
| [**intervalo de la barra de progreso del \_ conjunto de TDM \_ \_ \_**](tdm-set-progress-bar-range.md)                            | Establece los valores mínimo y máximo de la barra de progreso hospedada.<br/>                                                                                                                          |
| [**Estado de la barra de progreso del \_ conjunto de TDM \_ \_ \_**](tdm-set-progress-bar-state.md)                            | Establece el estado actual de la barra de progreso.<br/>                                                                                                                                               |
| [**\_texto del \_ elemento de actualización de TDM \_**](tdm-update-element-text.md)                                   | Actualiza un elemento de texto en un cuadro de diálogo de tarea. <br/>                                                                                                                                                 |
| [**\_icono de actualización de TDM \_**](tdm-update-icon.md)                                                    | Actualiza el icono de un cuadro de diálogo de tarea. <br/>                                                                                                                                                     |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                           | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_clic en el botón TDN \_](tdn-button-clicked.md)                  | Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón o vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                   |
| [TDN \_ creado](tdn-created.md)                                 | Enviado por un cuadro de diálogo de tarea después de crear el cuadro de diálogo de tarea y antes de que se muestre. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [TDN \_ destruido](tdn-destroyed.md)                             | Enviado por un cuadro de diálogo de tarea cuando se destruye y su identificador de ventana ya no es válido. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                       |
| [\_cuadro de diálogo TDN \_ construido](tdn-dialog-constructed.md)          | Enviado por un cuadro de diálogo de tarea después de crear el cuadro de diálogo de tarea y antes de que se muestre. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [TDN \_ \_ clic en el botón Expando \_](tdn-expando-button-clicked.md) | Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en el botón Expando del cuadro de diálogo de tarea. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                            |
| [ayuda de TDN \_](tdn-help.md)                                       | Enviado por un cuadro de diálogo de tarea cuando el usuario presiona F1 en el teclado mientras el cuadro de diálogo de tarea tiene el foco. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                            |
| [TDN \_ hipervínculo con \_ clic](tdn-hyperlink-clicked.md)            | Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en un hipervínculo en el contenido del cuadro de diálogo de tarea. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                        |
| [TDN \_ navegado](tdn-navigated.md)                             | Enviado por un cuadro de diálogo de tarea cuando se ha producido una navegación. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                                                     |
| [botón de radio TDN en el que se \_ \_ \_ hizo clic](tdn-radio-button-clicked.md)     | Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón o vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . <br/>                                                                                                                                                                                                  |
| [temporizador de TDN \_](tdn-timer.md)                                     | Enviado por un cuadro de diálogo de tarea aproximadamente cada 200 milisegundos. Este código de notificación se envía cuando se ha \_ establecido la marca de temporizador de devolución de llamada TDF \_ en el miembro **dwFlags** de la estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que se pasó a la función [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método **TaskDialogIndirect** .<br/> |
| [comprobación de TDN en la que se \_ \_ hizo clic](tdn-verification-clicked.md)      | Enviado por el cuadro de diálogo de tarea cuando el usuario hace clic en la casilla de verificación del cuadro de diálogo de tareas. Este código de notificación se recibe solo a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .<br/>                                                                                                                                                                                                       |



 

### <a name="structures"></a>Estructuras



| Tema                                           | Contenido                                                                                                                                                   |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_botón TASKDIALOG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialog_button) | Contiene información que se usa para mostrar un botón en un cuadro de diálogo de tarea. La estructura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usa esta estructura.<br/> |
| [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)    | Contiene información que se usa para mostrar un cuadro de diálogo de tarea. La función [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) usa esta estructura.<br/>          |



 

 

