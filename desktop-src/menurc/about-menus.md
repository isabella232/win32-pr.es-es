---
title: Acerca de los menús
description: En este tema se describen los menús.
ms.assetid: fd0b26f1-93cd-421b-9097-8502ab7681e9
keywords:
- recursos, menús
- menús, acerca de
- submenús
- barras de menús
- menús de nivel superior
- menús emergentes
- menús desplegables
- menús, nivel superior
- menús emergentes
- menús, lista desplegable
- nombres de menú
- menús, acceso directo
- menús, ventana
- menús, sistema
- menús, control
- menús contextuales
- Menú Ventana
- Menú sistema
- Menú control
- identificadores de ayuda
- Controladores de menú
- menú, elementos
- elementos de comando
- identificadores de elemento de menú
- posición de elemento de menú
- selección de elementos de menú
- borrar elementos de menú
- menús dibujados por el propietario
- menús, dibujado por el propietario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed5d42eb42aaaaa16eef0b5b118adcfe0f91156e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420610"
---
# <a name="about-menus"></a>Acerca de los menús

Un *menú* es una lista de elementos que especifican opciones o grupos de opciones (un submenú) para una aplicación. Al hacer clic en un elemento de menú, se abre un submenú o se hace que la aplicación lleve a cabo un comando. En esta sección se proporciona información sobre los temas siguientes:

