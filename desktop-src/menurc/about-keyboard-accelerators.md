---
title: Acerca de los aceleradores de teclado
description: En este tema se deba a los aceleradores de teclado.
ms.assetid: cbf7619d-289d-40c9-9a06-6ce47026d43f
keywords:
- Windows Interfaz de usuario,entrada del usuario
- Windows Interfaz de usuario,aceleradores de teclado
- entrada de usuario, aceleradores de teclado
- captura de entrada de usuario, aceleradores de teclado
- aceleradores de teclado
- Aceleradores
- WM_COMMAND mensaje
- WM_SYS comando
- tablas de aceleradores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b81240feb0ca21028c9d1813f4c8004e1c3bb932fe1ec8767e3719c26e7a5db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870741"
---
# <a name="about-keyboard-accelerators"></a>Acerca de los aceleradores de teclado

Los aceleradores están estrechamente relacionados con los menús: ambos proporcionan al usuario acceso al conjunto de comandos de una aplicación. Normalmente, los usuarios se basan en los menús de una aplicación para aprender el conjunto de comandos y, a continuación, cambiar al uso de aceleradores a medida que se vuelven más expertos con la aplicación. Los aceleradores proporcionan un acceso más rápido y directo a los comandos que los menús. Como mínimo, una aplicación debe proporcionar aceleradores para los comandos más usados. Aunque los aceleradores suelen generar comandos que existen como elementos de menú, también pueden generar comandos que no tienen elementos de menú equivalentes.

En esta sección se tratan los temas siguientes.

