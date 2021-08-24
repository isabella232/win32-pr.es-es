---
title: Acerca de los menús
description: En este tema se de abordan los menús.
ms.assetid: fd0b26f1-93cd-421b-9097-8502ab7681e9
keywords:
- resources,menus
- menús, acerca de
- submenús
- barras de menús
- menús de nivel superior
- menús emergentes
- menús desplegables
- menús, nivel superior
- menús, elementos emergentes
- menús, lista desplegable
- nombres de menú
- menús, acceso directo
- menus,Window
- menus,System
- menus,Control
- menús contextuales
- Menú Ventana
- Menú Del sistema
- Menú Control
- identificadores de ayuda
- identificadores de menú
- menú, elementos
- elementos de comando
- identificadores de elemento de menú
- posición del elemento de menú
- seleccionar elementos de menú
- borrar elementos de menú
- menús dibujados por el propietario
- menús, propietario dibujado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34d35ddf55ad31ed27cc12c6adffa5517e0081db6d70b4d01d3b88780a8797bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034502"
---
# <a name="about-menus"></a>Acerca de los menús

Un *menú* es una lista de elementos que especifican opciones o grupos de opciones (un submenú) para una aplicación. Al hacer clic en un elemento de menú, se abre un submenú o se hace que la aplicación lleve a cabo un comando. En esta sección se proporciona información sobre los temas siguientes:

