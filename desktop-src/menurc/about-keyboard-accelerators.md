---
title: Acerca de los aceleradores de teclado
description: En este tema se describen los aceleradores de teclado.
ms.assetid: cbf7619d-289d-40c9-9a06-6ce47026d43f
keywords:
- Interfaz de usuario de Windows, entrada de usuario
- Interfaz de usuario de Windows, aceleradores de teclado
- entrada de usuario, aceleradores de teclado
- captura de entradas de usuario, aceleradores de teclado
- aceleradores de teclado
- aceleradores
- Mensaje WM_COMMAND
- WM_SYS mensaje de comando
- tablas de aceleradores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9c89301f58d7d76b5d9b28dd6835850c0674db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995137"
---
# <a name="about-keyboard-accelerators"></a>Acerca de los aceleradores de teclado

Los aceleradores están estrechamente relacionados con los menús; ambos proporcionan al usuario acceso al conjunto de comandos de una aplicación. Normalmente, los usuarios se basan en los menús de una aplicación para conocer el conjunto de comandos y, a continuación, cambiar al uso de aceleradores a medida que se vuelven más expertos en la aplicación. Los aceleradores proporcionan un acceso más rápido y directo a los comandos que los menús. Como mínimo, una aplicación debe proporcionar aceleradores para los comandos más usados. Aunque los aceleradores generan normalmente comandos que existen como elementos de menú, también pueden generar comandos que no tienen elementos de menú equivalentes.

En esta sección se tratan los temas siguientes.