-   [Tablas de aceleradores](#accelerator-tables)
-   [Creación de tablas de acelerador](#accelerator-table-creation)
-   [Asignaciones de pulsaciones de teclas de acelerador](#accelerator-keystroke-assignments)
-   [Aceleradores y menús](#accelerators-and-menus)
-   [Estado de la interfaz de usuario](#ui-state)

## <a name="accelerator-tables"></a>Tablas de aceleradores

Una tabla de aceleradores consta de una matriz de estructuras [**ACCEL,**](/windows/win32/api/winuser/ns-winuser-accel) cada una de las que define un acelerador individual. Cada **estructura accel** incluye la siguiente información:

-   Combinación de pulsación de teclas del acelerador.
-   Identificador del acelerador.
-   Varias marcas. Esto incluye uno que especifica si el sistema va a proporcionar comentarios visuales resaltando el elemento de menú correspondiente, si existe, cuando se usa el acelerador.

Para procesar pulsaciones de teclas de acelerador para un subproceso especificado, el desarrollador debe llamar a la función [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) en el bucle de mensajes asociado a la cola de mensajes del subproceso. La **función TranslateAccelerator supervisa** la entrada del teclado en la cola de mensajes, comprobando las combinaciones de teclas que coinciden con una entrada de la tabla de aceleradores. Cuando **TranslateAccelerator** encuentra una coincidencia, traduce la entrada de teclado (es decir, los mensajes [**\_ KEYUP**](/windows/desktop/inputdev/wm-keyup) y [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) de WM) en un mensaje [**WM \_ COMMAND**](wm-command.md) o [**WM \_ SYSCOMMAND**](wm-syscommand.md) y, a continuación, envía el mensaje al procedimiento de ventana de la ventana especificada. En la ilustración siguiente se muestra cómo se procesan los aceleradores.

![modelo de procesamiento del acelerador de teclado](images/cskac-01.png)

El [**mensaje \_ WM COMMAND**](wm-command.md) incluye el identificador del acelerador que [**provocó que TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) generara el mensaje. El procedimiento de ventana examina el identificador para determinar el origen del mensaje y, a continuación, procesa el mensaje en consecuencia.

Las tablas de aceleradores existen en dos niveles diferentes. El sistema mantiene una única tabla de aceleradores para todo el sistema que se aplica a todas las aplicaciones. Una aplicación no puede modificar la tabla de aceleradores del sistema. Para obtener una descripción de los aceleradores proporcionados por la tabla de aceleradores del sistema, vea [Accelerator Keystroke Assignments](#accelerator-keystroke-assignments).

El sistema también mantiene tablas de aceleradores para cada aplicación. Una aplicación puede definir cualquier número de tablas de aceleradores para su uso con sus propias ventanas. Un identificador único de 32 bits **(HACCEL)** identifica cada tabla. Sin embargo, solo una tabla de aceleradores puede estar activa a la vez para un subproceso especificado. El identificador de la tabla de aceleradores que se pasa a [**la función TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) determina qué tabla de aceleradores está activa para un subproceso. La tabla de aceleradores activa se puede cambiar en cualquier momento pasando un identificador de tabla de aceleradores diferente a **TranslateAccelerator.**

## <a name="accelerator-table-creation"></a>Accelerator-Table creación

Se requieren varios pasos para crear una tabla de aceleradores para una aplicación. En primer lugar, se usa un compilador de recursos para crear recursos de tabla de aceleradores y agregarlos al archivo ejecutable de la aplicación. En tiempo de ejecución, la [**función LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) se usa para cargar la tabla de aceleradores en la memoria y recuperar el identificador en la tabla de aceleradores. Este identificador se pasa a la [**función TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para activar la tabla de aceleradores.

También se puede crear una tabla de aceleradores para una aplicación en tiempo de ejecución pasando una matriz de estructuras [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) a la [**función CreateAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) Este método admite aceleradores definidos por el usuario en la aplicación. Al igual que la función [**LoadAccelerators,**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) **CreateAcceleratorTable** devuelve un identificador de tabla de aceleradores que se puede pasar a [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para activar la tabla de aceleradores.

El sistema destruye automáticamente las tablas de aceleradores cargadas por [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) o creadas [**por CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea). Sin embargo, una aplicación puede liberar recursos mientras se ejecuta mediante la destrucción de tablas de aceleradores que ya no son necesarias mediante una llamada a la [**función DestroyAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)

Se puede copiar y modificar una tabla de aceleradores existente. La tabla de aceleradores existente se copia mediante la [**función CopyAcceleratorTable.**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea) Una vez modificada la copia, se recupera un identificador de la nueva tabla de aceleradores mediante una llamada a [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea). Por último, el identificador se pasa [**a TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para activar la nueva tabla.

## <a name="accelerator-keystroke-assignments"></a>Asignaciones de pulsaciones de teclas de acelerador

Se puede usar un código de caracteres ASCII o un código de clave virtual para definir el acelerador. Un código de caracteres ASCII hace que el acelerador distingue mayúsculas de minúsculas. Por lo tanto, el uso del carácter ASCII "C" define el acelerador como ALT+C en lugar de ALT+c. Sin embargo, los aceleradores que distinguen mayúsculas de minúsculas pueden resultar confusos de usar. Por ejemplo, se generará el acelerador ALT+C si la tecla CAPS LOCK está fuera de servicio o si la tecla MAYÚS está fuera de servicio, pero no si ambas están fuera de servicio.

Normalmente, no es necesario que los aceleradores distinguen mayúsculas de minúsculas, por lo que la mayoría de las aplicaciones usan códigos de clave virtual para los aceleradores en lugar de códigos de caracteres ASCII.

Evite los aceleradores que entren en conflicto con los elementos mnemotécnicos del menú de una aplicación, ya que el acelerador invalida el mnemotécnico, lo que puede confundir al usuario. Para obtener más información sobre los menús mnemotécnicos, vea [Menús](menus.md).

Si una aplicación define un acelerador que también se define en la tabla del acelerador del sistema, el acelerador definido por la aplicación invalida el acelerador del sistema, pero solo dentro del contexto de la aplicación. Sin embargo, evite esta práctica, ya que impide que el acelerador del sistema realice su rol estándar en la interfaz de usuario. Los aceleradores de todo el sistema se describen en la lista siguiente:



| Acelerador                 | Descripción                                                                                                      |
|------------------|-------------------------------------------------------------------------------------------------------|
| ALT+ESC          | Cambia a la siguiente aplicación.                                                                     |
| ALT+F4           | Cierra una aplicación o una ventana.                                                                    |
| ALT+GUIÓN       | Abre el **menú Ventana** de una ventana de documento.                                                      |
| ALT+PANTALLA DE IMPRESIÓN | Copia una imagen de la ventana activa en el Portapapeles.                                              |
| ALT+Barra espaciadora     | Abre el **menú** Ventana de la ventana principal de la aplicación.                                          |
| ALT+TAB          | Cambia a la siguiente aplicación.                                                                     |
| CTRL+ESC         | Cambia al **menú** Inicio.                                                                       |
| CTRL+F4          | Cierra el grupo activo o la ventana del documento.                                                           |
| F1               | Inicia el archivo de ayuda de la aplicación, si existe alguno.                                                    |
| PANTALLA DE IMPRESIÓN     | Copia una imagen en la pantalla en el Portapapeles.                                                     |
| MAYÚS+ALT+TAB    | Cambia a la aplicación anterior. El usuario debe mantener presionada la tecla ALT+MAYÚS mientras presiona TAB. |



 

## <a name="accelerators-and-menus"></a>Aceleradores y menús

Usar un acelerador es lo mismo que elegir un elemento de menú: ambas acciones hacen que el sistema envíe un mensaje [**WM \_ COMMAND**](wm-command.md) o [**WM \_ SYSCOMMAND**](wm-syscommand.md) al procedimiento de ventana correspondiente. El **mensaje \_ WM COMMAND** incluye un identificador que el procedimiento de ventana examina para determinar el origen del mensaje. Si un acelerador generó el **mensaje \_ WM COMMAND,** el identificador es el del acelerador. De forma similar, si un elemento de menú generó el **mensaje \_ WM COMMAND,** el identificador es el del elemento de menú. Dado que un acelerador proporciona un acceso directo para elegir un comando de un menú, una aplicación normalmente asigna el mismo identificador al acelerador y al elemento de menú correspondiente.

Una aplicación procesa un mensaje [**WM \_ COMMAND**](wm-command.md) del acelerador exactamente de la misma manera que el mensaje **WM COMMAND del elemento de \_ menú** correspondiente. Sin embargo, el mensaje **\_ WM COMMAND** contiene una marca que especifica si el mensaje se originó en un acelerador o un elemento de menú, en caso de que los aceleradores se deban procesar de forma diferente a sus elementos de menú correspondientes. El [**mensaje \_ SYSCOMMAND de WM**](wm-syscommand.md) no contiene esta marca.

El identificador determina si un acelerador genera un mensaje [**\_ WM COMMAND**](wm-command.md) o WM [**\_ SYSCOMMAND.**](wm-syscommand.md) Si el identificador tiene el mismo valor que un elemento de menú en el menú Sistema, el acelerador genera un **mensaje \_ SYSCOMMAND de WM.** De lo contrario, el acelerador genera un **mensaje \_ WM COMMAND.**

Si un acelerador tiene el mismo identificador que un elemento de menú y el elemento de menú está atenuado o deshabilitado, el acelerador se deshabilita y no genera un mensaje [**WM \_ COMMAND**](wm-command.md) o [**WM \_ SYSCOMMAND.**](wm-syscommand.md) Además, un acelerador no genera un mensaje de comando si se minimiza la ventana correspondiente.

Cuando el usuario usa un acelerador que corresponde a un elemento de menú, el procedimiento de ventana recibe los mensajes [**WM \_ INITMENU**](wm-initmenu.md) y [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) como si el usuario hubiera seleccionado el elemento de menú. Para obtener información sobre cómo procesar estos mensajes, vea [Menús](menus.md).

Un acelerador que se corresponde con un elemento de menú debe incluirse en el texto del elemento de menú.

## <a name="ui-state"></a>Estado de la interfaz de usuario

Windows permite a las aplicaciones ocultar o mostrar varias características en su interfaz de usuario. Esta configuración se conoce como estado de la interfaz de usuario. El estado de la interfaz de usuario incluye la siguiente configuración:

-   indicadores de foco (como rectángulos de foco en botones)
-   aceleradores de teclado (indicados por subrayados en las etiquetas de control)

Una ventana puede enviar mensajes para solicitar un cambio en el estado de la interfaz de usuario, puede consultar el estado de la interfaz de usuario o aplicar un determinado estado para sus ventanas secundarias. Estos mensajes son los siguientes.



| Message                                       | Descripción                                |
|-----------------------------------------------|--------------------------------------------|
| [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) | Indica que el estado de la interfaz de usuario debe cambiar. |
| [**WM \_ QUERYUISTATE**](wm-queryuistate.md)   | Recupera el estado de la interfaz de usuario de una ventana.       |
| [**WM \_ UPDATEUISTATE**](wm-updateuistate.md) | Cambia el estado de la interfaz de usuario.                      |



 

De forma predeterminada, todas las ventanas secundarias de una ventana de nivel superior se crean con el mismo estado de interfaz de usuario que su elemento primario.

El sistema controla el estado de la interfaz de usuario de los controles de los cuadros de diálogo. Al crear el cuadro de diálogo, el sistema inicializa el estado de la interfaz de usuario en consecuencia. Todos los controles secundarios heredan este estado. Una vez creado el cuadro de diálogo, el sistema supervisa las pulsaciones de tecla del usuario. Si la configuración del estado de la interfaz de usuario está oculta y el usuario navega con el teclado, el sistema actualiza el estado de la interfaz de usuario. Por ejemplo, si el usuario presiona la tecla Tab para mover el foco al siguiente control, el sistema llama a [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) para que los indicadores de foco sean visibles. Si el usuario presiona la tecla Alt, el sistema llama a **WM \_ CHANGEUISTATE** para que los aceleradores de teclado sean visibles.

Si un control admite la navegación entre los elementos de la interfaz de usuario que contiene, puede actualizar su propio estado de la interfaz de usuario. El control puede llamar a [**WM \_ QUERYUISTATE para**](wm-queryuistate.md) recuperar y almacenar en caché el estado inicial de la interfaz de usuario. Cada vez que el control recibe un [**mensaje \_ UPDATEUISTATE**](wm-updateuistate.md) de WM, puede actualizar su estado de la interfaz de usuario y enviar un mensaje [**\_ CHANGEUISTATE**](wm-changeuistate.md) de WM a su elemento primario. Cada ventana seguirá envíando el mensaje a su elemento primario hasta que llegue a la ventana de nivel superior. La ventana de nivel superior envía el **mensaje \_ UPDATEUISTATE de WM** a las ventanas del árbol de ventana. Si una ventana no pasa el mensaje **\_ CHANGEUISTATE** de WM, no alcanzará la ventana de nivel superior y el estado de la interfaz de usuario no se actualizará.

 

 