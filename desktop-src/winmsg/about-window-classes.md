---
description: Cada clase de ventana tiene un procedimiento de ventana asociado compartido por todas las ventanas de la misma clase. El procedimiento de ventana procesa mensajes para todas las ventanas de esa clase y, por tanto, controla su comportamiento y apariencia.
ms.assetid: db79fd4b-6a15-4bf9-a0d9-5f6415f6c75f
title: Acerca de las clases de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fcb46d862bf5b9249bb4f13b111ac10c441c3e687dd3fb1784f355c40d14b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932335"
---
# <a name="about-window-classes"></a>Acerca de las clases de ventana

Cada clase de ventana tiene un procedimiento de ventana asociado compartido por todas las ventanas de la misma clase. El procedimiento de ventana procesa mensajes para todas las ventanas de esa clase y, por tanto, controla su comportamiento y apariencia. Para más información, vea [Procedimientos de ventanas](window-procedures.md).

Un proceso debe registrar una clase de ventana para poder crear una ventana de esa clase. El registro de una clase de ventana asocia un procedimiento de ventana, estilos de clase y otros atributos de clase a un nombre de clase. Cuando un proceso especifica un nombre de clase en la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) el sistema crea una ventana con el procedimiento de ventana, los estilos y otros atributos asociados a ese nombre de clase.

En esta sección se tratan los temas siguientes.