-   [Menús y barras de menús](#menu-bars-and-menus)
    -   [Menús contextuales](#shortcut-menus)
    -   [El menú ventana](#the-window-menu)
    -   [Identificador de ayuda](#help-identifier)
-   [Acceso mediante teclado a menús](#keyboard-access-to-menus)
    -   [Interfaz de teclado estándar](#standard-keyboard-interface)
    -   [Teclas de acceso de menú](#menu-access-keys)
    -   [Teclas de método abreviado de menú](#menu-shortcut-keys)
-   [Creación de menús](#menu-creation)
    -   [Recursos de plantilla de menú](#menu-template-resources)
    -   [Plantilla de menú en memoria](#menu-template-in-memory)
    -   [Controladores de menú](#menu-handles)
    -   [Funciones de creación de menús](#menu-creation-functions)
    -   [Pantalla de menú](#menu-display)
    -   [Menús de clase de ventana](#window-class-menus)
-   [Elementos de menú](#menu-items)
    -   [Elementos de comando y elementos que abren submenús](#command-items-and-items-that-open-submenus)
    -   [Identificador de elemento de menú](#menu-item-identifier)
    -   [Posición de elemento de menú](#menu-item-position)
    -   [Obtener acceso a los elementos de menú mediante programación](#accessing-menu-items-programmatically)
    -   [Elementos de menú predeterminados](#default-menu-items)
    -   [Elementos de menú seleccionados y borrados](#selected-and-clear-menu-items)
    -   [Elementos de menú habilitados, atenuados y deshabilitados](#enabled-grayed-and-disabled-menu-items)
    -   [Elementos de menú resaltados](#highlighted-menu-items)
    -   [Elementos de menú dibujados por el propietario](#owner-drawn-menu-items)
    -   [Separadores de elementos de menú y saltos de línea](#menu-item-separators-and-line-breaks)
-   [Mensajes usados con menús](#messages-used-with-menus)
-   [Destrucción de menús](#menu-destruction)

## <a name="menu-bars-and-menus"></a>Menús y barras de menús

Un menú se organiza en una jerarquía. En el nivel superior de la jerarquía se encuentra la *barra de menús*. que contiene una lista de *menús*, que a su vez pueden contener *submenús*. Una barra de menús se denomina a veces *menú de nivel superior* y los menús y submenús también se conocen como *menús emergentes*.

Un elemento de menú puede ejecutar un comando o abrir un submenú. Un elemento que realiza un comando se denomina elemento de *comando* o *comando*.

Un elemento de la barra de menús casi siempre abre un menú. Las barras de menús raramente contienen elementos de comando. Un menú abierto en la barra de menús se despliega de la barra de menús y a veces se denomina *menú* desplegable. Cuando se muestra un menú desplegable, se adjunta a la barra de menús. Un elemento de menú de la barra de menús que abre un menú desplegable también se denomina *nombre de menú*.

Los nombres de menú de una barra de menús representan las categorías principales de comandos que proporciona una aplicación. Al seleccionar un nombre de menú en la barra de menús, normalmente se abre un menú cuyos elementos de menú corresponden a los comandos de una categoría. Por ejemplo, una barra de menús podría contener un nombre de menú de **archivo** que, cuando se hace clic en el usuario, activa un menú con elementos de menú como **nuevo**, **abrir** y **Guardar**. Para obtener información acerca de una barra de menús, llame a [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo).

Solo una ventana superpuesta o emergente puede contener una barra de menús. una ventana secundaria no puede contener una. Si la ventana tiene una barra de título, el sistema coloca la barra de menús justo debajo de ella. Una barra de menús siempre está visible. Sin embargo, un submenú no es visible hasta que el usuario selecciona un elemento de menú que lo activa. Para obtener más información sobre las ventanas superpuestas y ventanas emergentes, consulte [tipos de ventana](/windows/desktop/winmsg/window-features).

Cada menú debe tener una ventana propietaria. El sistema envía mensajes a la ventana propietaria de un menú cuando el usuario selecciona el menú o elige un elemento del menú.

En esta sección se tratan los temas siguientes.

-   [Menús contextuales](#shortcut-menus)
-   [El menú ventana](#the-window-menu)
-   [Identificador de ayuda](#help-identifier)

### <a name="shortcut-menus"></a>Menús contextuales

El sistema también proporciona *menús contextuales*. No se adjunta un menú contextual a la barra de menús. puede aparecer en cualquier parte de la pantalla. Normalmente, una aplicación asocia un menú contextual con una parte de una ventana, como el área cliente, o con un objeto específico, como un icono. Por esta razón, estos menús también se denominan *menús contextuales*.

Un menú contextual permanece oculto hasta que el usuario lo activa, normalmente al hacer clic con el botón secundario en una selección, una barra de herramientas o un botón de la barra de tareas. El menú suele mostrarse en la posición del símbolo de intercalación o del cursor del mouse.

### <a name="the-window-menu"></a>El menú ventana

El menú **ventana** (también conocido como menú **del sistema** o menú de **control** ) es un menú emergente definido y administrado prácticamente exclusivamente por el sistema operativo. El usuario puede abrir el menú ventana haciendo clic en el icono de la aplicación en la barra de título o haciendo clic con el botón secundario en cualquier lugar de la barra de título.

El menú **ventana** proporciona un conjunto estándar de elementos de menú que el usuario puede elegir para cambiar el tamaño o la posición de una ventana, o cerrar la aplicación. Los elementos del menú ventana se pueden agregar, eliminar y modificar, pero la mayoría de las aplicaciones solo usan el conjunto estándar de elementos de menú. Una ventana superpuesta, emergente o secundaria puede tener un menú ventana. No es habitual que una ventana superpuesta o emergente no incluya un menú ventana.

Cuando el usuario elige un comando en el menú **ventana** , el sistema envía un mensaje de [**WM \_ SYSCOMMAND**](wm-syscommand.md) a la ventana propietaria del menú. En la mayoría de las aplicaciones, el procedimiento de ventana no procesa los mensajes desde el menú ventana. En su lugar, simplemente pasa los mensajes a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para el procesamiento predeterminado del mensaje por el sistema. Si una aplicación agrega un comando al menú ventana, el procedimiento de ventana debe procesar el comando.

Una aplicación puede usar la función [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) para crear una copia del menú de ventana predeterminado que se va a modificar. Cualquier ventana que no use la función **GetSystemMenu** para hacer que su propia copia del menú ventana reciba el menú de ventana estándar.

### <a name="help-identifier"></a>Identificador de ayuda

Asociado a cada barra de menús, menú, submenú y menú contextual es un identificador de ayuda. Si el usuario presiona la tecla F1 mientras el menú está activo, este valor se envía a la ventana propietaria como parte de un mensaje de [**\_ ayuda de WM**](../shell/wm-help.md) .

## <a name="keyboard-access-to-menus"></a>Acceso mediante teclado a menús

El sistema proporciona una interfaz de teclado estándar para los menús. Puede mejorar esta interfaz proporcionando teclas de acceso de tecla de acceso y teclas de método abreviado (acelerador) para los elementos de menú.

En los temas siguientes se describe la interfaz de teclado estándar, las teclas de acceso y las teclas de método abreviado:

-   [Interfaz de teclado estándar](#standard-keyboard-interface)
-   [Teclas de acceso de menú](#menu-access-keys)
-   [Teclas de método abreviado de menú](#menu-shortcut-keys)

### <a name="standard-keyboard-interface"></a>Interfaz de teclado estándar

El sistema está diseñado para funcionar con o sin un mouse u otro dispositivo señalador. Dado que el sistema proporciona una interfaz de teclado estándar, el usuario puede usar el teclado para seleccionar elementos de menú. Esta interfaz de teclado no necesita código especial. Una aplicación recibe un mensaje de comando si el usuario selecciona un elemento de menú mediante el teclado o un mouse. La interfaz de teclado estándar procesa las pulsaciones de tecla siguientes.



| Pulsación de tecla              | Acción                                                                                                                                                                                                                                   |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Carácter alfabético | Selecciona el primer elemento de menú con el carácter especificado como su clave de acceso. Si el elemento seleccionado invoca un menú, se muestra el menú y el primer elemento se resalta. De lo contrario, se elige el elemento de menú.                            |
| ALT                    | Activa y desactiva el modo de barra de menús.                                                                                                                                                                                                     |
| ALT+Barra espaciadora           | Muestra el menú de la ventana.                                                                                                                                                                                                                |
| ENTRAR                  | Activa un menú y selecciona el primer elemento de menú si un elemento tiene un menú asociado. De lo contrario, esta pulsación de tecla elige el elemento como si el usuario suelta el botón del mouse mientras se selecciona el elemento.                              |
| ESC                    | Sale del modo de menú.                                                                                                                                                                                                                         |
| FLECHA IZQUIERDA             | Se desplaza al elemento de menú de nivel superior anterior. Los elementos de menú de nivel superior incluyen los nombres de menú y el menú ventana. Si el elemento seleccionado está en un menú, se selecciona la columna anterior en el menú o se selecciona el elemento de menú de nivel superior anterior. |
| FLECHA DERECHA            | Funciona como la tecla de flecha izquierda, excepto en la dirección opuesta. En los menús, esta pulsación de tecla avanza una columna; Cuando el elemento seleccionado actualmente está en la columna de la derecha, se selecciona el menú siguiente.                              |
| FLECHAS arriba y abajo      | Activa un menú cuando se presiona en el nombre de un menú. Cuando se presiona en un menú, la tecla de flecha arriba selecciona el elemento anterior; la pulsación de tecla flecha abajo selecciona el elemento siguiente.                                                                  |



 

### <a name="menu-access-keys"></a>Teclas de acceso de menú

La interfaz de teclado estándar para los menús se puede mejorar agregando teclas de acceso (mnemónicos) a los elementos de menú. Una tecla de acceso es una letra subrayada en el texto de un elemento de menú. Cuando un menú está activo, el usuario puede seleccionar un elemento de menú presionando la tecla correspondiente a la letra subrayada del elemento. El usuario hace que la barra de menús esté activa presionando la tecla ALT para resaltar el primer elemento en la barra de menús. Un menú está activo cuando se muestra.

Para crear una tecla de acceso para un elemento de menú, anteponga un signo de y comercial a cualquier carácter de la cadena de texto del elemento. Por ejemplo, la cadena de texto "&Move" hace que el sistema subraye la letra "M".

### <a name="menu-shortcut-keys"></a>Teclas de método abreviado de menú

Además de tener una tecla de acceso, un elemento de menú puede tener una tecla de método abreviado asociada. Una tecla de método abreviado es diferente de una tecla de acceso, ya que el menú no tiene que estar activo para que funcione la tecla de método abreviado. Además, una clave de acceso *siempre* está asociada a un elemento de menú, mientras que una tecla de método abreviado *suele* ser (pero no tiene que estar) asociada con un elemento de menú.

El texto que identifica la tecla de método abreviado se agrega a la cadena de texto del elemento de menú. El texto de acceso directo aparece a la derecha del nombre del elemento de menú, después de una barra diagonal inversa y un carácter de tabulación ( \\ t). Por ejemplo, "&Close \\ tAlt + F4" representa un comando CLOSE con la combinación de teclas Alt + F4 como tecla de método abreviado y con la letra "C" como su clave de acceso. Para obtener más información, consulte [aceleradores de teclado](keyboard-accelerators.md).

## <a name="menu-creation"></a>Creación de menús

Puede crear un menú mediante una plantilla de menú o funciones de creación de menús. Las plantillas de menú se suelen definir como recursos. Los recursos de la plantilla de menú se pueden cargar explícitamente o asignar como menú predeterminado para una clase de ventana. También puede crear recursos de plantilla de menú dinámicamente en la memoria.

En los temas siguientes se describe la creación de menús en detalle:

-   [Recursos de plantilla de menú](#menu-template-resources)
-   [Plantilla de menú en memoria](#menu-template-in-memory)
-   [Controladores de menú](#menu-handles)
-   [Funciones de creación de menús](#menu-creation-functions)
-   [Pantalla de menú](#menu-display)
-   [Menús de clase de ventana](#window-class-menus)

### <a name="menu-template-resources"></a>Recursos de plantilla de menú

La mayoría de las aplicaciones crean menús mediante recursos de plantilla de menú. Una *plantilla de menú* define un menú, incluidos los elementos de la barra de menús y todos los menús. Para obtener información sobre cómo crear un recurso de plantilla de menú, vea la documentación que se incluye con las herramientas de desarrollo.

Después de crear un recurso de plantilla de menú y agregarlo al archivo ejecutable (. exe) de la aplicación, puede usar la función [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) para cargar el recurso en la memoria. Esta función devuelve un identificador al menú, que puede asignar a una ventana mediante la función [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) . Puede asignar un menú a cualquier ventana que no sea una ventana secundaria.

La implementación de menús como recursos facilita la localización de la aplicación para su uso en varios países o regiones. Solo se debe localizar el archivo de definición de recursos para cada idioma, no para el código fuente de la aplicación.

### <a name="menu-template-in-memory"></a>Plantilla de menú en memoria

Se puede crear un menú a partir de una plantilla de menú que se compila en tiempo de ejecución en la memoria. Por ejemplo, una aplicación que permite a un usuario personalizar su menú podría crear una plantilla de menú en la memoria en función de las preferencias del usuario. A continuación, la aplicación podría guardar la plantilla en un archivo o en el registro para un uso futuro. Para crear un menú a partir de una plantilla en memoria, use la función [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) . Para obtener descripciones de los formatos de plantilla de menú, vea [recursos de plantilla de menú](#menu-template-resources).

Una plantilla de menú estándar consta de una estructura [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) seguida de una o más estructuras [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .

Una plantilla de menú extendida está formada por una estructura de [**\_ \_ encabezado de plantilla de MENUEX**](menuex-template-header.md) , seguida de una o varias estructuras de [**\_ \_ elemento de plantilla MENUEX**](menuex-template-item.md) .

### <a name="menu-handles"></a>Controladores de menú

El sistema genera un identificador único para cada menú. Un *identificador de menú* es un valor del tipo **HMENU** . Una aplicación debe especificar un identificador de menú en muchas de las funciones de menú. Recibirá un identificador de una barra de menús al crear el menú o cargar un recurso de menú.

Para recuperar un identificador de la barra de menús de un menú que se ha creado o cargado, utilice la función [**GetMenu**](/windows/desktop/api/Winuser/nf-winuser-getmenu) . Para recuperar un identificador del submenú asociado a un elemento de menú, use la función [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) o [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) . Para recuperar un identificador de un menú de ventana, utilice la función [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) .

### <a name="menu-creation-functions"></a>Funciones de creación de menús

Con las funciones de creación de menús, puede crear menús en tiempo de ejecución o agregar elementos de menú a los menús existentes. Puede usar la función [**CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu) para crear una barra de menús vacía y la función [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) para crear un menú vacío. Puede guardar cierta información de configuración de un menú mediante la estructura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) . Para obtener o recuperar la configuración de un menú, use [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo) o [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo). Para agregar elementos a un menú, utilice la función [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) . Todavía se admiten las funciones anteriores [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) y [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) , pero se debe usar **InsertMenuItem** para las nuevas aplicaciones.

### <a name="menu-display"></a>Pantalla de menú

Después de cargar o crear un menú, se debe asignar a una ventana para que el sistema pueda mostrarlo. Puede asignar un menú mediante la definición de un menú clase. Para obtener más información, vea [menús de clase de ventana](#window-class-menus). También puede asignar un menú a una ventana si especifica un identificador para el menú como el parámetro *hMenu* de la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , o bien mediante una llamada a la función [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) .

Para mostrar un menú contextual, use la función [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . Los menús contextuales, también denominados menús emergentes flotantes o menús contextuales, se muestran normalmente cuando se procesa el mensaje de [**\_ CONTEXTMENU de WM**](wm-contextmenu.md) .

Puede asignar un menú a cualquier ventana que no sea una ventana secundaria.

Todavía se admite la función [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) anterior, pero las nuevas aplicaciones deben usar la función [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .

### <a name="window-class-menus"></a>Menús de clase de ventana

Puede especificar un menú predeterminado, denominado menú de *clase,* al registrar una clase de ventana. Para ello, asigne el nombre del recurso de plantilla de menú al miembro **lpszMenuName** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) utilizada para registrar la clase.

De forma predeterminada, a cada ventana se le asigna el menú clase para su clase de ventana, por lo que no es necesario cargar explícitamente el menú y asignarlo a cada ventana. Puede invalidar el menú clase especificando un identificador de menú diferente en una llamada a la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . También puede cambiar el menú de una ventana una vez creado mediante la función [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) . Para obtener más información, vea [clases de ventana](/windows/desktop/winmsg/window-classes).

## <a name="menu-items"></a>Elementos de menú

En los temas siguientes se describe lo que hace el sistema cuando el usuario elige un elemento de menú y las maneras en que una aplicación puede controlar la apariencia y la funcionalidad de un elemento:

-   [Elementos de comando y elementos que abren submenús](#command-items-and-items-that-open-submenus)
-   [Identificador de elemento de menú](#menu-item-identifier)
-   [Posición de elemento de menú](#menu-item-position)
-   [Obtener acceso a los elementos de menú mediante programación](#accessing-menu-items-programmatically)
-   [Elementos de menú predeterminados](#default-menu-items)
-   [Elementos de menú seleccionados y borrados](#selected-and-clear-menu-items)
-   [Elementos de menú habilitados, atenuados y deshabilitados](#enabled-grayed-and-disabled-menu-items)
-   [Elementos de menú resaltados](#highlighted-menu-items)
-   [Elementos de menú dibujados por el propietario](#owner-drawn-menu-items)
-   [Separadores de elementos de menú y saltos de línea](#menu-item-separators-and-line-breaks)

### <a name="command-items-and-items-that-open-submenus"></a>Elementos de comando y elementos que abren submenús

Cuando el usuario elige un elemento de comando, el sistema envía un mensaje de comando a la ventana que posee el menú. Si el elemento de comando está en el menú ventana, el sistema envía el mensaje de [**\_ SYSCOMMAND de WM**](wm-syscommand.md) . De lo contrario, envía el mensaje del [**\_ comando de WM**](wm-command.md) .

Asociado a cada elemento de menú que abre un submenú es un identificador del submenú correspondiente. Cuando el usuario apunta a este tipo de elemento, el sistema abre el submenú. No se envía ningún mensaje de comando a la ventana propietaria. Sin embargo, el sistema envía un mensaje de [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) a la ventana propietaria antes de mostrar el submenú. Puede obtener un identificador para el submenú asociado a un elemento mediante la función [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) o [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

Normalmente, una barra de menús contiene nombres de menús, pero también puede contener elementos de comandos. Un submenú normalmente contiene elementos de comando, pero también puede contener elementos que abren submenús anidados. Al agregar estos elementos a los submenús, puede anidar los menús a cualquier profundidad. Para proporcionar una indicación visual al usuario, el sistema muestra automáticamente una flecha pequeña situada a la derecha del texto de un elemento de menú que abre un submenú.

### <a name="menu-item-identifier"></a>Identificador de Menu-Item

Asociado a cada elemento de menú es un entero único definido por la aplicación, denominado *identificador de elemento de menú*. Cuando el usuario elige un elemento de comando en un menú, el sistema envía el identificador del elemento a la ventana propietaria como parte de un mensaje [**de \_ comando de WM**](wm-command.md) . El procedimiento de ventana examina el identificador para determinar el origen del mensaje y procesa el mensaje en consecuencia. Además, puede especificar un elemento de menú mediante su identificador al llamar a funciones de menú; por ejemplo, para habilitar o deshabilitar un elemento de menú.

Los elementos de menú que abren submenús tienen identificadores del mismo modo que los elementos de comando. Sin embargo, el sistema no envía un mensaje de comando cuando se selecciona un elemento de este tipo en un menú. En su lugar, el sistema abre el submenú asociado al elemento de menú.

Para recuperar el identificador del elemento de menú en una posición especificada, utilice la función [**GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid) o [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

### <a name="menu-item-position"></a>Posición Menu-Item

Además de tener un identificador único, cada elemento de menú de una barra de menús o menú tiene un valor de posición único. El elemento situado más a la izquierda en una barra de menús, o el elemento superior de un menú, tiene la posición cero. El valor de posición se incrementa para los elementos de menú posteriores. El sistema asigna un valor de posición a todos los elementos de un menú, incluidos los separadores. En la ilustración siguiente se muestran los valores de posición de los elementos de una barra de menús y de un menú.

![barra de menús y menú](images/csemn-01.png)

Al llamar a una función de menú que modifica o recupera información sobre un elemento de menú concreto, puede especificar el elemento con su identificador o su posición. Para obtener más información, vea la siguiente sección.

### <a name="accessing-menu-items-programmatically"></a>Obtener acceso a los elementos de menú mediante programación

La mayoría de las funciones de menú permiten especificar un elemento de menú por posición o por comando. Algunas funciones usan las marcas **MF \_ BYPOSITION** y **MF \_ BYCOMMAND** para indicar el algoritmo de búsqueda; otros tienen un parámetro *fByPosition* explícito. Si especifica el elemento de menú por posición, el número de elemento es un índice basado en cero en el menú. Si especifica el elemento de menú por comando, se busca en el menú y en sus submenús un elemento cuyo identificador de menú sea igual al número de elemento proporcionado. Si más de un elemento de la jerarquía de menús coincide con el número de elemento, no se especifica cuál se usa. Si los menús contienen identificadores de menú duplicados, debe usar operaciones de menú basadas en posición para evitar esta ambigüedad.

### <a name="default-menu-items"></a>Elementos de menú predeterminados

Un submenú puede contener un elemento de menú predeterminado. Cuando el usuario abre un submenú haciendo doble clic en, el sistema envía un mensaje de comando a la ventana propietaria del menú y cierra el menú como si se hubiese elegido el elemento de comando predeterminado. Si no hay ningún elemento de comando predeterminado, el submenú permanece abierto. Para recuperar y establecer el elemento predeterminado para un submenú, use las funciones [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem) y [**SetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem) .

### <a name="selected-and-clear-menu-items"></a>Elementos de menú seleccionados y borrados

Un elemento de menú puede estar seleccionado o desactivado. El sistema muestra un mapa de bits junto a los elementos de menú seleccionados para indicar su estado seleccionado. El sistema no muestra un mapa de bits junto a borrar elementos, a menos que se especifique un mapa de bits "Clear" definido por la aplicación. Solo se pueden seleccionar los elementos de menú de un menú; los elementos de una barra de menús no se pueden seleccionar.

Las aplicaciones suelen activar o desactivar un elemento de menú para indicar si una opción está en vigor. Por ejemplo, supongamos que una aplicación tiene una barra de herramientas que el usuario puede mostrar u ocultar mediante un comando de la **barra de herramientas** en un menú. Cuando se oculta la barra de herramientas, el elemento de menú de la **barra de herramientas** está claro. Cuando el usuario elige el comando, la aplicación comprueba el elemento de menú y muestra la barra de herramientas.

Un atributo de marca de verificación controla si un elemento de menú está seleccionado. Puede establecer el atributo de la marca de verificación de un elemento de menú mediante la función [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) . Puede usar la función [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) para determinar si un elemento de menú está seleccionado o desactivado actualmente.

En lugar de [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) y [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate), puede usar las funciones [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) y [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) para recuperar y establecer el estado de activación de un elemento de menú.

A veces, un grupo de elementos de menú corresponde a un conjunto de opciones mutuamente excluyentes. En este caso, puede indicar la opción seleccionada mediante el uso de un elemento de menú de radio seleccionado (análogo a un control de botón de radio). Los elementos de radio seleccionados se muestran con un mapa de bits de viñeta en lugar de un mapa de bits de marca de verificación. Para comprobar un elemento de menú y convertirlo en un elemento de radio, use la función [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) .

De forma predeterminada, el sistema muestra una marca de verificación o un mapa de bits de viñeta junto a los elementos de menú seleccionados y ningún mapa de bits junto a elementos de menú desactivados. Sin embargo, puede usar la función [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) para asociar mapas de bits seleccionados y desactivados definidos por la aplicación con un elemento de menú. Después, el sistema usa los mapas de bits especificados para indicar el estado seleccionado o desactivado del elemento de menú.

Los mapas de bits definidos por la aplicación asociados a un elemento de menú deben tener el mismo tamaño que el mapa de bits de la marca de verificación predeterminada; las dimensiones pueden variar en función de la resolución de la pantalla. Para recuperar las dimensiones correctas, utilice la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Puede crear varios recursos de mapa de bits para diferentes resoluciones de pantalla. Cree un recurso de mapa de bits y escale, si es necesario. o bien, cree un mapa de bits en tiempo de ejecución y dibuje una imagen en él. Los mapas de bits pueden ser monocromáticos o de color. Sin embargo, dado que los elementos de menú se invierten cuando están resaltados, es posible que no se deseen los mapas de bits de colores invertidos. Para obtener más información, vea [mapas de bits](/windows/desktop/gdi/bitmaps).

### <a name="enabled-grayed-and-disabled-menu-items"></a>Elementos de menú habilitados, atenuados y deshabilitados

Un elemento de menú puede estar habilitado, atenuado o deshabilitado. De forma predeterminada, se habilita un elemento de menú. Cuando el usuario elige un elemento de menú habilitado, el sistema envía un mensaje de comando a la ventana propietaria o muestra el submenú correspondiente, dependiendo del tipo de elemento de menú que sea.

Cuando los elementos de menú no están disponibles para el usuario, deben estar atenuados o deshabilitados. Los elementos de menú atenuados y deshabilitados no se pueden elegir. Un elemento deshabilitado tiene el mismo aspecto que un elemento habilitado. Cuando el usuario hace clic en un elemento deshabilitado, el elemento no está seleccionado y no sucede nada. Los elementos deshabilitados pueden ser útiles en, por ejemplo, un tutorial que presenta un menú que parece activo pero no.

Una aplicación atenúa un elemento de menú no disponible para proporcionar una indicación visual al usuario de que un comando no está disponible. Puede utilizar un elemento atenuado cuando una acción no sea adecuada (por ejemplo, puede atenuar el comando **Imprimir** en el menú **archivo** cuando el sistema no tenga una impresora instalada).

La función [**EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem) habilita, atenúa o deshabilita un elemento de menú. Para determinar si un elemento de menú está habilitado, atenuado o deshabilitado, use la función [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

En lugar de [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa), también puede usar la función [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) para determinar si un elemento de menú está habilitado, atenuado o deshabilitado.

### <a name="highlighted-menu-items"></a>Elementos de menú resaltados

El sistema resalta automáticamente los elementos de menú en los menús cuando el usuario los selecciona. Sin embargo, el resaltado se puede Agregar o quitar explícitamente desde un nombre de menú en la barra de menús mediante la función [**HiliteMenuItem**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem) . Esta función no tiene ningún efecto en los elementos de menú de los menús. Sin embargo, cuando se usa **HiliteMenuItem** para resaltar un nombre de menú, el nombre solo parece estar seleccionado. Si el usuario presiona la tecla entrar, no se elige el elemento resaltado. Esta característica puede ser útil en, por ejemplo, una aplicación de entrenamiento que muestre el uso de menús.

### <a name="owner-drawn-menu-items"></a>Owner-Drawn elementos de menú

Una aplicación puede controlar por completo la apariencia de un elemento de menú mediante un *elemento dibujado por el propietario*. Los elementos dibujados por el propietario requieren que una aplicación asuma la responsabilidad total del dibujo seleccionado (resaltado), seleccionado y borrado. Por ejemplo, si una aplicación proporciona un menú fuente, podría dibujar cada elemento de menú mediante la fuente correspondiente; el elemento de Roman se dibujaría con Roman, el elemento de cursiva se dibujaría en cursiva, etc. Para obtener más información, vea [crear Owner-Drawn elementos de menú](using-menus.md).

### <a name="menu-item-separators-and-line-breaks"></a>Separadores de elementos de menú y saltos de línea

El sistema proporciona un tipo especial de elemento de menú, denominado *separador*, que aparece como una línea horizontal. Puede usar un separador para dividir un menú en grupos de elementos relacionados. No se puede usar un separador en una barra de menús y el usuario no puede seleccionar un separador.

Cuando una barra de menús contiene más nombres de menús de los que caben en una línea, el sistema ajusta la barra de menús de forma automática a dos o más líneas. Puede hacer que se produzca un salto de línea en un elemento específico de una barra de menús asignando la marca de tipo **\_ MENUBREAK de MFT** al elemento. El sistema coloca el elemento y todos los elementos subsiguientes en una nueva línea.

Cuando un menú contiene más elementos de los que caben en una columna, el menú se trunca. Puede hacer que se produzca un salto de columna en un elemento específico de un menú asignando la marca **MFT \_ MENUBREAK** Type al elemento o usando la opción MENUBREAK en la instrucción [MenuItem](/windows/desktop/menurc/menuitem-statement) . El sistema coloca el elemento y todos los elementos subsiguientes en una nueva columna. La marca **MFT \_ MENUBARBREAK** Type tiene el mismo efecto, salvo que aparece una línea vertical entre la nueva columna y la antigua.

Si usa las funciones [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) para asignar saltos de línea, debe asignar las marcas de tipo **MF \_ MENUBREAK** o **MF \_ MENUBARBREAK**.

## <a name="messages-used-with-menus"></a>Mensajes usados con menús

La actividad relacionada con el menú informes del sistema mediante el envío de mensajes al procedimiento de ventana de la ventana que posee el menú. El sistema envía una serie de mensajes cuando el usuario selecciona elementos en la barra de menús o hace clic con el botón secundario del mouse para mostrar un menú contextual.

Cuando el usuario activa un elemento en la barra de menús, la ventana propietaria recibe primero un mensaje de [**\_ SYSCOMMAND de WM**](wm-syscommand.md) . Este mensaje incluye una marca que indica si el usuario activó el menú mediante el teclado (SC \_ KEYMENU) o el mouse (SC \_ MOUSEMENU). Para obtener más información, consulte [acceso mediante teclado a menús](#keyboard-access-to-menus).

Después, antes de mostrar los menús, el sistema envía el mensaje de [**\_ INITMENU de WM**](wm-initmenu.md) al procedimiento de ventana para que una aplicación pueda modificar los menús antes de que el usuario los vea. El sistema envía el mensaje de **\_ INITMENU de WM** solo una vez por cada activación de menú.

Cuando el usuario apunta a un elemento de menú que abre un submenú, el sistema envía a la ventana propietaria el mensaje de [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) antes de mostrar el submenú. Este mensaje ofrece a la aplicación una oportunidad para modificar el submenú antes de que se muestre.

Cada vez que el usuario mueve el resaltado de un elemento a otro, el sistema envía un mensaje de [**WM \_ MENUSELECT**](wm-menuselect.md) al procedimiento de ventana de la ventana propietaria del menú. Este mensaje identifica el elemento de menú actualmente seleccionado. Muchas aplicaciones proporcionan un área de información en la parte inferior de sus ventanas principales y usan este mensaje para mostrar información adicional sobre el elemento de menú seleccionado.

Cuando el usuario elige un elemento de comando en un menú, el sistema envía un mensaje de [**\_ comando de WM**](wm-command.md) al procedimiento de ventana. La palabra de orden inferior del parámetro *wParam* del mensaje de **\_ comando de WM** contiene el identificador del elemento elegido. El procedimiento de ventana debe examinar el identificador y procesar el mensaje en consecuencia.

Puede guardar la información de un menú mediante la estructura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) . Si el menú se define con un **MENUINFO**. valor **dwStyle** de mns \_ NOTIFYBYPOS, el sistema envía [**WM \_ MENUCOMMAND**](wm-menucommand.md) en lugar del [**\_ comando WM**](wm-command.md) cuando se selecciona un elemento. Esto permite tener acceso a la información de la estructura **MENUINFO** y también proporciona el índice del elemento seleccionado directamente.

No se puede tener acceso a todos los menús a través de la barra de menús de una ventana. Muchas aplicaciones muestran menús contextuales cuando el usuario hace clic con el botón secundario del mouse en una ubicación específica. Dichas aplicaciones deben procesar el mensaje de [**\_ CONTEXTMENU de WM**](wm-contextmenu.md) y mostrar un menú contextual, si procede. Si una aplicación no muestra un menú contextual, debe pasar el mensaje **de \_ CONTEXTMENU de WM** a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para el procesamiento predeterminado.

El mensaje de [**\_ MENURBUTTONUP de WM**](wm-menurbuttonup.md) se envía cuando el usuario suelta el botón secundario del mouse mientras el cursor está en un elemento de menú. Este mensaje se proporciona para que las aplicaciones puedan mostrar un menú contextual o de acceso directo para un elemento de menú.

Hay algunos mensajes que solo afectan a los menús de arrastrar y colocar. El [**\_ MENUGETOBJECT de WM**](wm-menugetobject.md) se envía al propietario de un menú de arrastrar y colocar cuando el cursor del Mouse entra en un elemento de menú o se mueve desde el centro de un elemento hasta la parte superior o inferior de un elemento. El mensaje de [**\_ MENUDRAG de WM**](wm-menudrag.md) se envía cuando el usuario arrastra realmente un elemento de menú.

Cuando se destruye un menú desplegable o un submenú, el sistema envía un mensaje de [**WM \_ UNINITMENUPOPUP**](wm-uninitmenupopup.md) .

## <a name="menu-destruction"></a>Destrucción de menús

Si se asigna un menú a una ventana y dicha ventana se destruye, el sistema destruye automáticamente el menú y sus submenús, liberando el identificador del menú y la memoria ocupada por el menú. El sistema no destruye automáticamente un menú que no está asignado a una ventana. Una aplicación debe destruir el menú sin asignar llamando a la función [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu) . De lo contrario, el menú sigue existiendo en la memoria incluso después de que se cierre la aplicación. Para finalizar el menú activo del subproceso que realiza la llamada, use [**EndMenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu). Si una plataforma no admite **EndMenu**, envíe un mensaje de [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) al propietario del menú activo.

 

 