-   [Tablas de aceleradores](#accelerator-tables)
-   [Acelerador: creación de tablas](#accelerator-table-creation)
-   [Asignaciones de pulsaciones de teclas del acelerador](#accelerator-keystroke-assignments)
-   [Aceleradores y menús](#accelerators-and-menus)
-   [Estado de la interfaz de usuario](#ui-state)

## <a name="accelerator-tables"></a>Tablas de aceleradores

Una tabla de aceleradores consta de una matriz de estructuras de [**aceleración**](/windows/win32/api/winuser/ns-winuser-accel) , cada una de las cuales define un acelerador individual. Cada estructura de **aceleración** incluye la siguiente información:

-   Combinación de teclas del acelerador.
-   Identificador del acelerador.
-   Varias marcas. Esto incluye una que especifica si el sistema debe proporcionar comentarios visuales resaltando el elemento de menú correspondiente, si existe, cuando se utiliza el acelerador.

Para procesar las pulsaciones de teclas de aceleración de un subproceso especificado, el desarrollador debe llamar a la función [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) en el bucle de mensajes asociado a la cola de mensajes del subproceso. La función **TranslateAccelerator** supervisa la entrada del teclado en la cola de mensajes, comprobando las combinaciones de teclas que coinciden con una entrada de la tabla de aceleradores. Cuando **TranslateAccelerator** encuentra una coincidencia, convierte la entrada del teclado (es decir, los mensajes de [**KEYDOWN \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) y [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) ) en un [**\_ comando de WM**](wm-command.md) o en un mensaje de [**\_ SYSCOMMAND de WM**](wm-syscommand.md) y, a continuación, envía el mensaje al procedimiento de ventana de la ventana especificada. En la ilustración siguiente se muestra cómo se procesan los aceleradores.

![modelo de procesamiento de aceleradores de teclado](images/cskac-01.png)

El mensaje de [**\_ comando de WM**](wm-command.md) incluye el identificador del acelerador que causó que [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) genere el mensaje. El procedimiento de ventana examina el identificador para determinar el origen del mensaje y, a continuación, procesa el mensaje en consecuencia.

Las tablas de aceleradores existen en dos niveles diferentes. El sistema mantiene una única tabla de aceleradores para todo el sistema que se aplica a todas las aplicaciones. Una aplicación no puede modificar la tabla de aceleradores del sistema. Para obtener una descripción de los aceleradores proporcionados por la tabla de aceleradores del sistema, consulte [asignaciones de pulsaciones de teclas del acelerador](#accelerator-keystroke-assignments).

El sistema también mantiene las tablas de aceleradores para cada aplicación. Una aplicación puede definir cualquier número de tablas de aceleradores para su uso con sus propias ventanas. Un identificador único de 32 bits (**HACCEL**) identifica cada tabla. Sin embargo, solo una tabla de aceleradores puede estar activa a la vez para un subproceso especificado. El identificador de la tabla de aceleradores que se pasa a la función [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) determina qué tabla de aceleradores está activa para un subproceso. La tabla de aceleradores activa se puede cambiar en cualquier momento pasando un identificador de tabla de aceleradores distinto a **TranslateAccelerator**.

## <a name="accelerator-table-creation"></a>Creación de Accelerator-Table

Se requieren varios pasos para crear una tabla de aceleradores para una aplicación. En primer lugar, se usa un compilador de recursos para crear recursos de tabla de aceleradores y agregarlos al archivo ejecutable de la aplicación. En tiempo de ejecución, la función [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) se usa para cargar la tabla de aceleradores en la memoria y recuperar el identificador de la tabla de aceleradores. Este identificador se pasa a la función [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para activar la tabla de aceleradores.

También se puede crear una tabla de aceleradores para una aplicación en tiempo de ejecución si se pasa una matriz de estructuras de [**aceleración**](/windows/win32/api/winuser/ns-winuser-accel) a la función [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) . Este método admite aceleradores definidos por el usuario en la aplicación. Al igual que la función [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , **CreateAcceleratorTable** devuelve un identificador de tabla de aceleradores que se puede pasar a [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para activar la tabla de aceleradores.

El sistema destruye automáticamente las tablas de aceleradores cargados por [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) o creadas por [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea). Sin embargo, una aplicación puede liberar recursos mientras se está ejecutando mediante la destrucción de tablas de aceleradores que ya no son necesarios llamando a la función [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .

Se puede copiar y modificar una tabla de aceleradores existente. La tabla de aceleradores existente se copia mediante la función [**CopyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-copyacceleratortablea) . Una vez modificada la copia, se recupera un identificador de la nueva tabla de aceleradores mediante una llamada a [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea). Por último, el identificador se pasa a [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) para activar la nueva tabla.

## <a name="accelerator-keystroke-assignments"></a>Asignaciones de pulsaciones de teclas del acelerador

Se puede usar un código de carácter ASCII o un código de tecla virtual para definir el acelerador. Un código de carácter ASCII hace que la distinción entre mayúsculas y minúsculas sea sensible. Por lo tanto, el uso del carácter ASCII "C" define el acelerador como ALT + C en lugar de ALT + c. Sin embargo, los aceleradores que distinguen mayúsculas de minúsculas pueden ser confusos. Por ejemplo, se generará el acelerador ALT + C si la tecla Bloq Mayús está presionada o si la tecla Mayús está presionada, pero no si ambos están inactivos.

Normalmente, los aceleradores no tienen que distinguir entre mayúsculas y minúsculas, por lo que la mayoría de las aplicaciones usan códigos de tecla virtual para los aceleradores en lugar de códigos de caracteres ASCII.

Evite los aceleradores que entran en conflicto con las teclas de menú de una aplicación, ya que el acelerador invalida la tecla de método, que puede confundir al usuario. Para obtener más información sobre las teclas de menú, vea [menús](menus.md).

Si una aplicación define un acelerador que también se define en la tabla de aceleradores del sistema, el acelerador definido por la aplicación invalida el acelerador del sistema, pero solo dentro del contexto de la aplicación. No obstante, evite esta práctica, ya que impide que el acelerador del sistema realice su rol estándar en la interfaz de usuario. Los aceleradores para todo el sistema se describen en la lista siguiente:



|                  |                                                                                                       |
|------------------|-------------------------------------------------------------------------------------------------------|
| ALT+ESC          | Cambia a la siguiente aplicación.                                                                     |
| ALT+F4           | Cierra una aplicación o una ventana.                                                                    |
| ALT+GUIÓN       | Abre el menú **ventana** de una ventana de documento.                                                      |
| ALT + IMPR PANT | Copia una imagen de la ventana activa en el portapapeles.                                              |
| ALT+Barra espaciadora     | Abre el menú **ventana** de la ventana principal de la aplicación.                                          |
| ALT+TAB          | Cambia a la siguiente aplicación.                                                                     |
| CTRL+ESC         | Cambia al menú **Inicio** .                                                                       |
| CTRL+F4          | Cierra la ventana de documento o el grupo activo.                                                           |
| F1               | Inicia el archivo de ayuda de la aplicación, si existe.                                                    |
| IMPR PANT     | Copia una imagen de la pantalla en el portapapeles.                                                     |
| MAYÚS + ALT + TAB    | Cambia a la aplicación anterior. El usuario debe presionar y mantener presionada la tecla ALT + MAYÚS mientras presiona la tecla TAB. |



 

## <a name="accelerators-and-menus"></a>Aceleradores y menús

El uso de un acelerador es el mismo que cuando se elige un elemento de menú: ambas acciones hacen que el sistema envíe un [**\_ comando de WM**](wm-command.md) o un mensaje de [**WM \_ SYSCOMMAND**](wm-syscommand.md) al procedimiento de ventana correspondiente. El mensaje de **\_ comando de WM** incluye un identificador que el procedimiento de ventana examina para determinar el origen del mensaje. Si un acelerador genera el mensaje del **\_ comando de WM** , el identificador es el del acelerador. Del mismo modo, si un elemento de menú ha generado el mensaje de **\_ comando de WM** , el identificador es el del elemento de menú. Dado que un acelerador proporciona un acceso directo para elegir un comando de un menú, una aplicación normalmente asigna el mismo identificador al acelerador y al elemento de menú correspondiente.

Una aplicación procesa un mensaje [**del \_ comando WM**](wm-command.md) de acelerador exactamente de la misma manera que el mensaje de **\_ comando de WM** del elemento de menú correspondiente. Sin embargo, el mensaje de **\_ comando de WM** contiene una marca que especifica si el mensaje se originó a partir de un acelerador o un elemento de menú, en el caso de que los aceleradores se deben procesar de forma diferente a los elementos de menú correspondientes. El mensaje de [**\_ SYSCOMMAND de WM**](wm-syscommand.md) no contiene esta marca.

El identificador determina si un acelerador genera un [**\_ comando de WM**](wm-command.md) o un mensaje de [**\_ SYSCOMMAND de WM**](wm-syscommand.md) . Si el identificador tiene el mismo valor que un elemento de menú del menú sistema, el acelerador genera un mensaje de **\_ SYSCOMMAND de WM** . De lo contrario, el acelerador genera un mensaje de **\_ comando de WM** .

Si un acelerador tiene el mismo identificador que un elemento de menú y el elemento de menú está atenuado o deshabilitado, el acelerador está deshabilitado y no genera un [**\_ comando de WM**](wm-command.md) o un mensaje de [**\_ SYSCOMMAND de WM**](wm-syscommand.md) . Además, un acelerador no genera un mensaje de comando si se minimiza la ventana correspondiente.

Cuando el usuario usa un acelerador que corresponde a un elemento de menú, el procedimiento de ventana recibe los mensajes de [**WM \_ INITMENU**](wm-initmenu.md) y [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) como si el usuario hubiera seleccionado el elemento de menú. Para obtener información sobre cómo procesar estos mensajes, vea [menús](menus.md).

Un acelerador que corresponde a un elemento de menú debe incluirse en el texto del elemento de menú.

## <a name="ui-state"></a>Estado de la interfaz de usuario

Windows permite a las aplicaciones ocultar o mostrar varias características en su interfaz de usuario. Esta configuración se conoce como estado de la interfaz de usuario. El estado de la interfaz de usuario incluye la configuración siguiente:

-   indicadores de foco (como rectángulos de foco en botones)
-   aceleradores de teclado (indicados mediante subrayados en etiquetas de control)

Una ventana puede enviar mensajes para solicitar un cambio en el estado de la interfaz de usuario, puede consultar el estado de la interfaz de usuario o aplicar un estado determinado para sus ventanas secundarias. Estos mensajes son los siguientes.



| Message                                       | Descripción                                |
|-----------------------------------------------|--------------------------------------------|
| [**CHANGEUISTATE de WM \_**](wm-changeuistate.md) | Indica que el estado de la interfaz de usuario debería cambiar. |
| [**QUERYUISTATE de WM \_**](wm-queryuistate.md)   | Recupera el estado de la interfaz de usuario de una ventana.       |
| [**UPDATEUISTATE de WM \_**](wm-updateuistate.md) | Cambia el estado de la interfaz de usuario.                      |



 

De forma predeterminada, todas las ventanas secundarias de una ventana de nivel superior se crean con el mismo estado de la interfaz de usuario que su elemento primario.

El sistema controla el estado de la interfaz de usuario para los controles de los cuadros de diálogo. Al crear el cuadro de diálogo, el sistema inicializa el estado de la interfaz de usuario en consecuencia. Todos los controles secundarios heredan este estado. Una vez creado el cuadro de diálogo, el sistema supervisa las pulsaciones de teclas del usuario. Si la configuración de estado de la interfaz de usuario está oculta y el usuario navega con el teclado, el sistema actualiza el estado de la interfaz de usuario. Por ejemplo, si el usuario presiona la tecla TAB para desplazar el foco al control siguiente, el sistema llama a [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) para que los indicadores de foco sean visibles. Si el usuario presiona la tecla Alt, el sistema llama a **WM \_ CHANGEUISTATE** para que los aceleradores de teclado sean visibles.

Si un control admite la navegación entre los elementos de la interfaz de usuario que contiene, puede actualizar su propio estado de la interfaz de usuario. El control puede llamar a [**WM \_ QUERYUISTATE**](wm-queryuistate.md) para recuperar y almacenar en caché el estado inicial de la interfaz de usuario. Siempre que el control recibe un mensaje de [**\_ UPDATEUISTATE de WM**](wm-updateuistate.md) , puede actualizar su estado de la interfaz de usuario y enviar un mensaje de [**WM \_ CHANGEUISTATE**](wm-changeuistate.md) a su elemento primario. Cada ventana seguirá enviando el mensaje a su elemento primario hasta que llegue a la ventana de nivel superior. La ventana de nivel superior envía el mensaje de **\_ UPDATEUISTATE de WM** a las ventanas en el árbol de ventanas. Si una ventana no pasa el mensaje de **\_ CHANGEUISTATE de WM** , no llegará a la ventana de nivel superior y no se actualizará el estado de la interfaz de usuario.

 

 