-   [Tipos de clases de ventana](#types-of-window-classes)
    -   [Clases del sistema](#system-classes)
    -   [Clases globales de aplicación](#application-global-classes)
    -   [Clases locales de aplicación](#application-local-classes)
-   [Cómo el sistema busca una clase window](#how-the-system-locates-a-window-class)
-   [Registrar una clase Window](#registering-a-window-class)
-   [Elementos de una clase Window](#elements-of-a-window-class)
    -   [Nombre de la clase](#class-name)
    -   [Dirección del procedimiento de ventana](#window-procedure-address)
    -   [Identificador de instancia](#instance-handle)
    -   [Cursor de clase](#class-cursor)
    -   [Iconos de clase](#class-icons)
    -   [Pincel de fondo de clase](#class-background-brush)
    -   [Menú Clase](#class-menu)
    -   [Estilos de clase](#class-styles)
    -   [Memoria de clase adicional](#extra-class-memory)
    -   [Memoria de ventana adicional](#extra-window-memory)

## <a name="types-of-window-classes"></a>Tipos de clases de ventana

Hay tres tipos de clases de ventana:

-   [Clases del sistema](#system-classes)
-   [Clases globales de aplicación](#application-global-classes)
-   [Clases locales de aplicación](#application-local-classes)

Estos tipos difieren en el ámbito y en cuándo y cómo se registran y destruyen.

### <a name="system-classes"></a>Clases del sistema

Una clase del sistema es una clase de ventana registrada por el sistema. Muchas clases del sistema están disponibles para todos los procesos que se van a usar, mientras que otras solo las usa internamente el sistema. Dado que el sistema registra estas clases, un proceso no puede destruirlas.

El sistema registra las clases del sistema para un proceso la primera vez que uno de sus subprocesos llama a una función User Windows Interfaz de dispositivo gráfico (GDI).

Cada aplicación recibe su propia copia de las clases del sistema. Todas las aplicaciones basadas en Windows de 16 bits en las mismas clases del sistema de recurso compartido de VDM, tal como lo hacen en aplicaciones de 16 Windows.

En la tabla siguiente se describen las clases del sistema que están disponibles para su uso por todos los procesos.



| Clase     | Descripción                         |
|-----------|-------------------------------------|
| Botón    | Clase de un botón.             |
| ComboBox  | Clase de un cuadro combinado.          |
| Editar      | Clase para un control de edición.      |
| ListBox   | Clase de un cuadro de lista.           |
| MDIClient | Clase para una ventana de cliente MDI. |
| ScrollBar | Clase de una barra de desplazamiento.         |
| estática    | Clase para un control estático.     |



 

En la tabla siguiente se describen las clases del sistema que solo están disponibles para su uso por el sistema. Se enumeran aquí para mayor integridad.



| Clase      | Descripción                                                            |
|------------|------------------------------------------------------------------------|
| ComboLBox  | Clase del cuadro de lista contenido en un cuadro combinado.                   |
| DDEMLEvent | Clase para eventos datos dinámicos Exchange Management Library (DDEML). |
| Message    | Clase de una ventana de solo mensaje.                                   |
| \#32768    | Clase de un menú.                                                  |
| \#32769    | Clase de la ventana de escritorio.                                      |
| \#32770    | Clase de un cuadro de diálogo.                                            |
| \#32771    | Clase de la ventana del conmutador de tareas.                                  |
| \#32772    | Clase de títulos de icono.                                             |



 

### <a name="application-global-classes"></a>Clases globales de aplicación

Una [clase global de aplicación](#application-global-classes) es una clase de ventana registrada por un archivo ejecutable o DLL que está disponible para todos los demás módulos del proceso. Por ejemplo, el .dll llamar a la función [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) para registrar una clase de ventana que define un control personalizado como una clase global de aplicación para que un proceso que carga el .dll pueda crear instancias del control personalizado.

Para crear una clase que se pueda usar en cada proceso, cree la clase de ventana en un .dll y cargue el .dll en cada proceso. Para cargar el .dll en cada proceso, agregue su nombre al valor **de \_ archivos DLL de AppInit** en la siguiente clave del Registro:

**HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** Windows \\ **NT** \\ **CurrentVersion** \\ **Windows**

Cada vez que se inicia un proceso, el sistema carga el .dll especificado en el contexto del proceso recién iniciado antes de llamar a su función de punto de entrada. El .dll debe registrar la clase durante su procedimiento de inicialización y debe especificar el estilo **\_ GLOBALCLASS de CS.** Para obtener más información, vea [Estilos de clase](#class-styles).

Para quitar una clase global de aplicación y liberar el almacenamiento asociado a ella, use la [**función UnregisterClass.**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)

### <a name="application-local-classes"></a>Clases locales de aplicación

Una [clase local de aplicación](#application-local-classes) es cualquier clase de ventana que un ejecutable .dll registra para su uso exclusivo. Aunque puede registrar cualquier número de clases locales, es habitual registrar solo una. Esta clase de ventana admite el procedimiento de ventana de la ventana principal de la aplicación.

El sistema destruye una clase local cuando se cierra el módulo que lo registró. Una aplicación también puede usar la [**función UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) para quitar una clase local y liberar el almacenamiento asociado a ella.

## <a name="how-the-system-locates-a-window-class"></a>Cómo el sistema busca una clase window

El sistema mantiene una lista de estructuras para cada uno de los tres tipos de clases de ventana. Cuando una aplicación llama a [**la función CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) para crear una ventana con una clase especificada, el sistema usa el procedimiento siguiente para buscar la clase.

1.  Busque en la lista de clases locales de la aplicación una clase con el nombre especificado cuyo identificador de instancia coincida con el identificador de instancia del módulo. (Varios módulos pueden usar el mismo nombre para registrar clases locales en el mismo proceso).
2.  Si el nombre no está en la lista de clases locales de la aplicación, busque en la lista de clases globales de la aplicación.
3.  Si el nombre no está en la lista de clases globales de la aplicación, busque en la lista de clases del sistema.

Todas las ventanas creadas por la aplicación usan este procedimiento, incluidas las ventanas creadas por el sistema en nombre de la aplicación, como los cuadros de diálogo. Es posible invalidar las clases del sistema sin que afecte a otras aplicaciones. Es decir, una aplicación puede registrar una clase local de aplicación con el mismo nombre que una clase del sistema. Esto reemplaza la clase del sistema en el contexto de la aplicación, pero no impide que otras aplicaciones utilicen la clase del sistema.

## <a name="registering-a-window-class"></a>Registro de una clase Window

Una clase de ventana define los atributos de una ventana, como su estilo, icono, cursor, menú y procedimiento de ventana. El primer paso para registrar una clase de ventana es rellenar una estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) con la información de clase de ventana. Para obtener más información, vea [Elementos de una clase Window](#elements-of-a-window-class). A continuación, pase la estructura a [**la función RegisterClassEx.**](/windows/win32/api/winuser/nf-winuser-registerclassexa) Para obtener más información, vea [Usar clases de ventana](using-window-classes.md).

Para registrar una clase global de aplicación, especifique el estilo GLOBALCLASS de CS en el \_ miembro **de** estilo de la [**estructura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) Al registrar una clase local de aplicación, no especifique el estilo **\_ GLOBALCLASS de CS.**

Si registra la clase window con la versión ANSI de [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa), **RegisterClassExA**, la aplicación solicita que el sistema pase parámetros de texto de mensajes a las ventanas de la clase creada mediante el juego de caracteres ANSI; si registra la clase mediante la versión Unicode de **RegisterClassEx**, **RegisterClassExW**, la aplicación solicita que el sistema pase parámetros de texto de mensajes a las ventanas de la clase creada mediante el juego de caracteres Unicode. La [**función IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) permite a las aplicaciones consultar la naturaleza de cada ventana. Para obtener más información sobre las funciones ANSI y Unicode, vea [Convenciones para prototipos de función.](/windows/desktop/Intl/conventions-for-function-prototypes)

El archivo ejecutable o dll que registró la clase es el propietario de la clase . El sistema determina la propiedad de clase del **miembro hInstance** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) que se pasa a la [**función RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) cuando se registra la clase. En el caso de los archivos **DLL, el miembro hInstance** debe ser el identificador de la .dll instancia.

La clase no se destruye cuando se descarga .dll que posee. Por lo tanto, si el sistema llama al procedimiento de ventana para una ventana de esa clase, provocará una infracción de acceso, porque el .dll que contiene el procedimiento de ventana ya no está en memoria. El proceso debe destruir todas las ventanas mediante la clase antes de .dll descarga y llamar a la [**función UnregisterClass.**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)

## <a name="elements-of-a-window-class"></a>Elementos de una clase Window

Los elementos de una clase de ventana definen el comportamiento predeterminado de las ventanas que pertenecen a la clase . La aplicación que registra una clase de ventana asigna elementos a la clase estableciendo los miembros adecuados en una estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) y pasando la estructura a la [**función RegisterClassEx.**](/windows/win32/api/winuser/nf-winuser-registerclassexa) Las [**funciones GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa) [**y GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) recuperan información sobre una clase de ventana determinada. La [**función SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) cambia los elementos de una clase local o global que la aplicación ya ha registrado.

Aunque una clase de ventana completa consta de muchos elementos, el sistema solo requiere que una aplicación proporcione un nombre de clase, la dirección del procedimiento de ventana y un identificador de instancia. Use los demás elementos para definir atributos predeterminados para ventanas de la clase, como la forma del cursor y el contenido del menú de la ventana. Debe inicializar los miembros no usados de la [**estructura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en cero o **NULL.** Los elementos de clase de ventana son como se muestra en la tabla siguiente.



| Elemento                                               | Propósito                                                                                                                                                                                                                                       |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nombre de la clase](#class-name)                             | Distingue la clase de otras clases registradas.                                                                                                                                                                                        |
| [Dirección del procedimiento de ventana](#window-procedure-address) | Puntero a la función que procesa todos los mensajes enviados a las ventanas de la clase y define el comportamiento de la ventana.                                                                                                                      |
| [Identificador de instancia](#instance-handle)                   | Identifica la aplicación o .dll que registró la clase.                                                                                                                                                                                 |
| [Cursor de clase](#class-cursor)                         | Define el cursor del mouse que el sistema muestra para una ventana de la clase .                                                                                                                                                                  |
| [Iconos de clase](#class-icons)                           | Define el icono grande y el icono pequeño.                                                                                                                                                                                                    |
| [Pincel de fondo de clase](#class-background-brush)     | Define el color y el patrón que rellenan el área de cliente cuando se abre o pinta la ventana.                                                                                                                                                 |
| [Menú Clase](#class-menu)                             | Especifica el menú predeterminado para las ventanas que no definen explícitamente un menú.                                                                                                                                                                  |
| [Estilos de clase](#class-styles)                         | Define cómo actualizar la ventana después de moverla o cambiar su tamaño, cómo procesar los doble clics del mouse, cómo asignar espacio para el contexto del dispositivo y otros aspectos de la ventana.                                                       |
| [Memoria de clase adicional](#extra-class-memory)             | Especifica la cantidad de memoria adicional, en bytes, que el sistema debe reservar para la clase . Todas las ventanas de la clase comparten la memoria adicional y pueden usarla para cualquier propósito definido por la aplicación. El sistema inicializa esta memoria en cero. |
| [Memoria adicional de ventana](#extra-window-memory)           | Especifica la cantidad de memoria adicional, en bytes, que el sistema debe reservar para cada ventana que pertenezca a la clase . La memoria adicional se puede usar para cualquier propósito definido por la aplicación. El sistema inicializa esta memoria en cero.          |



 

### <a name="class-name"></a>Class Name (Nombre de clase)

Cada clase de ventana necesita [un nombre de clase](#class-name) para distinguir una clase de otra. Asigne un nombre de clase estableciendo el miembro **lpszClassName** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en la dirección de una cadena terminada en NULL que especifica el nombre. Dado que las clases de ventana son específicas del proceso, los nombres de clase de ventana solo deben ser únicos dentro del mismo proceso. Además, dado que los nombres de clase ocupan espacio en la tabla atom privada del sistema, debe mantener las cadenas de nombre de clase lo más cortas posibles.

La [**función GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname) recupera el nombre de la clase a la que pertenece una ventana determinada.

### <a name="window-procedure-address"></a>Dirección del procedimiento de ventana

Cada clase necesita una dirección de procedimiento de ventana para definir el punto de entrada del procedimiento de ventana que se usa para procesar todos los mensajes de las ventanas de la clase . El sistema pasa mensajes al procedimiento cuando requiere que la ventana lleve a cabo tareas, como pintar su área de cliente o responder a la entrada del usuario. Un proceso asigna un procedimiento de ventana a una clase copiando su dirección en el **miembro lpfnWndProc** de la [**estructura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) Para más información, vea [Procedimientos de ventanas](window-procedures.md).

### <a name="instance-handle"></a>Identificador de instancia

Cada clase de ventana requiere un identificador de instancia para identificar la aplicación o .dll que registró la clase. El sistema requiere identificadores de instancia para realizar un seguimiento de todos los módulos. El sistema asigna un identificador a cada copia de un ejecutable en ejecución o .dll.

El sistema pasa un identificador de instancia a la función de punto de entrada de cada ejecutable (consulte [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)) y .dll (consulte [**DllMain**](/windows/desktop/Dlls/dllmain)). El archivo ejecutable .dll asigna este identificador de instancia a la clase copiandolo en el **miembro hInstance** de la [**estructura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa)

### <a name="class-cursor"></a>Cursor de clase

El *cursor de* clase define la forma del cursor cuando está en el área de cliente de una ventana de la clase . El sistema establece automáticamente el cursor en la forma especificada cuando el cursor entra en el área cliente de la ventana y garantiza que mantiene esa forma mientras permanece en el área cliente. Para asignar una forma de cursor a una clase de ventana, cargue una forma de cursor predefinida mediante la función [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) y, a continuación, asigne el identificador de cursor devuelto al **miembro hCursor** de la estructura [**WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) Como alternativa, proporcione un recurso de cursor personalizado y use la **función LoadCursor** para cargarlo desde los recursos de la aplicación.

El sistema no requiere un cursor de clase. Si una aplicación establece el **miembro hCursor** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en **NULL,** no se define ningún cursor de clase. El sistema asume que la ventana establece la forma del cursor cada vez que el cursor se mueve a la ventana. Una ventana puede establecer la forma del cursor llamando a la [**función SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) cada vez que la ventana recibe el [**mensaje WM \_ MOUSEMOVE.**](/windows/desktop/inputdev/wm-mousemove) Para obtener más información sobre los cursores, vea [Cursores](/windows/desktop/menurc/cursors).

### <a name="class-icons"></a>Iconos de clase

Un *icono de* clase es una imagen que el sistema usa para representar una ventana de una clase determinada. Una aplicación puede tener dos iconos de clase: uno grande y otro pequeño. El sistema muestra el  icono de clase grande de una ventana en la ventana del conmutador de tareas que aparece cuando el usuario presiona ALT+TAB y en las vistas de icono grande de la barra de tareas y el explorador. El *icono de clase pequeña* aparece en la barra de título de una ventana y en las vistas de icono pequeño de la barra de tareas y el explorador.

Para asignar un icono grande y pequeño a una clase de ventana, especifique los identificadores de los iconos en los **miembros hIcon** y **hIconSm** de la estructura [**WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) Las dimensiones de icono deben ajustarse a las dimensiones necesarias para iconos de clase grandes y pequeños. Para un icono de clase grande, puede determinar las dimensiones necesarias especificando los valores **DE SM \_ CXICON** y **SM \_ CYICON** en una llamada a la [**función GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Para un icono de clase pequeña, especifique los **valores DE SM \_ CXSMICON** **y SM \_ CYSMICON.** Para obtener información, vea [Iconos](/windows/desktop/menurc/icons).

Si una aplicación establece los miembros **hIcon** y **hIconSm** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en **NULL,** el sistema usa el icono de aplicación predeterminado como iconos de clase grandes y pequeños para la clase de ventana. Si especifica un icono de clase grande, pero no uno pequeño, el sistema crea un icono de clase pequeña basado en el grande. Sin embargo, si especifica un icono de clase pequeña, pero no uno grande, el sistema usa el icono de aplicación predeterminado como icono de clase grande y el icono especificado como icono de clase pequeña.

Puede invalidar el icono de clase grande o pequeña para una ventana determinada mediante el mensaje [**\_ SETICON de WM.**](wm-seticon.md) Puede recuperar el icono de clase grande o pequeño actual mediante el mensaje [**\_ GETICON de WM.**](wm-geticon.md)

### <a name="class-background-brush"></a>Pincel de fondo de clase

Un *pincel de fondo de* clase prepara el área de cliente de una ventana para el dibujo posterior por parte de la aplicación. El sistema usa el pincel para rellenar el área de cliente con un color sólido o un patrón, con lo que se quitan todas las imágenes anteriores de esa ubicación, tanto si pertenecen a la ventana como si no. El sistema notifica a una ventana que su fondo debe pintarse mediante el envío del [**mensaje \_ ERASEB DOMAINND**](wm-erasebkgnd.md) de WM a la ventana. Para obtener más información, vea [Pinceles](/windows/desktop/gdi/brushes).

Para asignar un pincel de fondo a una clase, cree un pincel mediante las funciones GDI adecuadas y asigne el identificador de pincel devuelto al **miembro hbrBackground** de la estructura [**WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa)

En lugar de crear un pincel, una aplicación puede establecer el **miembro hbrBackground** en uno de los valores de color estándar del sistema. Para obtener una lista de los valores de color del sistema estándar, [**vea SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors).

Para usar un color estándar del sistema, la aplicación debe aumentar el valor de color de fondo en uno. Por ejemplo, **COLOR \_ BACKGROUND** + 1 es el color de fondo del sistema. Como alternativa, puede usar la función [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) para recuperar un identificador de un pincel que se corresponde con un color estándar del sistema y, a continuación, especificar el identificador en el miembro **hbrBackground** de la estructura [**WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa)

El sistema no requiere que una clase de ventana tenga un pincel de fondo de clase. Si este parámetro se establece en **NULL,** la ventana debe pintar su propio fondo cada vez que recibe el [**mensaje \_ ERASEBNDND de WM.**](wm-erasebkgnd.md)

### <a name="class-menu"></a>Menú Clase

Un *menú de clase* define el menú predeterminado que usarán las ventanas de la clase si no se proporciona ningún menú explícito cuando se crean las ventanas. Un menú es una lista de comandos desde los que un usuario puede elegir acciones para que la aplicación lleve a cabo.

Puede asignar un menú a una clase estableciendo el miembro **lpszMenuName** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en la dirección de una cadena terminada en NULL que especifica el nombre del recurso del menú. Se supone que el menú es un recurso de la aplicación determinada. El sistema carga automáticamente el menú cuando es necesario. Si el recurso de menú se identifica mediante un entero y no por un nombre, la aplicación puede establecer el miembro **lpszMenuName** en ese entero aplicando la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) antes de asignar el valor.

El sistema no requiere un menú de clases. Si una aplicación establece el **miembro lpszMenuName** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en **NULL,** las ventanas de la clase no tienen barras de menú. Incluso si no se proporciona ningún menú de clase, una aplicación todavía puede definir una barra de menús para una ventana cuando crea la ventana.

Si se proporciona un menú para una clase y se crea una ventana secundaria de esa clase, se omite el menú. Para obtener más información, vea [Menús](/windows/desktop/menurc/menus).

### <a name="class-styles"></a>Estilos de clase

Los estilos de clase definen elementos adicionales de la clase de ventana. Se pueden combinar dos o más estilos mediante el operador OR bit a bit ( \| ). Para asignar un estilo a una clase de ventana, asigne el estilo al miembro **de** estilo de la [**estructura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) Para obtener una lista de estilos de clase, vea [**Estilos de clase de ventana**](window-class-styles.md).

### <a name="classes-and-device-contexts"></a>Clases y contextos de dispositivo

Un *contexto de dispositivo* es un conjunto especial de valores que las aplicaciones usan para dibujar en el área cliente de sus ventanas. El sistema requiere un contexto de dispositivo para cada ventana de la pantalla, pero permite cierta flexibilidad en la forma en que el sistema almacena y trata ese contexto de dispositivo.

Si no se especifica explícitamente ningún estilo de contexto de dispositivo, el sistema asume que cada ventana usa un contexto de dispositivo recuperado de un grupo de contextos mantenido por el sistema. En tales casos, cada ventana debe recuperar e inicializar el contexto del dispositivo antes de pintarlo y liberarlo después de pintarlo.

Para evitar recuperar un contexto de dispositivo cada vez que necesite pintar dentro de una ventana, una aplicación puede especificar el estilo **\_ OWNDC** de CS para la clase de ventana. Este estilo de clase dirige al sistema a crear un contexto de dispositivo privado, es decir, para asignar un contexto de dispositivo único para cada ventana de la clase. La aplicación solo necesita recuperar el contexto una vez y, a continuación, usarlo para todo el dibujo posterior.

### <a name="extra-class-memory"></a>Memoria de clase adicional

El sistema mantiene una estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) internamente para cada clase de ventana del sistema. Cuando una aplicación registra una clase de ventana, puede dirigir al sistema a asignar y anexar una serie de bytes adicionales de memoria al final de la estructura **WNDCLASSEX.** Esta memoria se denomina *memoria de clase adicional* y la comparten todas las ventanas que pertenecen a la clase . Use la memoria de clase adicional para almacenar cualquier información relacionada con la clase .

Dado que se asigna memoria adicional desde el montón local del sistema, una aplicación debe usar memoria de clase adicional con moderación. Se produce un error en la función [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) si la cantidad de memoria de clase adicional solicitada es superior a 40 bytes. Si una aplicación requiere más de 40 bytes, debe asignar su propia memoria y almacenar un puntero a la memoria en la memoria de clase adicional.

Las [**funciones SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword) [**y SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) copian un valor en la memoria de clase adicional. Para recuperar un valor de la memoria de clase adicional, use las [**funciones GetClassWord**](/windows/win32/api/winuser/nf-winuser-getclassword) [**y GetClassLong.**](/windows/win32/api/winuser/nf-winuser-getclasslonga) El **miembro cbClsExtra** de la [**estructura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) especifica la cantidad de memoria de clase adicional que se asignará. Una aplicación que no use memoria de clase adicional debe inicializar el **miembro cbClsExtra** en cero.

### <a name="extra-window-memory"></a>Memoria adicional de ventana

El sistema mantiene una estructura de datos interna para cada ventana. Al registrar una clase de ventana, una aplicación puede especificar un número de bytes adicionales de memoria, denominado *memoria de ventana adicional.* Al crear una ventana de la clase , el sistema asigna y anexa la cantidad especificada de memoria de ventana adicional al final de la estructura de la ventana. Una aplicación puede usar esta memoria para almacenar datos específicos de la ventana.

Dado que se asigna memoria adicional desde el montón local del sistema, una aplicación debe usar memoria de ventana adicional con moderación. Se produce un error en la función [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) si la cantidad de memoria de ventana adicional solicitada es superior a 40 bytes. Si una aplicación requiere más de 40 bytes, debe asignar su propia memoria y almacenar un puntero a la memoria en la memoria adicional de la ventana.

La [**función SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) copia un valor en la memoria adicional. La [**función GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) recupera un valor de la memoria adicional. El **miembro cbWndExtra** de la [**estructura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) especifica la cantidad de memoria de ventana adicional que se asignará. Una aplicación que no use la memoria debe **inicializar cbWndExtra** en cero.

 

 
