---
description: Cada documento de una aplicación de interfaz de múltiples documentos (MDI) se muestra en una ventana secundaria independiente dentro del área cliente de la ventana principal de la aplicación.
ms.assetid: 35dff281-3b11-4954-85cf-a0f1c9ed346a
title: Acerca de la interfaz de varios documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0397127d7ec343ebdb7696c2dd7d57204a5d5ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669871"
---
# <a name="about-the-multiple-document-interface"></a>Acerca de la interfaz de varios documentos

Cada documento de una aplicación de interfaz de múltiples documentos (MDI) se muestra en una ventana secundaria independiente dentro del área cliente de la ventana principal de la aplicación. Las aplicaciones MDI típicas incluyen aplicaciones de procesamiento de texto que permiten al usuario trabajar con varios documentos de texto y aplicaciones de hojas de cálculo que permiten al usuario trabajar con varios gráficos y hojas de cálculo. Para obtener más información, vea los siguientes temas.

-   [Ventanas de marco, cliente y secundaria](#frame-client-and-child-windows)
-   [Creación de ventanas secundarias](#child-window-creation)
-   [Activación de la ventana secundaria](#child-window-activation)
-   [Menús de varios documentos](#multiple-document-menus)
-   [Varios aceleradores de documentos](#multiple-document-accelerators)
-   [Tamaño y organización de la ventana secundaria](#child-window-size-and-arrangement)
-   [Ventanas de título de icono](#icon-title-windows)
-   [Datos de la ventana secundaria](#child-window-data)
    -   [Estructura de ventana](#window-structure)
    -   [Propiedades de la ventana](#window-properties)

## <a name="frame-client-and-child-windows"></a>Ventanas de marco, cliente y secundaria

Una aplicación MDI tiene tres tipos de ventanas: una ventana de marco, una ventana de cliente MDI, así como varias ventanas secundarias. La *ventana marco* es similar a la ventana principal de la aplicación: tiene un borde de tamaño, una barra de título, un menú ventana, un botón minimizar y un botón maximizar. La aplicación debe registrar una clase de ventana para la ventana de marco y proporcionar un procedimiento de ventana para que sea compatible.

Una aplicación MDI no muestra los resultados en el área cliente de la ventana de marco. En su lugar, muestra la ventana del cliente MDI. Una *ventana de cliente MDI* es un tipo especial de ventana secundaria que pertenece a **la clase de** ventana registrada previamente. La ventana de cliente es un elemento secundario de la ventana de marco. sirve como fondo para las ventanas secundarias. También proporciona compatibilidad para crear y manipular ventanas secundarias. Por ejemplo, una aplicación MDI puede crear, activar o maximizar las ventanas secundarias mediante el envío de mensajes a la ventana del cliente MDI.

Cuando el usuario abre o crea un documento, la ventana de cliente crea una ventana secundaria para el documento. La ventana de cliente es la ventana primaria de todas las ventanas secundarias MDI de la aplicación. Cada ventana secundaria tiene un borde de tamaño, una barra de título, un menú ventana, un botón minimizar y un botón maximizar. Dado que se recorta una ventana secundaria, se limita a la ventana del cliente y no puede aparecer fuera de ella.

Una aplicación MDI puede admitir más de un tipo de documento. Por ejemplo, una aplicación de hoja de cálculo típica permite al usuario trabajar con gráficos y hojas de cálculo. Para cada tipo de documento que admita, una aplicación MDI debe registrar una clase de ventana secundaria y proporcionar un procedimiento de ventana para admitir las ventanas que pertenecen a esa clase. Para obtener más información sobre las clases de ventana, vea [clases de ventana](window-classes.md). Para obtener más información acerca de los procedimientos de ventana, vea [procedimientos de ventana](window-procedures.md).

A continuación se encuentra una aplicación MDI típica. Se denomina MULTIPAD.

![ventana de marco de aplicación de multipad y ventana de cliente](images/csmdi-01.png)

## <a name="child-window-creation"></a>Creación de ventanas secundarias

Para crear una ventana secundaria, una aplicación MDI llama a la función [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) o envía el mensaje de [**WM \_ MDICREATE**](wm-mdicreate.md) a la ventana del cliente MDI. Una manera más eficaz de crear una ventana secundaria MDI es llamar a la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , especificando el estilo extendido **WS \_ ex \_ MDICHILD** .

Para destruir una ventana secundaria, una aplicación MDI envía un mensaje de [**WM \_ MDIDESTROY**](wm-mdidestroy.md) a la ventana del cliente MDI.

## <a name="child-window-activation"></a>Activación de la ventana secundaria

Cualquier número de ventanas secundarias puede aparecer en la ventana del cliente en cualquier momento, pero solo una puede estar activa. La ventana secundaria activa se coloca delante de todas las demás ventanas secundarias y se resalta su borde.

El usuario puede activar una ventana secundaria inactiva haciendo clic en ella. Una aplicación MDI activa una ventana secundaria mediante el envío de un mensaje de [**WM \_ MDIACTIVATE**](wm-mdiactivate.md) a la ventana del cliente MDI. Cuando la ventana de cliente procesa este mensaje, envía un mensaje de **WM \_ MDIACTIVATE** al procedimiento de ventana de la ventana secundaria que se va a activar y al procedimiento de ventana de la ventana secundaria que se va a desactivar.

Para evitar que una ventana secundaria se active, controle el mensaje de [**\_ NCACTIVATE de WM**](wm-ncactivate.md) en la ventana secundaria devolviendo **false**.

El sistema realiza un seguimiento de la posición de cada ventana secundaria en la pila de ventanas superpuestas. Este apilamiento se conoce como el [orden Z](window-features.md). El usuario puede activar la siguiente ventana secundaria en el orden Z; para ello, haga clic en **siguiente** en el menú ventana de la ventana activa. Una aplicación activa la siguiente ventana secundaria (o anterior) en el orden Z mediante el envío de un mensaje de [**WM \_ MDINEXT**](wm-mdinext.md) a la ventana de cliente.

Para recuperar el identificador de la ventana secundaria activa, la aplicación MDI envía un mensaje de [**WM \_ MDIGETACTIVE**](wm-mdigetactive.md) a la ventana de cliente.

## <a name="multiple-document-menus"></a>Menús de varios documentos

La ventana de marco de una aplicación MDI debe incluir una barra de menús con un menú ventana. El menú ventana debe incluir elementos que organicen las ventanas secundarias dentro de la ventana de cliente o que cierren todas las ventanas secundarias. El menú ventana de una aplicación MDI típica podría incluir los elementos de la tabla siguiente.



| Elemento de menú         | Propósito                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Icono**          | Organiza las ventanas secundarias en un formato de mosaico para que cada una de ellas aparezca en su totalidad en la ventana del cliente.                       |
| **Cascade**       | Organiza las ventanas secundarias en un formato en cascada. Las ventanas secundarias se superponen entre sí, pero la barra de título de cada una está visible. |
| **Organizar iconos** | Organiza los iconos de las ventanas secundarias minimizadas en la parte inferior de la ventana de cliente.                                     |
| **Cerrar todo**     | Cierra todas las ventanas secundarias.                                                                                                |



 

Siempre que se crea una ventana secundaria, el sistema anexa automáticamente un nuevo elemento de menú al menú ventana. El texto del elemento de menú es el mismo que el texto de la barra de menús de la nueva ventana secundaria. Al hacer clic en el elemento de menú, el usuario puede activar la ventana secundaria correspondiente. Cuando se destruye una ventana secundaria, el sistema quita automáticamente el elemento de menú correspondiente del menú ventana.

El sistema puede Agregar hasta diez elementos de menú al menú ventana. Cuando se crea la décima ventana secundaria, el sistema agrega el elemento **más Windows** al menú ventana. Al hacer clic en este elemento, se muestra el cuadro de diálogo **seleccionar ventana** . El cuadro de diálogo contiene un cuadro de lista con los títulos de todas las ventanas secundarias MDI disponibles actualmente. El usuario puede activar una ventana secundaria haciendo clic en su título en el cuadro de lista.

Si la aplicación MDI admite varios tipos de ventanas secundarias, personalice la barra de menús para reflejar las operaciones asociadas a la ventana activa. Para ello, proporcione recursos de menú independientes para cada tipo de ventana secundaria que admita la aplicación. Cuando se activa un nuevo tipo de ventana secundaria, la aplicación debe enviar un mensaje de [**WM \_ MDISETMENU**](wm-mdisetmenu.md) a la ventana del cliente, pasándole el identificador al menú correspondiente.

Cuando no existe ninguna ventana secundaria, la barra de menús solo debe contener los elementos usados para crear o abrir un documento.

Cuando el usuario navega por los menús de una aplicación MDI mediante las teclas de cursor, las claves se comportan de manera diferente que cuando el usuario navega por los menús de una aplicación típica. En una aplicación MDI, el control pasa del menú ventana de la aplicación al menú ventana de la ventana secundaria activa y, a continuación, al primer elemento de la barra de menús.

## <a name="multiple-document-accelerators"></a>Varios aceleradores de documentos

Para recibir y procesar las teclas de aceleración de sus ventanas secundarias, una aplicación MDI debe incluir la función [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) en su bucle de mensajes. El bucle debe llamar a **TranslateMDISysAccel** antes de llamar a la función [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) o [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .

Las teclas de aceleración del menú ventana de una ventana secundaria MDI son diferentes de las de una ventana secundaria no MDI. En una ventana secundaria MDI, la combinación de teclas ALT + – (menos) abre el menú ventana, la combinación de teclas CTRL + F4 cierra la ventana secundaria activa y la combinación de teclas CTRL + F6 activa la ventana secundaria siguiente.

## <a name="child-window-size-and-arrangement"></a>Tamaño y organización de la ventana secundaria

Una aplicación MDI controla el tamaño y la posición de sus ventanas secundarias mediante el envío de mensajes a la ventana del cliente MDI. Para maximizar la ventana secundaria activa, la aplicación envía el mensaje de [**WM \_ MDIMAXIMIZE**](wm-mdimaximize.md) a la ventana de cliente. Cuando una ventana secundaria está maximizada, su área cliente rellena completamente la ventana del cliente MDI. Además, el sistema oculta automáticamente la barra de título de la ventana secundaria y agrega el icono del menú ventana de la ventana secundaria y el botón restaurar a la barra de menús de la aplicación MDI. La aplicación puede restaurar la ventana del cliente a su tamaño y posición originales (premaximizados) enviando la ventana del cliente a un mensaje de [**WM \_ MDIRESTORE**](wm-mdirestore.md) .

Una aplicación MDI puede organizar sus ventanas secundarias en formato en cascada o de mosaico. Cuando las ventanas secundarias se encuentran en cascada, las ventanas aparecen en una pila. La ventana de la parte inferior de la pila ocupa la esquina superior izquierda de la pantalla y las ventanas restantes se desplazan vertical y horizontalmente para que el borde izquierdo y la barra de título de cada ventana secundaria estén visibles. Para organizar las ventanas secundarias en el formato en cascada, una aplicación MDI envía el mensaje de [**\_ MDICASCADE de WM**](wm-mdicascade.md) . Normalmente, la aplicación envía este mensaje cuando el usuario hace clic en **cascada** en el menú ventana.

Cuando las ventanas secundarias están en mosaico, el sistema muestra todas las ventanas secundarias en su totalidad, superpuestas a ninguna de las ventanas. Todas las ventanas tienen el mismo tamaño, según sea necesario, para que quepan en la ventana del cliente. Para organizar las ventanas secundarias en el formato de mosaico, una aplicación MDI envía un mensaje de [**WM \_ MDITILE**](wm-mditile.md) a la ventana de cliente. Normalmente, la aplicación envía este mensaje cuando el usuario hace clic en **mosaico** en el menú ventana.

Una aplicación MDI debe proporcionar un icono diferente para cada tipo de ventana secundaria que admita. La aplicación especifica un icono al registrar la clase de ventana secundaria. El sistema muestra automáticamente el icono de una ventana secundaria en la parte inferior de la ventana de cliente cuando se minimiza la ventana secundaria. Una aplicación MDI dirige el sistema para organizar los iconos de la ventana secundaria mediante el envío de un mensaje de [**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md) a la ventana de cliente. Normalmente, la aplicación envía este mensaje cuando el usuario hace clic en **organizar iconos** en el menú ventana.

## <a name="icon-title-windows"></a>Ventanas de título de icono

Dado que las ventanas secundarias MDI se pueden minimizar, una aplicación MDI debe evitar manipular las ventanas de título de icono como si fueran ventanas secundarias MDI normales. Las ventanas de título de icono aparecen cuando la aplicación enumera las ventanas secundarias de la ventana del cliente MDI. No obstante, las ventanas de título de icono se diferencian de otras ventanas secundarias en que son propiedad de una ventana secundaria MDI.

Para determinar si una ventana secundaria es una ventana de título de icono, utilice la función [**GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) con el índice de propietario de GW \_ . Las ventanas que no son de título devuelven **null**. Tenga en cuenta que esta prueba no es suficiente para las ventanas de nivel superior, ya que los menús y los cuadros de diálogo son ventanas de propiedad.

## <a name="child-window-data"></a>Datos de la ventana secundaria

Dado que el número de ventanas secundarias varía en función de cuántos documentos Abra el usuario, una aplicación MDI debe ser capaz de asociar datos (por ejemplo, el nombre del archivo actual) con cada ventana secundaria. Existen dos formas de hacerlo:

-   Almacene los datos de la ventana secundaria en la estructura de la ventana.
-   Usar las propiedades de la ventana.

### <a name="window-structure"></a>Estructura de ventana

Cuando una aplicación MDI registra una clase de ventana, puede reservar espacio adicional en la estructura de la ventana para los datos de aplicación específicos de esta clase de Windows concreta. Para almacenar y recuperar datos en este espacio adicional, la aplicación usa las funciones [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) y [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

Para mantener una gran cantidad de datos para una ventana secundaria, una aplicación puede asignar memoria para una estructura de datos y, a continuación, almacenar el identificador en la memoria que contiene la estructura en el espacio adicional asociado a la ventana secundaria.

### <a name="window-properties"></a>Propiedades de la ventana

Una aplicación MDI también puede almacenar datos por documento mediante las propiedades de la ventana. Los *datos por documento* son datos específicos del tipo de documento contenido en una ventana secundaria determinada. Las propiedades son diferentes de espacio adicional en la estructura de la ventana, ya que no es necesario asignar espacio adicional al registrar la clase de ventana. Una ventana puede tener cualquier número de propiedades. Además, cuando se usan desplazamientos para tener acceso al espacio adicional en las estructuras de ventana, se hace referencia a las propiedades mediante nombres de cadena. Para obtener más información acerca de las propiedades de la ventana, consulte propiedades de la [ventana](window-properties.md).

 

 
