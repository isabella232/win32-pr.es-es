---
title: Aceleradores de teclado
description: En esta sección se deba a los aceleradores de teclado. Un acelerador de teclado es una pulsación de tecla o una combinación de pulsaciones de tecla que genera un mensaje de comando para una aplicación.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\keyboardaccelerators.htm
keywords:
- entrada de usuario, aceleradores de teclado
- capturar la entrada del usuario, los aceleradores de teclado
- aceleradores de teclado
- Aceleradores
- WM_COMMAND mensaje
- WM_SYS comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df67f4879edc2e0e81a8715155bf2edfac05f1e5ce9d3557f9b051ae682a6afa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734473"
---
# <a name="keyboard-accelerators"></a>Aceleradores de teclado

Un *acelerador de* teclado (o, simplemente, acelerador) es una pulsación de teclas o una combinación de pulsaciones de tecla que genera un mensaje WM [**\_ COMMAND**](wm-command.md) o [**WM \_ SYSCOMMAND**](wm-syscommand.md) para una aplicación.

### <a name="in-this-section"></a>En esta sección



| Nombre                                                                 | Descripción                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Acerca de los aceleradores de teclado](about-keyboard-accelerators.md)       | Describe los aceleradores de teclado.<br/>                                |
| [Uso de aceleradores de teclado](using-keyboard-accelerators.md)       | Describe las tareas asociadas a los aceleradores de teclado.<br/> |
| [Referencia del acelerador de teclado](keyboard-accelerator-reference.md) | Contiene la referencia de API.<br/>                                     |



 

### <a name="keyboard-accelerator-functions"></a>Funciones del acelerador de teclado



| Nombre                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea)       | Copia la tabla de aceleradores especificada. Esta función se usa para obtener los datos de accelerator-table que corresponden a un identificador accelerator-table o para determinar el tamaño de los datos de accelerator-table. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea)   | Crea una tabla de aceleradores. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) | Destruye una tabla de aceleradores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa)               | Carga la tabla de aceleradores especificada. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)       | Procesa las teclas de aceleración para los comandos de menú. La función convierte un mensaje [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) o [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) en un mensaje WM [**\_ COMMAND**](wm-command.md) o [**WM \_ SYSCOMMAND**](wm-syscommand.md) (si hay una entrada para la clave en la tabla de aceleradores especificada) y, a continuación, envía el mensaje **WM \_ COMMAND** o **WM \_ SYSCOMMAND** directamente al procedimiento de ventana especificado. [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) no devuelve hasta que el procedimiento de ventana haya procesado el mensaje. <br/> |



 

### <a name="keyboard-accelerator-messages"></a>Mensajes del acelerador de teclado



| Nombre                                          | Descripción                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) | Se envía para indicar que se debe cambiar el estado de la interfaz de usuario.<br/>                                                                                                                                                                                                                                                  |
| [**WM \_ INITMENU**](wm-initmenu.md)           | Se envía cuando un menú está a punto de activarse. Se produce cuando el usuario hace clic en un elemento de la barra de menús o presiona una tecla de menú. Esto permite a la aplicación modificar el menú antes de que se muestre. <br/> Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) <br/> |
| [**WM \_ QUERYUISTATE**](wm-queryuistate.md)   | Se envía para recuperar el estado de la interfaz de usuario de una ventana.<br/>                                                                                                                                                                                                                                                            |
| [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) | Se envía para cambiar el estado de la interfaz de usuario para la ventana especificada y todas sus ventanas secundarias.<br/>                                                                                                                                                                                                                        |



 

### <a name="keyboard-accelerator-notifications"></a>Notificaciones del acelerador de teclado



| Nombre                                          | Descripción                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) | Se envía cuando un menú desplegable o submenú está a punto de activarse. Esto permite a una aplicación modificar el menú antes de que se muestre, sin cambiar todo el menú. <br/>                                                                                                                                              |
| [**WM \_ MENUCHAR**](wm-menuchar.md)           | Se envía cuando un menú está activo y el usuario presiona una tecla que no se corresponde con ninguna tecla mnemotécnica o de aceleración. Este mensaje se envía a la ventana propietaria del menú. <br/>                                                                                                                                             |
| [**MENÚ \_ WMSELECCIONAR**](wm-menuselect.md)       | Se envía a la ventana de propietario de un menú cuando el usuario selecciona un elemento de menú. <br/>                                                                                                                                                                                                                                                      |
| [**WM \_ SYSCHAR**](wm-syschar.md)             | Se publica en la ventana con el foco del teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje [**\_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) de WM. Especifica el código de carácter de una tecla de carácter del sistema, es decir, una tecla de carácter que se presiona mientras la tecla ALT está abajo. <br/> |
| [**WM \_ SYSCOMMAND**](wm-syscommand.md)       | Una ventana recibe este mensaje cuando el  usuario elige un comando en el menú Ventana o cuando el usuario elige el botón maximizar, minimizar, restaurar o cerrar botón.<br/>                                                                                                                                |



 

### <a name="keyboard-accelerator-structures"></a>Estructuras del acelerador de teclado



| Nombre                   | Descripción                                                          |
|------------------------|----------------------------------------------------------------------|
| [**Accel**](/windows/win32/api/winuser/ns-winuser-accel) | Define una tecla de aceleración utilizada en una tabla de aceleradores. <br/> |



 

 

