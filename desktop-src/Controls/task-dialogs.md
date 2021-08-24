---
title: Cuadro de diálogo Tarea
description: Esta sección contiene información sobre los elementos de programación utilizados con un cuadro de diálogo de tarea. Un cuadro de diálogo de tarea es similar, aunque mucho más flexible que un cuadro de mensaje básico.
ms.assetid: vs|controls|~\controls\taskdialogs\taskdialogs.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6797314b75fff46ddf8a4f64638fefb5ea0181d2353bd1a1d3caa57325d28e7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168555"
---
# <a name="task-dialog"></a>Cuadro de diálogo Tarea

Esta sección contiene información sobre los elementos de programación utilizados con un cuadro de diálogo de tarea. Un *cuadro de diálogo de* tarea es similar, aunque mucho más flexible que un cuadro de mensaje básico.

### <a name="overviews"></a>Temas de introducción



| Tema                                           | Contenido                                            |
|-------------------------------------------------|-----------------------------------------------------|
| [Acerca de los cuadros de diálogo de tareas](task-dialogs-overview.md) | Describe los elementos de un cuadro de diálogo de tarea.<br/> |



 

### <a name="functions"></a>Funciones



| Tema                                                  | Contenido                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog)                       | Crea, muestra y opera un cuadro de diálogo de tarea. El cuadro de diálogo de tarea contiene texto y título del mensaje definidos por la aplicación, iconos y cualquier combinación de botones de inserción predefinidos. Esta función no admite el registro de una función de devolución de llamada para recibir notificaciones.<br/>                                                                                                                |
| [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) | Función definida por la aplicación que se usa con [**la función TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) Recibe mensajes del cuadro de diálogo de tarea cuando se producen varios eventos.<br/> El **tipo PFTASKDIALOGCALLBACK** define un puntero a esta función de devolución de llamada. [*TaskDialogCallbackProc es*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) un marcador de posición para el nombre de la función definida por la aplicación.<br/> |
| [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)       | Crea, muestra y opera un cuadro de diálogo de tarea. El cuadro de diálogo de tarea contiene iconos definidos por la aplicación, mensajes, título, casilla de verificación, vínculos de comandos, botones de inserción y botones de radio. Esta función puede registrar una función de devolución de llamada para recibir mensajes de notificación.<br/>                                                                                                               |



 

### <a name="messages"></a>error de Hadoop



| Tema                                                                                           | Contenido                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BOTÓN HACER CLIC EN TDM \_ \_**](tdm-click-button.md)                                                  | Simula la acción de un clic de botón en un cuadro de diálogo de tarea.<br/>                                                                                                                                  |
| [**TDM \_ HAGA CLIC EN EL BOTÓN DE \_ \_ RADIO**](tdm-click-radio-button.md)                                     | Simula la acción de hacer clic en un botón de radio en un cuadro de diálogo de tarea.<br/>                                                                                                                            |
| [**COMPROBACIÓN DE \_ CLICS DE TDM \_**](tdm-click-verification.md)                                      | Simula la acción de una casilla de verificación al hacer clic en un cuadro de diálogo de tarea.<br/>                                                                                                                   |
| [**BOTÓN HABILITAR \_ TDM \_**](tdm-enable-button.md)                                                | Habilita o deshabilita un botón de inserción en un cuadro de diálogo de tarea.<br/>                                                                                                                                       |
| [**BOTÓN DE RADIO HABILITAR TDM \_ \_ \_**](tdm-enable-radio-button.md)                                   | Habilita o deshabilita un botón de radio en un cuadro de diálogo de tarea.<br/>                                                                                                                                      |
| [**PÁGINA DE NAVEGACIÓN DE TDM \_ \_**](tdm-navigate-page.md)                                                | Vuelve a crear un cuadro de diálogo de tarea con nuevo contenido, simulando la funcionalidad de un asistente para varias páginas.<br/>                                                                                           |
| [**TDM \_ SET \_ BUTTON \_ ELEVATION \_ REQUIRED \_ STATE**](tdm-set-button-elevation-required-state.md) | Especifica si un botón de diálogo de tarea determinado o un vínculo de comando debe tener un icono de escudo de Control de cuentas de usuario (UAC); es decir, si la acción invocada por el botón requiere elevación. <br/> |
| [**TEXTO DEL \_ ELEMENTO SET \_ DE TDM \_**](tdm-set-element-text.md)                                         | Actualiza un elemento de texto en un cuadro de diálogo de tarea.<br/>                                                                                                                                                  |
| [**TDM \_ SET \_ MARQUEE \_ PROGRESS \_ BAR**](tdm-set-marquee-progress-bar.md)                        | Indica si la barra de progreso hospedada debe mostrarse en modo de marquesina.<br/>                                                                                                            |
| [**MARQUEE \_ DE LA BARRA DE PROGRESO DEL CONJUNTO \_ \_ \_ DE TDM**](tdm-set-progress-bar-marquee.md)                        | Inicia y detiene la presentación de marquesina de la barra de progreso y establece la velocidad de la marquesina.<br/>                                                                                              |
| [**TDM \_ SET \_ PROGRESS \_ BAR \_ POS**](tdm-set-progress-bar-pos.md)                                | Establece la posición actual de una barra de progreso.<br/>                                                                                                                                             |
| [**INTERVALO DE BARRAS \_ DE PROGRESO DEL CONJUNTO \_ \_ DE \_ TDM**](tdm-set-progress-bar-range.md)                            | Establece los valores mínimo y máximo de la barra de progreso hospedada.<br/>                                                                                                                          |
| [**ESTADO DE LA \_ BARRA DE PROGRESO DEL CONJUNTO \_ \_ DE \_ TDM**](tdm-set-progress-bar-state.md)                            | Establece el estado actual de la barra de progreso.<br/>                                                                                                                                               |
| [**TEXTO DEL \_ ELEMENTO UPDATE \_ DE TDM \_**](tdm-update-element-text.md)                                   | Actualiza un elemento de texto en un cuadro de diálogo de tarea. <br/>                                                                                                                                                 |
| [**ICONO DE ACTUALIZACIÓN DE TDM \_ \_**](tdm-update-icon.md)                                                    | Actualiza el icono de un cuadro de diálogo de tarea. <br/>                                                                                                                                                     |



 

