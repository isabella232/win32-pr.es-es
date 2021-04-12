---
title: Aceleradores de teclado
description: En esta sección se describen los aceleradores de teclado. Una tecla de aceleración es una pulsación o combinación de pulsaciones de teclas que genera un mensaje de comando para una aplicación.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators.htm
keywords:
- entrada de usuario, aceleradores de teclado
- captura de entradas de usuario, aceleradores de teclado
- aceleradores de teclado
- aceleradores
- Mensaje WM_COMMAND
- WM_SYS mensaje de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd8cecd2fc1273750c75b8e5f33106d22343a14
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420680"
---
# <a name="keyboard-accelerators"></a>Aceleradores de teclado

Una tecla de *aceleración* (o, simplemente, acelerador) es una pulsación o combinación de pulsaciones de teclas que genera un [**\_ comando de WM**](wm-command.md) o un mensaje de [**\_ SYSCOMMAND de WM**](wm-syscommand.md) para una aplicación.

### <a name="in-this-section"></a>En esta sección



| Nombre                                                                 | Descripción                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Acerca de los aceleradores de teclado](about-keyboard-accelerators.md)       | Describe los aceleradores de teclado.<br/>                                |
| [Usar aceleradores de teclado](using-keyboard-accelerators.md)       | Describe las tareas que están asociadas a los aceleradores de teclado.<br/> |
| [Referencia de acelerador de teclado](keyboard-accelerator-reference.md) | Contiene la referencia de la API.<br/>                                     |



 

### <a name="keyboard-accelerator-functions"></a>Funciones de acelerador de teclado



| Nombre                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea)       | Copia la tabla de aceleradores especificada. Esta función se usa para obtener los datos de la tabla de aceleradores que corresponden a un identificador de tabla de aceleradores, o para determinar el tamaño de los datos de la tabla de aceleradores. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)   | Crea una tabla de aceleradores. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) | Destruye una tabla de aceleradores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa)               | Carga la tabla de aceleradores especificada. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)       | Procesa las teclas de aceleración de los comandos de menú. La función traduce un mensaje de [**\_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) o de WM [**\_ de WM a**](/windows/desktop/inputdev/wm-keydown) un [**\_ comando de WM**](wm-command.md) o a un mensaje de [**WM \_ SYSCOMMAND**](wm-syscommand.md) (si hay una entrada para la clave en la tabla de aceleradores especificada) y, a continuación, envía el **\_ comando de WM** o el mensaje de **WM \_ SYSCOMMAND** directamente al procedimiento de ventana especificado. [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) no vuelve hasta que el procedimiento de ventana haya procesado el mensaje. <br/> |



 

### <a name="keyboard-accelerator-messages"></a>Mensajes del acelerador de teclado



| Nombre                                          | Descripción                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHANGEUISTATE de WM \_**](wm-changeuistate.md) | Se envía para indicar que se debe cambiar el estado de la interfaz de usuario.<br/>                                                                                                                                                                                                                                                  |
| [**INITMENU de WM \_**](wm-initmenu.md)           | Se envía cuando un menú está a punto de activarse. Se produce cuando el usuario hace clic en un elemento de la barra de menús o presiona una tecla de menú. Esto permite que la aplicación modifique el menú antes de que se muestre. <br/> Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |
| [**QUERYUISTATE de WM \_**](wm-queryuistate.md)   | Se envía para recuperar el estado de la interfaz de usuario de una ventana.<br/>                                                                                                                                                                                                                                                            |
| [**UPDATEUISTATE de WM \_**](wm-updateuistate.md) | Se envía para cambiar el estado de la interfaz de usuario de la ventana especificada y de todas sus ventanas secundarias.<br/>                                                                                                                                                                                                                        |



 

### <a name="keyboard-accelerator-notifications"></a>Notificaciones del acelerador de teclado



| Nombre                                          | Descripción                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INITMENUPOPUP de WM \_**](wm-initmenupopup.md) | Se envía cuando un menú desplegable o un submenú está a punto de activarse. Esto permite que una aplicación modifique el menú antes de que se muestre, sin cambiar todo el menú. <br/>                                                                                                                                              |
| [**MENUCHAR de WM \_**](wm-menuchar.md)           | Se envía cuando un menú está activo y el usuario presiona una tecla que no se corresponde con ninguna tecla de método abreviado o tecla de aceleración. Este mensaje se envía a la ventana que posee el menú. <br/>                                                                                                                                             |
| [**MENUSELECT de WM \_**](wm-menuselect.md)       | Se envía a la ventana propietaria de un menú cuando el usuario selecciona un elemento de menú. <br/>                                                                                                                                                                                                                                                      |
| [**SYSCHAR de WM \_**](wm-syschar.md)             | Se envía a la ventana con el foco de teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje de [**\_ SYSKEYDOWN de WM**](/windows/desktop/inputdev/wm-syskeydown) . Especifica el código de carácter de una tecla de carácter del sistema, que es una tecla de carácter que se presiona mientras la tecla ALT está presionada. <br/> |
| [**SYSCOMMAND de WM \_**](wm-syscommand.md)       | Una ventana recibe este mensaje cuando el usuario elige un comando en el menú **ventana** o cuando el usuario elige el botón maximizar, el botón minimizar, el botón Restaurar o el botón Cerrar.<br/>                                                                                                                                |



 

### <a name="keyboard-accelerator-structures"></a>Estructuras de aceleradores de teclado



| Nombre                   | Descripción                                                          |
|------------------------|----------------------------------------------------------------------|
| [**FONÉTICA**](/windows/win32/api/winuser/ns-winuser-accel) | Define una tecla de aceleración utilizada en una tabla de aceleradores. <br/> |



 

 