-   [Menús y barras de menús](#menu-bars-and-menus)
    -   [Menús contextuales](#shortcut-menus)
    -   [Menú Ventana](#the-window-menu)
    -   [Identificador de ayuda](#help-identifier)
-   [Acceso mediante teclado a los menús](#keyboard-access-to-menus)
    -   [Interfaz de teclado estándar](#standard-keyboard-interface)
    -   [Teclas de acceso de menú](#menu-access-keys)
    -   [Teclas de método abreviado de menú](#menu-shortcut-keys)
-   [Creación de menús](#menu-creation)
    -   [Recursos de plantilla de menú](#menu-template-resources)
    -   [Plantilla de menú en memoria](#menu-template-in-memory)
    -   [Identificadores de menú](#menu-handles)
    -   [Funciones de creación de menús](#menu-creation-functions)
    -   [Presentación del menú](#menu-display)
    -   [Menús de clase de ventana](#window-class-menus)
-   [Elementos de menú](#menu-items)
    -   [Elementos y elementos de comandos que abren submenús](#command-items-and-items-that-open-submenus)
    -   [Identificador de elemento de menú](#menu-item-identifier)
    -   [Posición del elemento de menú](#menu-item-position)
    -   [Acceso a elementos de menú mediante programación](#accessing-menu-items-programmatically)
    -   [Elementos de menú predeterminados](#default-menu-items)
    -   [Elementos de menú seleccionados y despejados](#selected-and-clear-menu-items)
    -   [Elementos de menú Habilitado, Atenuado y Deshabilitado](#enabled-grayed-and-disabled-menu-items)
    -   [Elementos de menú resaltados](#highlighted-menu-items)
    -   [Elementos de menú dibujados por el propietario](#owner-drawn-menu-items)
    -   [Separadores de elementos de menú y saltos de línea](#menu-item-separators-and-line-breaks)
-   [Mensajes usados con menús](#messages-used-with-menus)
-   [Destrucción de menús](#menu-destruction)

## <a name="menu-bars-and-menus"></a>Menús y barras de menús

Un menú se organiza en una jerarquía. En el nivel superior de la jerarquía se encuentra la barra *de menús*; que contiene una lista de *menús*, que a su vez pueden contener *submenús*. A veces, una barra de menús se denomina menú de nivel superior y los menús y submenús también se conocen como *menús emergentes.*

Un elemento de menú puede llevar a cabo un comando o abrir un submenú. Un elemento que lleva a cabo un comando se denomina elemento *de comando* o *comando*.

Un elemento de la barra de menús casi siempre abre un menú. Las barras de menús rara vez contienen elementos de comando. Un menú abierto desde la barra de menús baja de la barra de menús y, a veces, se denomina *menú desplegable*. Cuando se muestra un menú desplegable, se adjunta a la barra de menús. Un elemento de menú de la barra de menús que abre un menú desplegable también se denomina nombre *de menú*.

Los nombres de menú de una barra de menús representan las categorías principales de comandos que proporciona una aplicación. Al seleccionar un nombre de menú en la barra de menús, normalmente se abre un menú cuyos elementos de menú corresponden a los comandos de una categoría. Por ejemplo, una barra  de menús podría contener un nombre de menú Archivo que, cuando el usuario hace clic en él, activa un menú con elementos de menú como **Nuevo,** **Abrir** y **Guardar.** Para obtener información sobre una barra de menús, llame a [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo).

Solo una ventana superpuesta o emergente puede contener una barra de menús; una ventana secundaria no puede contener una. Si la ventana tiene una barra de título, el sistema coloca la barra de menús justo debajo de ella. Una barra de menús siempre está visible. Sin embargo, un submenú no está visible hasta que el usuario selecciona un elemento de menú que lo activa. Para obtener más información sobre las ventanas superpuestas y emergentes, vea [Tipos de ventana](/windows/desktop/winmsg/window-features).

Cada menú debe tener una ventana de propietario. El sistema envía mensajes a la ventana de propietario de un menú cuando el usuario selecciona el menú o elige un elemento del menú.

En esta sección se tratan los temas siguientes.

-   [Menús contextuales](#shortcut-menus)
-   [Menú Ventana](#the-window-menu)
-   [Identificador de ayuda](#help-identifier)

### <a name="shortcut-menus"></a>Menús contextuales

El sistema también proporciona *menús contextuales.* Un menú contextual no está asociado a la barra de menús; puede aparecer en cualquier parte de la pantalla. Normalmente, una aplicación asocia un menú contextual con una parte de una ventana, como el área de cliente, o con un objeto específico, como un icono. Por esta razón, estos menús también se *denominan menús contextuales.*

Un menú contextual permanece oculto hasta que el usuario lo activa, normalmente haciendo clic con el botón derecho en una selección, una barra de herramientas o un botón de la barra de tareas. Normalmente, el menú se muestra en la posición del cursor del cursor del mouse o del cursor de cursor.

### <a name="the-window-menu"></a>Menú Ventana

El **menú** Ventana (también  conocido como menú Sistema o **Control)** es un menú emergente definido y administrado casi exclusivamente por el sistema operativo. El usuario puede abrir el menú de la ventana haciendo clic en el icono de la aplicación en la barra de título o haciendo clic con el botón derecho en cualquier lugar de la barra de título.

El **menú** Ventana proporciona un conjunto estándar de elementos de menú que el usuario puede elegir para cambiar el tamaño o la posición de una ventana, o cerrar la aplicación. Los elementos del menú de la ventana se pueden agregar, eliminar y modificar, pero la mayoría de las aplicaciones solo usan el conjunto estándar de elementos de menú. Una ventana superpuesta, emergente o secundaria puede tener un menú de ventana. No es habitual que una ventana superpuesta o emergente no incluya un menú de ventana.

Cuando el usuario elige un comando en el menú **Ventana,** el sistema envía un mensaje [**WM \_ SYSCOMMAND**](wm-syscommand.md) a la ventana de propietario del menú. En la mayoría de las aplicaciones, el procedimiento de ventana no procesa mensajes desde el menú de la ventana. En su lugar, simplemente pasa los mensajes a la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para el procesamiento predeterminado del sistema del mensaje. Si una aplicación agrega un comando al menú de ventana, el procedimiento de ventana debe procesar el comando.

Una aplicación puede usar la [**función GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) para crear una copia del menú de ventana predeterminado que se modificará. Cualquier ventana que no use la **función GetSystemMenu** para realizar su propia copia del menú de ventana recibe el menú de ventana estándar.

### <a name="help-identifier"></a>Identificador de ayuda

Asociado a cada barra de menús, menú, submenú y menú contextual es un identificador de ayuda. Si el usuario presiona la tecla F1 mientras el menú está activo, este valor se envía a la ventana de propietario como parte de un [**mensaje DE AYUDA \_ de WM.**](../shell/wm-help.md)

## <a name="keyboard-access-to-menus"></a>Acceso mediante teclado a los menús

El sistema proporciona una interfaz de teclado estándar para los menús. Puede mejorar esta interfaz proporcionando teclas de acceso mnemotécnicas y teclas de método abreviado (acelerador) para los elementos de menú.

En los temas siguientes se describen la interfaz de teclado estándar, las teclas de acceso y las teclas de método abreviado:

-   [Interfaz de teclado estándar](#standard-keyboard-interface)
-   [Teclas de acceso del menú](#menu-access-keys)
-   [Teclas de método abreviado de menú](#menu-shortcut-keys)

### <a name="standard-keyboard-interface"></a>Interfaz de teclado estándar

El sistema está diseñado para funcionar con o sin un mouse u otro dispositivo que apunta. Dado que el sistema proporciona una interfaz de teclado estándar, el usuario puede usar el teclado para seleccionar elementos de menú. Esta interfaz de teclado no necesita código especial. Una aplicación recibe un mensaje de comando si el usuario selecciona un elemento de menú a través del teclado o mediante un mouse. La interfaz de teclado estándar procesa las siguientes pulsaciones de tecla.



| Pulsación de tecla              | Acción                                                                                                                                                                                                                                   |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Carácter alfabético | Selecciona el primer elemento de menú con el carácter especificado como clave de acceso. Si el elemento seleccionado invoca un menú, se muestra el menú y se resalta el primer elemento. De lo contrario, se elige el elemento de menú.                            |
| ALT                    | Activa y desactiva el modo de barra de menús.                                                                                                                                                                                                     |
| ALT+Barra espaciadora           | Muestra el menú de la ventana.                                                                                                                                                                                                                |
| ENTRAR                  | Activa un menú y selecciona el primer elemento de menú si un elemento tiene un menú asociado a él. De lo contrario, esta pulsación de tecla elige el elemento como si el usuario hubiera liberado el botón del mouse mientras se seleccionaba el elemento.                              |
| ESC                    | Sale del modo de menú.                                                                                                                                                                                                                         |
| FLECHA IZQUIERDA             | Se desvía al elemento de menú de nivel superior anterior. Los elementos de menú de nivel superior incluyen nombres de menú y el menú de ventana. Si el elemento seleccionado está en un menú, se selecciona la columna anterior del menú o se selecciona el elemento de menú de nivel superior anterior. |
| FLECHA DERECHA            | Funciona como la tecla DE FLECHA IZQUIERDA, excepto en la dirección opuesta. En los menús, esta pulsación de tecla mueve hacia delante una columna; cuando el elemento seleccionado actualmente está en la columna del extremo derecho, se selecciona el menú siguiente.                              |
| FLECHAS ARRIBA o ABAJO      | Activa un menú cuando se presiona en un nombre de menú. Cuando se presiona en un menú, la pulsación de tecla FLECHA ARRIBA selecciona el elemento anterior; La pulsación de tecla FLECHA ABAJO selecciona el siguiente elemento.                                                                  |



 

### <a name="menu-access-keys"></a>Teclas de acceso del menú

La interfaz de teclado estándar para los menús se puede mejorar agregando teclas de acceso (mnemotécnicas) a los elementos de menú. Una clave de acceso es una letra subrayada en el texto de un elemento de menú. Cuando un menú está activo, el usuario puede seleccionar un elemento de menú presionando la tecla que corresponde a la letra subrayada del elemento. El usuario activa la barra de menús presionando la tecla ALT para resaltar el primer elemento de la barra de menús. Un menú está activo cuando se muestra.

Para crear una clave de acceso para un elemento de menú, preceda cualquier carácter de la cadena de texto del elemento con una y comercial. Por ejemplo, la cadena de texto "&Move" hace que el sistema subrayado la letra "M".

### <a name="menu-shortcut-keys"></a>Teclas de método abreviado de menú

Además de tener una clave de acceso, un elemento de menú puede tener una tecla de método abreviado asociada. Una tecla de método abreviado es diferente de una clave de acceso, porque el menú no tiene que estar activo para que la tecla de método abreviado funcione. Además, una tecla de acceso *siempre* está asociada a un elemento de menú, mientras que una tecla de método abreviado suele estar *asociada* (pero no tiene que estar) con un elemento de menú.

El texto que identifica la tecla de método abreviado se agrega a la cadena de texto del elemento de menú. El texto del método abreviado aparece a la derecha del nombre del elemento de menú, después de una barra diagonal inversa y un carácter de tabulación \\ (t). Por ejemplo, "&Cerrar tAlt+F4" representa un comando Cerrar con la combinación de teclas ALT+F4 como tecla de método abreviado y con la letra "C" como clave de \\ acceso. Para obtener más información, vea [Aceleradores de teclado](keyboard-accelerators.md).

## <a name="menu-creation"></a>Creación de menús

Puede crear un menú mediante una plantilla de menú o funciones de creación de menús. Las plantillas de menú se definen normalmente como recursos. Los recursos de plantilla de menú se pueden cargar explícitamente o asignarse como menú predeterminado para una clase de ventana. También puede crear recursos de plantilla de menú dinámicamente en memoria.

En los temas siguientes se describe con detalle la creación de menús:

-   [Recursos de plantilla de menú](#menu-template-resources)
-   [Plantilla de menú en memoria](#menu-template-in-memory)
-   [Identificadores de menú](#menu-handles)
-   [Funciones de creación de menús](#menu-creation-functions)
-   [Presentación del menú](#menu-display)
-   [Menús de clase de ventana](#window-class-menus)

### <a name="menu-template-resources"></a>Recursos de plantilla de menú

La mayoría de las aplicaciones crean menús mediante recursos de plantilla de menú. Una *plantilla de menú* define un menú, incluidos los elementos de la barra de menús y todos los menús. Para obtener información sobre cómo crear un recurso de plantilla de menú, consulte la documentación incluida con las herramientas de desarrollo.

Después de crear un recurso de plantilla de menú y agregarlo al archivo ejecutable (.exe) de la aplicación, puede usar la función [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) para cargar el recurso en la memoria. Esta función devuelve un identificador al menú, que puede asignar a una ventana mediante la [**función SetMenu.**](/windows/desktop/api/Winuser/nf-winuser-setmenu) Puede asignar un menú a cualquier ventana que no sea una ventana secundaria.

La implementación de menús como recursos facilita la localización de una aplicación para su uso en varios países o regiones. Solo el archivo de definición de recursos debe localizarse para cada idioma, no para el código fuente de la aplicación.

### <a name="menu-template-in-memory"></a>Plantilla de menú en memoria

Se puede crear un menú a partir de una plantilla de menú integrada en memoria en tiempo de ejecución. Por ejemplo, una aplicación que permite a un usuario personalizar su menú podría crear una plantilla de menú en memoria en función de las preferencias del usuario. A continuación, la aplicación podría guardar la plantilla en un archivo o en el Registro para su uso futuro. Para crear un menú a partir de una plantilla en memoria, use la [**función LoadMenuIndirect.**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) Para obtener descripciones de los formatos de plantilla de menú, vea [Recursos de plantilla de menú.](#menu-template-resources)

Una plantilla de menú estándar consta de una [**estructura MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) seguida de una o varias [**estructuras MENUITEMTEMPLATE.**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)

Una plantilla de menú extendida consta de una [**estructura MENUEX \_ TEMPLATE \_ HEADER**](menuex-template-header.md) seguida de una o varias estructuras [**MENUEX TEMPLATE \_ \_ ITEM.**](menuex-template-item.md)

### <a name="menu-handles"></a>Identificadores de menú

El sistema genera un identificador único para cada menú. Un *identificador de* menú es un valor del tipo **HMENU.** Una aplicación debe especificar un identificador de menú en muchas de las funciones de menú. Recibirá un identificador en una barra de menús al crear el menú o cargar un recurso de menú.

Para recuperar un identificador en la barra de menús de un menú que se ha creado o cargado, use la [**función GetMenu.**](/windows/desktop/api/Winuser/nf-winuser-getmenu) Para recuperar un identificador del submenú asociado a un elemento de menú, use la [**función GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) o [**GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) Para recuperar un identificador en un menú de ventana, use la [**función GetSystemMenu.**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)

### <a name="menu-creation-functions"></a>Funciones de creación de menús

Con las funciones de creación de menús, puede crear menús en tiempo de ejecución o agregar elementos de menú a los menús existentes. Puede usar la función [**CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu) para crear una barra de menús vacía y la [**función CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) para crear un menú vacío. Puede guardar cierta información de configuración para un menú mediante la [**estructura MENUINFO.**](/windows/win32/api/winuser/ns-winuser-menuinfo) Para obtener o recuperar la configuración de un menú, use [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo) o [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo). Para agregar elementos a un menú, use la [**función InsertMenuItem.**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) Todavía se [**admiten las**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) funciones AppendMenu e [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) anteriores, pero **InsertMenuItem** debe usarse para las nuevas aplicaciones.

### <a name="menu-display"></a>Presentación del menú

Una vez cargado o creado un menú, debe asignarse a una ventana para que el sistema pueda mostrarlo. Puede asignar un menú definiendo un menú de clase. Para obtener más información, vea [Menús de clase de ventana](#window-class-menus). También puede asignar un menú a una ventana especificando un identificador para el menú como el parámetro *hMenu* de la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o llamando a la [**función SetMenu.**](/windows/desktop/api/Winuser/nf-winuser-setmenu)

Para mostrar un menú contextual, use [**la función TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) Los menús contextuales, también denominados menús emergentes flotantes o menús contextuales, se muestran normalmente cuando se procesa el mensaje [**\_ CONTEXTMENU**](wm-contextmenu.md) de WM.

Puede asignar un menú a cualquier ventana que no sea una ventana secundaria.

Todavía se [**admite la función TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) anterior, pero las nuevas aplicaciones deben usar la [**función TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)

### <a name="window-class-menus"></a>Menús de clase de ventana

Puede especificar un menú predeterminado, denominado menú *de clase,* al registrar una clase de ventana. Para ello, asigne el nombre del recurso de plantilla de menú al miembro **lpszMenuName** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) utilizada para registrar la clase.

De forma predeterminada, a cada ventana se le asigna el menú de clase para su clase de ventana, por lo que no es necesario cargar explícitamente el menú y asignarlo a cada ventana. Puede invalidar el menú de clase especificando un identificador de menú diferente en una llamada a la [**función CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) También puede cambiar el menú de una ventana después de crearla mediante la [**función SetMenu.**](/windows/desktop/api/Winuser/nf-winuser-setmenu) Para obtener más información, vea [Clases de ventana](/windows/desktop/winmsg/window-classes).

## <a name="menu-items"></a>Elementos de menú

En los temas siguientes se describe lo que hace el sistema cuando el usuario elige un elemento de menú y las formas en que una aplicación puede controlar la apariencia y la funcionalidad de un elemento:

-   [Elementos y elementos de comandos que abren submenús](#command-items-and-items-that-open-submenus)
-   [Identificador de elemento de menú](#menu-item-identifier)
-   [Posición del elemento de menú](#menu-item-position)
-   [Acceso a elementos de menú mediante programación](#accessing-menu-items-programmatically)
-   [Elementos de menú predeterminados](#default-menu-items)
-   [Elementos de menú seleccionados y despejados](#selected-and-clear-menu-items)
-   [Elementos de menú Habilitado, Atenuado y Deshabilitado](#enabled-grayed-and-disabled-menu-items)
-   [Elementos de menú resaltados](#highlighted-menu-items)
-   [Elementos de menú dibujados por el propietario](#owner-drawn-menu-items)
-   [Separadores de elementos de menú y saltos de línea](#menu-item-separators-and-line-breaks)

### <a name="command-items-and-items-that-open-submenus"></a>Elementos y elementos de comandos que abren submenús

Cuando el usuario elige un elemento de comando, el sistema envía un mensaje de comando a la ventana propietaria del menú. Si el elemento de comando está en el menú de la ventana, el sistema envía el [**mensaje \_ SYSCOMMAND de WM.**](wm-syscommand.md) De lo contrario, envía el [**mensaje \_ WM COMMAND.**](wm-command.md)

Asociado a cada elemento de menú que abre un submenú es un identificador del submenú correspondiente. Cuando el usuario apunta a este tipo de elemento, el sistema abre el submenú. No se envía ningún mensaje de comando a la ventana de propietario. Sin embargo, el sistema envía un [**mensaje \_ WM INITMENUPOPUP**](wm-initmenupopup.md) a la ventana de propietario antes de mostrar el submenú. Puede obtener un identificador del submenú asociado a un elemento mediante la [**función GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) o [**GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

Normalmente, una barra de menús contiene nombres de menú, pero también puede contener elementos de comando. Un submenú normalmente contiene elementos de comando, pero también puede contener elementos que abren submenús anidados. Al agregar estos elementos a los submenús, puede anidar menús a cualquier profundidad. Para proporcionar una indicación visual para el usuario, el sistema muestra automáticamente una flecha pequeña a la derecha del texto de un elemento de menú que abre un submenú.

### <a name="menu-item-identifier"></a>Menu-Item identificador

Asociado a cada elemento de menú es un entero único definido por la aplicación, denominado identificador *de elemento de menú.* Cuando el usuario elige un elemento de comando de un menú, el sistema envía el identificador del elemento a la ventana de propietario como parte de un [**mensaje \_ WM COMMAND.**](wm-command.md) El procedimiento de ventana examina el identificador para determinar el origen del mensaje y procesa el mensaje en consecuencia. Además, puede especificar un elemento de menú mediante su identificador al llamar a funciones de menú; por ejemplo, para habilitar o deshabilitar un elemento de menú.

Los elementos de menú que abren submenús tienen identificadores igual que los elementos de comando. Sin embargo, el sistema no envía un mensaje de comando cuando se selecciona un elemento de este tipo en un menú. En su lugar, el sistema abre el submenú asociado al elemento de menú.

Para recuperar el identificador del elemento de menú en una posición especificada, use la [**función GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid) o [**GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

### <a name="menu-item-position"></a>Menu-Item posición

Además de tener un identificador único, cada elemento de menú de una barra de menús o un menú tiene un valor de posición único. El elemento situado más a la izquierda en una barra de menús o el elemento superior de un menú tiene la posición cero. El valor de posición se incrementa para los elementos de menú posteriores. El sistema asigna un valor de posición a todos los elementos de un menú, incluidos los separadores. En la ilustración siguiente se muestran los valores de posición de los elementos en una barra de menús y en un menú.

![barra de menús y menú](images/csemn-01.png)

Al llamar a una función de menú que modifica o recupera información sobre un elemento de menú específico, puede especificar el elemento mediante su identificador o su posición. Para obtener más información, vea la siguiente sección.

### <a name="accessing-menu-items-programmatically"></a>Acceso a elementos de menú mediante programación

La mayoría de las funciones de menú permiten especificar un elemento de menú por posición o por comando. Algunas funciones usan las **marcas MF \_ BYPOSITION** y **MF \_ BYCOMMAND** para indicar el algoritmo de búsqueda; otras tienen un *parámetro fByPosition* explícito. Si especifica el elemento de menú por posición, el número de elemento es un índice de base cero en el menú. Si especifica el elemento de menú por comando, se busca en el menú y sus submenús un elemento cuyo identificador de menú sea igual al número de elemento proporcionado. Si más de un elemento de la jerarquía de menús coincide con el número de elemento, no se especifica cuál se usa. Si los menús contienen identificadores de menú duplicados, debe usar operaciones de menú basadas en la posición para evitar esta ambigüedad.

### <a name="default-menu-items"></a>Elementos de menú predeterminados

Un submenú puede contener un elemento de menú predeterminado. Cuando el usuario abre un submenú haciendo doble clic, el sistema envía un mensaje de comando a la ventana de propietario del menú y cierra el menú como si se hubiera elegido el elemento de comando predeterminado. Si no hay ningún elemento de comando predeterminado, el submenú permanece abierto. Para recuperar y establecer el elemento predeterminado para un submenú, use las funciones [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem) y [**SetMenuDefaultItem.**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)

### <a name="selected-and-clear-menu-items"></a>Elementos de menú seleccionados y despejados

Un elemento de menú se puede seleccionar o borrar. El sistema muestra un mapa de bits junto a los elementos de menú seleccionados para indicar su estado seleccionado. El sistema no muestra un mapa de bits junto a los elementos sin borrar, a menos que se especifique un mapa de bits "clear" definido por la aplicación. Solo se pueden seleccionar los elementos de menú de un menú; No se pueden seleccionar los elementos de una barra de menús.

Las aplicaciones suelen comprobar o borrar un elemento de menú para indicar si una opción está en vigor. Por ejemplo, suponga que una aplicación tiene una barra de herramientas que el usuario puede mostrar u ocultar mediante un comando barra **de** herramientas en un menú. Cuando la barra de herramientas está oculta, el elemento de menú **Barra** de herramientas está claro. Cuando el usuario elige el comando, la aplicación comprueba el elemento de menú y muestra la barra de herramientas.

Un atributo de marca de verificación controla si un elemento de menú está seleccionado. Puede establecer el atributo de marca de verificación de un elemento de menú mediante la [**función CheckMenuItem.**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) Puede usar la función [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) para determinar si un elemento de menú está seleccionado o borrado actualmente.

En lugar [**de CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) y [**GetMenuState,**](/windows/desktop/api/Winuser/nf-winuser-getmenustate)puede usar las funciones [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) y [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) para recuperar y establecer el estado de comprobación de un elemento de menú.

A veces, un grupo de elementos de menú corresponde a un conjunto de opciones mutuamente excluyentes. En este caso, puede indicar la opción seleccionada mediante un elemento de menú de radio seleccionado (análogo a un control de botón de radio). Los elementos de radio seleccionados se muestran con un mapa de bits de viñeta en lugar de un mapa de bits de marca de verificación. Para comprobar un elemento de menú y convertirlo en un elemento de radio, use la [**función CheckMenuRadioItem.**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)

De forma predeterminada, el sistema muestra una marca de verificación o un mapa de bits de viñeta junto a los elementos de menú seleccionados y ningún mapa de bits junto a los elementos de menú borrados. Sin embargo, puede usar la función [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) para asociar mapas de bits seleccionados y borrados definidos por la aplicación con un elemento de menú. A continuación, el sistema usa los mapas de bits especificados para indicar el estado seleccionado o borrado del elemento de menú.

Los mapas de bits definidos por la aplicación asociados a un elemento de menú deben tener el mismo tamaño que el mapa de bits de marca de verificación predeterminado, cuyas dimensiones pueden variar en función de la resolución de pantalla. Para recuperar las dimensiones correctas, use la [**función GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Puede crear varios recursos de mapa de bits para diferentes resoluciones de pantalla. crear un recurso de mapa de bits y escalarlo, si es necesario; o cree un mapa de bits en tiempo de ejecución y dibuje una imagen en él. Los mapas de bits pueden ser monocromáticos o de color. Sin embargo, dado que los elementos de menú se invierten cuando se resaltan, la apariencia de ciertos mapas de bits de color invertidos puede no ser deseable. Para obtener más información, vea [Mapas de bits.](/windows/desktop/gdi/bitmaps)

### <a name="enabled-grayed-and-disabled-menu-items"></a>Elementos de menú Habilitado, Atenuado y Deshabilitado

Un elemento de menú se puede habilitar, atenuar o deshabilitar. De forma predeterminada, un elemento de menú está habilitado. Cuando el usuario elige un elemento de menú habilitado, el sistema envía un mensaje de comando a la ventana del propietario o muestra el submenú correspondiente, en función del tipo de elemento de menú que sea.

Cuando los elementos de menú no están disponibles para el usuario, deben estar atenuados o deshabilitados. No se pueden elegir los elementos de menú atenuados y deshabilitados. Un elemento deshabilitado tiene el mismo aspecto que un elemento habilitado. Cuando el usuario hace clic en un elemento deshabilitado, el elemento no está seleccionado y no ocurre nada. Los elementos deshabilitados pueden ser útiles en, por ejemplo, un tutorial que presenta un menú que parece activo pero no lo está.

Una aplicación atenua un elemento de menú no disponible para proporcionar una indicación visual al usuario de que un comando no está disponible. Puede usar un elemento atenuado cuando una acción no sea  adecuada (por  ejemplo, puede atenuar el comando Imprimir en el menú Archivo cuando el sistema no tenga instalada una impresora).

La [**función EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem) habilita, atenua o deshabilita un elemento de menú. Para determinar si un elemento de menú está habilitado, atenuado o deshabilitado, use la [**función GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

En lugar [**de GetMenuItemInfo,**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)también puede usar la función [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) para determinar si un elemento de menú está habilitado, atenuado o deshabilitado.

### <a name="highlighted-menu-items"></a>Elementos de menú resaltados

El sistema resalta automáticamente los elementos de menú en los menús a medida que el usuario los selecciona. Sin embargo, el resaltado se puede agregar o quitar explícitamente de un nombre de menú en la barra de menús mediante [**la función HiliteMenuItem.**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem) Esta función no tiene ningún efecto en los elementos de menú de los menús. Sin **embargo, cuando hiliteMenuItem** se usa para resaltar un nombre de menú, el nombre solo parece estar seleccionado. Si el usuario presiona la tecla ENTRAR, no se elige el elemento resaltado. Esta característica puede ser útil en, por ejemplo, una aplicación de entrenamiento que muestra el uso de menús.

### <a name="owner-drawn-menu-items"></a>Owner-Drawn de menú

Una aplicación puede controlar completamente la apariencia de un elemento de menú mediante un *elemento dibujado por el propietario*. Los elementos dibujados por el propietario requieren que una aplicación asóquese la responsabilidad total de dibujar los estados seleccionados (resaltados), seleccionados y borrados. Por ejemplo, si una aplicación proporciona un menú de fuentes, podría dibujar cada elemento de menú mediante la fuente correspondiente; El elemento de Román se dibujaría con román, el elemento de Cursiva se dibujaría en cursiva, y así sucesivamente. Para obtener más información, vea [Creating Owner-Drawn Menu Items](using-menus.md).

### <a name="menu-item-separators-and-line-breaks"></a>Separadores de elementos de menú y saltos de línea

El sistema proporciona un tipo especial de elemento de menú, denominado *separador*, que aparece como una línea horizontal. Puede usar un separador para dividir un menú en grupos de elementos relacionados. No se puede usar un separador en una barra de menús y el usuario no puede seleccionar un separador.

Cuando una barra de menús contiene más nombres de menú de los que caben en una línea, el sistema ajusta la barra de menús al dividirla automáticamente en dos o más líneas. Puede hacer que se produzca un salto de línea en un elemento específico de una barra de menús mediante la asignación de la marca de tipo **\_ MENUBREAK** de MFT al elemento. El sistema coloca ese elemento y todos los elementos posteriores en una nueva línea.

Cuando un menú contiene más elementos de los que caben en una columna, el menú se truncará. Puede hacer que se produzca un salto de columna en un elemento específico de un menú mediante la asignación de la marca de tipo **\_ MENUBREAK** de MFT al elemento o mediante la opción MENUBREAK de la [instrucción MENUITEM.](/windows/desktop/menurc/menuitem-statement) El sistema coloca ese elemento y todos los elementos posteriores en una nueva columna. La **marca de tipo \_ MENUBARBREAK** de MFT tiene el mismo efecto, salvo que aparece una línea vertical entre la nueva columna y la antigua.

Si usa las funciones [**AppendMenu,**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) para asignar saltos de línea, debe asignar las marcas de tipo **MF \_ MENUBREAK** o **MF \_ MENUBARBREAK.**

## <a name="messages-used-with-menus"></a>Mensajes usados con menús

El sistema notifica la actividad relacionada con el menú mediante el envío de mensajes al procedimiento de ventana de la ventana propietaria del menú. El sistema envía una serie de mensajes cuando el usuario selecciona elementos en la barra de menús o hace clic en el botón derecho del mouse para mostrar un menú contextual.

Cuando el usuario activa un elemento en la barra de menús, la ventana de propietario recibe primero un [**mensaje \_ SYSCOMMAND de WM.**](wm-syscommand.md) Este mensaje incluye una marca que indica si el usuario activó el menú mediante el teclado (SC KEYMENU) o el \_ mouse (SC \_ MOUSEMENU). Para obtener más información, vea [Acceso mediante teclado a los menús](#keyboard-access-to-menus).

A continuación, antes de mostrar los menús, el sistema envía el mensaje [**\_ WM INITMENU**](wm-initmenu.md) al procedimiento de ventana para que una aplicación pueda modificar los menús antes de que el usuario los vea. El sistema envía el mensaje **WM \_ INITMENU** solo una vez por activación del menú.

Cuando el usuario apunta a un elemento de menú que abre un submenú, el sistema envía a la ventana de propietario el mensaje [**\_ WM INITMENUPOPUP**](wm-initmenupopup.md) antes de mostrar el submenú. Este mensaje ofrece a la aplicación la oportunidad de modificar el submenú antes de que se muestre.

Cada vez que el usuario mueve el resaltado de un elemento a otro, el sistema envía un mensaje [**\_ WM MENUSELECT**](wm-menuselect.md) al procedimiento de ventana de la ventana propietaria del menú. Este mensaje identifica el elemento de menú seleccionado actualmente. Muchas aplicaciones proporcionan un área de información en la parte inferior de sus ventanas principales y usan este mensaje para mostrar información adicional sobre el elemento de menú seleccionado.

Cuando el usuario elige un elemento de comando de un menú, el sistema envía un mensaje [**WM \_ COMMAND**](wm-command.md) al procedimiento de ventana. La palabra de orden bajo del parámetro *wParam* del mensaje **WM \_ COMMAND** contiene el identificador del elemento elegido. El procedimiento de ventana debe examinar el identificador y procesar el mensaje en consecuencia.

Puede guardar la información de un menú mediante la [**estructura MENUINFO.**](/windows/win32/api/winuser/ns-winuser-menuinfo) Si el menú se define con **menuINFO**. **Valor dwStyle** de MNS NOTIFYBYPOS, el sistema envía \_ [**WM \_ MENUCOMMAND**](wm-menucommand.md) en lugar del [**comando WM \_**](wm-command.md) cuando se selecciona un elemento. Esto le permite acceder a la información de la **estructura MENUINFO** y también proporciona el índice del elemento seleccionado directamente.

No todos los menús son accesibles a través de la barra de menús de una ventana. Muchas aplicaciones muestran menús contextuales cuando el usuario hace clic con el botón derecho del mouse en una ubicación específica. Estas aplicaciones deben procesar el mensaje [**\_ CONTEXTMENU de WM**](wm-contextmenu.md) y mostrar un menú contextual, si procede. Si una aplicación no muestra un menú contextual, debe pasar el mensaje **\_ CONTEXTMENU** de WM a la [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para el procesamiento predeterminado.

El [**mensaje \_ WM MENURBUTTONUP**](wm-menurbuttonup.md) se envía cuando el usuario suelta el botón derecho del mouse mientras el cursor está en un elemento de menú. Este mensaje se proporciona para que las aplicaciones puedan mostrar un menú contextual o contextual para un elemento de menú.

Hay algunos mensajes que solo implican menús de arrastrar y colocar. [**EL \_ ELEMENTO MENUGETOBJECT**](wm-menugetobject.md) de WM se envía al propietario de un menú de arrastrar y colocar cuando el cursor del mouse entra en un elemento de menú o se mueve desde el centro de un elemento a la parte superior o inferior de un elemento. El [**mensaje \_ WM MENUDRAG**](wm-menudrag.md) se envía cuando el usuario arrastra realmente un elemento de menú.

Cuando se ha destruido un menú desplegable o un submenú, el sistema envía un mensaje [**\_ WM UNINITMENUPOPUP.**](wm-uninitmenupopup.md)

## <a name="menu-destruction"></a>Destrucción de menús

Si se asigna un menú a una ventana y esa ventana se destruye, el sistema destruye automáticamente el menú y sus submenús, liberando el identificador del menú y la memoria ocupada por el menú. El sistema no destruye automáticamente un menú que no está asignado a una ventana. Una aplicación debe destruir el menú sin signo llamando a la [**función DestroyMenu.**](/windows/desktop/api/Winuser/nf-winuser-destroymenu) De lo contrario, el menú seguirá existiendo en la memoria incluso después de que se cierre la aplicación. Para finalizar el menú activo del subproceso que realiza la llamada, use [**EndMenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu). Si una plataforma no admite **EndMenu,** envíe al propietario del menú activo un [**mensaje \_ CANCELMODE de WM.**](/windows/desktop/winmsg/wm-cancelmode)

 

 