### <a name="notifications"></a>Notificaciones



| Tema                                                           | Contenido                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CLIC EN EL BOTÓN TDN \_ \_](tdn-button-clicked.md)                  | Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón o un vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                   |
| [TDN \_ CREADO](tdn-created.md)                                 | Enviado por un cuadro de diálogo de tarea una vez creado el diálogo de tareas y antes de que se muestre. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                  |
| [TDN \_ DESTRUIDO](tdn-destroyed.md)                             | Enviado por un cuadro de diálogo de tarea cuando se destruye y su identificador de ventana ya no es válido. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                       |
| [DIÁLOGO DE TDN \_ \_ CONSTRUIDO](tdn-dialog-constructed.md)          | Enviado por un cuadro de diálogo de tarea una vez creado el diálogo de tareas y antes de que se muestre. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                  |
| [CLIC EN EL BOTÓN EXPANDIR DE TDN \_ \_ \_](tdn-expando-button-clicked.md) | Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en el botón expandir del cuadro de diálogo de tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                            |
| [TDN \_ HELP](tdn-help.md)                                       | Enviado por un cuadro de diálogo de tarea cuando el usuario presiona F1 en el teclado mientras el diálogo de tareas tiene el foco. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                            |
| [HIPERVÍNCULO DE TDN \_ EN EL QUE SE HA HECHO \_ CLIC](tdn-hyperlink-clicked.md)            | Enviado por un cuadro de diálogo de tarea cuando el usuario hace clic en un hipervínculo en el contenido del cuadro de diálogo de la tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                        |
| [TDN \_ NAVIGATED](tdn-navigated.md)                             | Enviado por un cuadro de diálogo de tarea cuando se ha producido una navegación. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                                                     |
| [BOTÓN DE RADIO TDN \_ EN EL QUE SE HA HECHO \_ \_ CLIC](tdn-radio-button-clicked.md)     | Enviado por un cuadro de diálogo de tarea cuando el usuario selecciona un botón o un vínculo de comando en el cuadro de diálogo de tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) <br/>                                                                                                                                                                                                  |
| [TEMPORIZADOR de \_ TDN](tdn-timer.md)                                     | Enviado por un cuadro de diálogo de tarea aproximadamente cada 200 milisegundos. Este código de notificación se envía cuando se ha establecido la marca TDF CALLBACK TIMER en el miembro dwFlags de la estructura TASKDIALOGCONFIG que se pasó a la \_ \_ función [**TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)  [](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el **método TaskDialogIndirect.**<br/> |
| [COMPROBACIÓN DE TDN \_ EN LA QUE SE HA HECHO \_ CLIC](tdn-verification-clicked.md)      | Enviado por el cuadro de diálogo de tarea cuando el usuario hace clic en la casilla de verificación del cuadro de diálogo de tarea. Este código de notificación solo se recibe a través de la función de devolución de llamada del cuadro de diálogo de tarea, que se puede registrar mediante el [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)<br/>                                                                                                                                                                                                       |



 

### <a name="structures"></a>Estructuras



| Tema                                           | Contenido                                                                                                                                                   |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BOTÓN \_ TASKDIALOG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialog_button) | Contiene información utilizada para mostrar un botón en un cuadro de diálogo de tarea. La [**estructura TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) usa esta estructura.<br/> |
| [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)    | Contiene información utilizada para mostrar un cuadro de diálogo de tarea. La [**función TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) usa esta estructura.<br/>          |



 

 

