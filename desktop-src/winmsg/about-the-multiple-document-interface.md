---
description: Cada documento de una aplicación de interfaz de múltiples documentos (MDI) se muestra en una ventana secundaria independiente dentro del área cliente de la ventana principal de la aplicación.
ms.assetid: 35dff281-3b11-4954-85cf-a0f1c9ed346a
title: Acerca de la interfaz de varios documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071d3bebad8e6aba48b69b66fd41f9f7933c1d9785ae38512003aaf1bd9a19e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706010"
---
# <a name="about-the-multiple-document-interface"></a>Acerca de la interfaz de varios documentos

Cada documento de una aplicación de interfaz de múltiples documentos (MDI) se muestra en una ventana secundaria independiente dentro del área cliente de la ventana principal de la aplicación. Las aplicaciones MDI típicas incluyen aplicaciones de procesamiento de palabras que permiten al usuario trabajar con varios documentos de texto y aplicaciones de hoja de cálculo que permiten al usuario trabajar con varios gráficos y hojas de cálculo. Para obtener más información, vea los temas siguientes:

-   [Marco, cliente y secundario Windows](#frame-client-and-child-windows)
-   [Creación de ventanas secundarias](#child-window-creation)
-   [Activación de ventana secundaria](#child-window-activation)
-   [Menús de varios documentos](#multiple-document-menus)
-   [Varios aceleradores de documentos](#multiple-document-accelerators)
-   [Organización y tamaño de la ventana secundaria](#child-window-size-and-arrangement)
-   [Icono Título Windows](#icon-title-windows)
-   [Datos de ventana secundaria](#child-window-data)
    -   [Estructura de ventana](#window-structure)
    -   [Propiedades de la ventana](#window-properties)

## <a name="frame-client-and-child-windows"></a>Marco, cliente y secundario Windows

Una aplicación MDI tiene tres tipos de ventanas: una ventana de marco, una ventana de cliente MDI, así como varias ventanas secundarias. La *ventana marco es* como la ventana principal de la aplicación: tiene un borde de tamaño, una barra de título, un menú de ventana, un botón minimizar y un botón maximizar. La aplicación debe registrar una clase de ventana para la ventana de marco y proporcionar un procedimiento de ventana para admitirla.

Una aplicación MDI no muestra la salida en el área cliente de la ventana de marco. En su lugar, muestra la ventana de cliente MDI. Una *ventana de cliente MDI* es un tipo especial de ventana secundaria que pertenece a la clase de ventana registrada previamente **MDICLIENT**. La ventana de cliente es un elemento secundario de la ventana de marco; sirve como fondo para las ventanas secundarias. También proporciona compatibilidad para crear y manipular ventanas secundarias. Por ejemplo, una aplicación MDI puede crear, activar o maximizar ventanas secundarias mediante el envío de mensajes a la ventana cliente de MDI.

Cuando el usuario abre o crea un documento, la ventana de cliente crea una ventana secundaria para el documento. La ventana de cliente es la ventana primaria de todas las ventanas secundarias MDI de la aplicación. Cada ventana secundaria tiene un borde de tamaño, una barra de título, un menú de ventana, un botón minimizar y un botón maximizar. Dado que se recorta una ventana secundaria, se limita a la ventana de cliente y no puede aparecer fuera de ella.

Una aplicación MDI puede admitir más de un tipo de documento. Por ejemplo, una aplicación de hoja de cálculo típica permite al usuario trabajar con gráficos y hojas de cálculo. Para cada tipo de documento que admite, una aplicación MDI debe registrar una clase de ventana secundaria y proporcionar un procedimiento de ventana para admitir las ventanas que pertenecen a esa clase. Para obtener más información sobre las clases de ventana, vea [Clases de ventana](window-classes.md). Para obtener más información sobre los procedimientos de ventana, vea [Procedimientos de ventana](window-procedures.md).

A continuación se muestra una aplicación MDI típica. Se denomina Multipad.

![ventana de marco de aplicación mdi multipad y ventana de cliente](images/csmdi-01.png)

## <a name="child-window-creation"></a>Creación de ventanas secundarias

Para crear una ventana secundaria, una aplicación MDI llama a la función [**CreateMDIWindow**](/windows/win32/api/winuser/nf-winuser-createmdiwindowa) o envía el mensaje [**\_ WM MDICREATE**](wm-mdicreate.md) a la ventana de cliente MDI. Una manera más eficaz de crear una ventana secundaria MDI es llamar a la función [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) especificando el estilo extendido **\_ \_ MDICHILD de WS EX.**

Para destruir una ventana secundaria, una aplicación MDI envía un mensaje [**\_ WM MDIDESTROY**](wm-mdidestroy.md) a la ventana de cliente MDI.

## <a name="child-window-activation"></a>Activación de ventana secundaria

Cualquier número de ventanas secundarias puede aparecer en la ventana de cliente en cualquier momento, pero solo una puede estar activa. La ventana secundaria activa se coloca delante de todas las demás ventanas secundarias y su borde está resaltado.

El usuario puede activar una ventana secundaria inactiva haciendo clic en ella. Una aplicación MDI activa una ventana secundaria mediante el envío de un mensaje [**\_ WM MDIACTIVATE**](wm-mdiactivate.md) a la ventana de cliente MDI. A medida que la ventana de cliente procesa este mensaje, envía un mensaje **\_ WM MDIACTIVATE** al procedimiento de ventana de la ventana secundaria que se va a activar y al procedimiento de ventana de la ventana secundaria que se está desactivando.

Para evitar que se active una ventana secundaria, controle el mensaje [**\_ WM NCACTIVATE**](wm-ncactivate.md) en la ventana secundaria devolviendo **FALSE**.

El sistema realiza un seguimiento de la posición de cada ventana secundaria en la pila de ventanas superpuestas. Este apilamiento se conoce como [orden Z.](window-features.md) El usuario puede activar la siguiente ventana secundaria en el orden Z haciendo clic en **Siguiente** en el menú de la ventana activa. Una aplicación activa la siguiente (o anterior) ventana secundaria en el orden Z mediante el envío de un mensaje [**\_ WM MDINEXT**](wm-mdinext.md) a la ventana de cliente.

Para recuperar el identificador de la ventana secundaria activa, la aplicación MDI envía un mensaje [**\_ WM MDIGETACTIVE**](wm-mdigetactive.md) a la ventana de cliente.

## <a name="multiple-document-menus"></a>Menús de varios documentos

La ventana marco de una aplicación MDI debe incluir una barra de menús con un menú de ventana. El menú de la ventana debe incluir elementos que organice las ventanas secundarias dentro de la ventana de cliente o que cierren todas las ventanas secundarias. El menú de ventana de una aplicación MDI típica podría incluir los elementos de la tabla siguiente.



| Elemento de menú         | Propósito                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------|
| **Icono**          | Organiza las ventanas secundarias en un formato de icono para que cada una aparezca en su totalidad en la ventana de cliente.                       |
| **Cascade**       | Organiza las ventanas secundarias en un formato en cascada. Las ventanas secundarias se superponen entre sí, pero la barra de título de cada una está visible. |
| **Organizar iconos** | Organiza los iconos de las ventanas secundarias minimizadas a lo largo de la parte inferior de la ventana de cliente.                                     |
| **Cerrar todo**     | Cierra todas las ventanas secundarias.                                                                                                |



 

Cada vez que se crea una ventana secundaria, el sistema anexa automáticamente un nuevo elemento de menú al menú de la ventana. El texto del elemento de menú es el mismo que el texto de la barra de menús de la nueva ventana secundaria. Al hacer clic en el elemento de menú, el usuario puede activar la ventana secundaria correspondiente. Cuando se destruye una ventana secundaria, el sistema quita automáticamente el elemento de menú correspondiente del menú de la ventana.

El sistema puede agregar hasta diez elementos de menú al menú de la ventana. Cuando se crea la décima ventana secundaria, el sistema agrega el elemento **Más Windows** al menú de la ventana. Al hacer clic en este elemento se **muestra el cuadro de diálogo** Seleccionar ventana . El cuadro de diálogo contiene un cuadro de lista con los títulos de todas las ventanas secundarias MDI disponibles actualmente. El usuario puede activar una ventana secundaria haciendo clic en su título en el cuadro de lista.

Si la aplicación MDI admite varios tipos de ventanas secundarias, adapte la barra de menús para reflejar las operaciones asociadas a la ventana activa. Para ello, proporcione recursos de menú independientes para cada tipo de ventana secundaria que admita la aplicación. Cuando se activa un nuevo tipo de ventana secundaria, la aplicación debe enviar un mensaje [**\_ WM MDISETMENU**](wm-mdisetmenu.md) a la ventana de cliente y pasarle el identificador al menú correspondiente.

Cuando no existe ninguna ventana secundaria, la barra de menús solo debe contener elementos usados para crear o abrir un documento.

Cuando el usuario navega por los menús de una aplicación MDI mediante teclas de cursor, las claves se comportan de forma diferente a cuando el usuario navega por los menús de una aplicación típica. En una aplicación MDI, el control pasa desde el menú de ventana de la aplicación al menú de ventana de la ventana secundaria activa y, a continuación, al primer elemento de la barra de menús.

## <a name="multiple-document-accelerators"></a>Varios aceleradores de documentos

Para recibir y procesar las teclas de aceleración de sus ventanas secundarias, una aplicación MDI debe incluir la función [**TranslateMDISysAccel**](/windows/win32/api/winuser/nf-winuser-translatemdisysaccel) en su bucle de mensajes. El bucle debe llamar **a TranslateMDISysAccel antes** de llamar a la [**función TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) [**o DispatchMessage.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)

Las teclas de aceleración del menú de ventana de una ventana secundaria MDI son diferentes de las de una ventana secundaria que no es MDI. En una ventana secundaria MDI, la combinación de teclas ALT+ - (menos) abre el menú de la ventana, la combinación de teclas CTRL+F4 cierra la ventana secundaria activa y la combinación de teclas CTRL+F6 activa la siguiente ventana secundaria.

## <a name="child-window-size-and-arrangement"></a>Organización y tamaño de la ventana secundaria

Una aplicación MDI controla el tamaño y la posición de sus ventanas secundarias mediante el envío de mensajes a la ventana cliente de MDI. Para maximizar la ventana secundaria activa, la aplicación envía el mensaje [**\_ WM MDIMAXIMIZE**](wm-mdimaximize.md) a la ventana de cliente. Cuando se maximiza una ventana secundaria, su área de cliente rellena completamente la ventana de cliente MDI. Además, el sistema oculta automáticamente la barra de título de la ventana secundaria y agrega el icono de menú de ventana de la ventana secundaria y el botón Restaurar a la barra de menús de la aplicación MDI. La aplicación puede restaurar la ventana de cliente a su tamaño y posición originales (premaximized) enviando a la ventana de cliente un [**mensaje \_ WM MDIRESTORE.**](wm-mdirestore.md)

Una aplicación MDI puede organizar sus ventanas secundarias en un formato en cascada o de mosaico. Cuando las ventanas secundarias están en cascada, las ventanas aparecen en una pila. La ventana de la parte inferior de la pila ocupa la esquina superior izquierda de la pantalla y las ventanas restantes se desplazan vertical y horizontalmente para que el borde izquierdo y la barra de título de cada ventana secundaria estén visibles. Para organizar las ventanas secundarias en formato en cascada, una aplicación MDI envía el [**mensaje \_ WM MDICASCADE.**](wm-mdicascade.md) Normalmente, la aplicación envía este mensaje cuando el usuario hace clic en **Cascade en** el menú de la ventana.

Cuando las ventanas secundarias están en mosaico, el sistema muestra cada ventana secundaria en su totalidad, superpuesta ninguna de las ventanas. Todas las ventanas tienen un tamaño, según sea necesario, para ajustarse a la ventana de cliente. Para organizar las ventanas secundarias en el formato de icono, una aplicación MDI envía un mensaje [**\_ WM MDITILE**](wm-mditile.md) a la ventana de cliente. Normalmente, la aplicación envía este mensaje cuando el usuario hace clic **en Icono en** el menú de la ventana.

Una aplicación MDI debe proporcionar un icono diferente para cada tipo de ventana secundaria que admita. La aplicación especifica un icono al registrar la clase de ventana secundaria. El sistema muestra automáticamente el icono de una ventana secundaria en la parte inferior de la ventana de cliente cuando se minimiza la ventana secundaria. Una aplicación MDI indica al sistema que organice los iconos de ventana secundarios mediante el envío de un mensaje [**\_ WM MDIICONARRANGE**](wm-mdiiconarrange.md) a la ventana de cliente. Normalmente, la aplicación envía este mensaje cuando el usuario hace clic en **Organizar iconos** en el menú de la ventana.

## <a name="icon-title-windows"></a>Icono Título Windows

Dado que las ventanas secundarias MDI se pueden minimizar, una aplicación MDI debe evitar manipular las ventanas de título de icono como si fueran ventanas secundarias MDI normales. Las ventanas de título de icono aparecen cuando la aplicación enumera las ventanas secundarias de la ventana de cliente MDI. Sin embargo, las ventanas de título de icono difieren de otras ventanas secundarias, ya que son propiedad de una ventana secundaria MDI.

Para determinar si una ventana secundaria es una ventana de título de icono, use la [**función GetWindow**](/windows/win32/api/winuser/nf-winuser-getwindow) con el índice GW \_ OWNER. Las ventanas que no son de **título devuelven NULL.** Tenga en cuenta que esta prueba no es suficiente para las ventanas de nivel superior, ya que los menús y los cuadros de diálogo son ventanas de propiedad.

## <a name="child-window-data"></a>Datos de ventana secundaria

Dado que el número de ventanas secundarias varía en función de cuántos documentos abra el usuario, una aplicación MDI debe poder asociar datos (por ejemplo, el nombre del archivo actual) a cada ventana secundaria. Existen dos modos para hacer esto:

-   Almacene los datos de la ventana secundaria en la estructura de la ventana.
-   Usar propiedades de ventana.

### <a name="window-structure"></a>Estructura de ventana

Cuando una aplicación MDI registra una clase de ventana, puede reservar espacio adicional en la estructura de ventana para los datos de aplicación específicos de esta clase determinada de ventanas. Para almacenar y recuperar datos en este espacio adicional, la aplicación usa las [**funciones GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) [**y SetWindowLong.**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)

Para mantener una gran cantidad de datos para una ventana secundaria, una aplicación puede asignar memoria para una estructura de datos y, a continuación, almacenar el identificador en la memoria que contiene la estructura en el espacio adicional asociado a la ventana secundaria.

### <a name="window-properties"></a>Propiedades de la ventana

Una aplicación MDI también puede almacenar datos por documento mediante propiedades de ventana. *Los datos por documento* son datos específicos del tipo de documento contenido en una ventana secundaria determinada. Las propiedades son diferentes del espacio adicional en la estructura de la ventana, ya que no es necesario asignar espacio adicional al registrar la clase de ventana. Una ventana puede tener cualquier número de propiedades. Además, cuando se usan desplazamientos para acceder al espacio adicional en las estructuras de ventana, los nombres de cadenas conocen las propiedades. Para obtener más información sobre las propiedades de la ventana, vea [Propiedades de ventana](window-properties.md).

 

 
