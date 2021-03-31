---
description: Cada clase de ventana tiene un procedimiento de ventana asociado compartido por todas las ventanas de la misma clase. El procedimiento de ventana procesa los mensajes de todas las ventanas de esa clase y, por tanto, controla su comportamiento y apariencia.
ms.assetid: db79fd4b-6a15-4bf9-a0d9-5f6415f6c75f
title: Acerca de las clases de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b683176c3fd7904cf3f89b385ce0fa393b89e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278629"
---
# <a name="about-window-classes"></a>Acerca de las clases de ventana

Cada clase de ventana tiene un procedimiento de ventana asociado compartido por todas las ventanas de la misma clase. El procedimiento de ventana procesa los mensajes de todas las ventanas de esa clase y, por tanto, controla su comportamiento y apariencia. Para más información, vea [Procedimientos de ventanas](window-procedures.md).

Un proceso debe registrar una clase de ventana antes de poder crear una ventana de esa clase. Al registrar una clase de ventana se asocia un procedimiento de ventana, estilos de clase y otros atributos de clase con un nombre de clase. Cuando un proceso especifica un nombre de clase en la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , el sistema crea una ventana con el procedimiento de ventana, los estilos y otros atributos asociados a ese nombre de clase.

En esta sección se tratan los temas siguientes.

-   [Tipos de clases de ventana](#types-of-window-classes)
    -   [Clases del sistema](#system-classes)
    -   [Clases globales de la aplicación](#application-global-classes)
    -   [Clases locales de la aplicación](#application-local-classes)
-   [Cómo localiza el sistema una clase de ventana](#how-the-system-locates-a-window-class)
-   [Registrar una clase de ventana](#registering-a-window-class)
-   [Elementos de una clase de ventana](#elements-of-a-window-class)
    -   [Nombre de la clase](#class-name)
    -   [Dirección del procedimiento de ventana](#window-procedure-address)
    -   [Identificador de instancia](#instance-handle)
    -   [Cursor de clase](#class-cursor)
    -   [Iconos de clase](#class-icons)
    -   [Pincel de fondo de clase](#class-background-brush)
    -   [Menú clase](#class-menu)
    -   [Estilos de clase](#class-styles)
    -   [Memoria de clase adicional](#extra-class-memory)
    -   [Memoria de ventana adicional](#extra-window-memory)

## <a name="types-of-window-classes"></a>Tipos de clases de ventana

Hay tres tipos de clases de ventana:

-   [Clases del sistema](#system-classes)
-   [Clases globales de la aplicación](#application-global-classes)
-   [Clases locales de la aplicación](#application-local-classes)

Estos tipos se diferencian en el ámbito y en Cuándo y cómo se registran y destruyen.

### <a name="system-classes"></a>Clases del sistema

Una clase del sistema es una clase de ventana registrada por el sistema. Muchas clases del sistema están disponibles para todos los procesos que se van a usar, mientras que otras solo las utiliza internamente el sistema. Dado que el sistema registra estas clases, un proceso no puede destruirlas.

El sistema registra las clases del sistema para un proceso la primera vez que uno de sus subprocesos llama a un usuario o una función de Windows Interfaz de dispositivo gráfico (GDI).

Cada aplicación recibe su propia copia de las clases del sistema. Todas las aplicaciones basadas en Windows de 16 bits en el mismo VDM comparten clases del sistema, igual que en Windows de 16 bits.

En la tabla siguiente se describen las clases del sistema que están disponibles para que las usen todos los procesos.



| Clase     | Descripción                         |
|-----------|-------------------------------------|
| Botón    | Clase para un botón.             |
| ComboBox  | La clase de un cuadro combinado.          |
| Editar      | La clase para un control de edición.      |
| ListBox   | La clase para un cuadro de lista.           |
| MDIClient | La clase para una ventana de cliente MDI. |
| ScrollBar | La clase de una barra de desplazamiento.         |
| estática    | La clase para un control estático.     |



 

En la tabla siguiente se describen las clases del sistema que solo están disponibles para su uso por parte del sistema. Se enumeran aquí por razones de integridad.



| Clase      | Descripción                                                            |
|------------|------------------------------------------------------------------------|
| ComboLBox  | Clase para el cuadro de lista contenido en un cuadro combinado.                   |
| DDEMLEvent | Clase para los eventos de la biblioteca de administración de Intercambio dinámico de datos (DDEML). |
| Message    | La clase para una ventana de solo mensaje.                                   |
| \#32768    | La clase para un menú.                                                  |
| \#32769    | La clase para la ventana de escritorio.                                      |
| \#32770    | La clase para un cuadro de diálogo.                                            |
| \#32771    | La clase para la ventana de cambio de tarea.                                  |
| \#32772    | Clase para los títulos de los iconos.                                             |



 

### <a name="application-global-classes"></a>Clases globales de la aplicación

Una [clase global de aplicación](#application-global-classes) es una clase de ventana registrada por un archivo ejecutable o dll que está disponible para todos los demás módulos del proceso. Por ejemplo, el archivo. dll puede llamar a la función [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) para registrar una clase de ventana que define un control personalizado como una clase global de aplicación, de modo que un proceso que cargue el archivo. dll pueda crear instancias del control personalizado.

Para crear una clase que se pueda usar en todos los procesos, cree la clase de ventana en un archivo. dll y cargue el archivo. dll en cada proceso. Para cargar el archivo. dll en cada proceso, agregue su nombre al valor de **\_ dll AppInit** en la siguiente clave del registro:

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows**

Cada vez que se inicia un proceso, el sistema carga el archivo. dll especificado en el contexto del proceso recién iniciado antes de llamar a su función de punto de entrada. El archivo. dll debe registrar la clase durante su procedimiento de inicialización y debe especificar el estilo **CS \_ GLOBALCLASS** . Para obtener más información, consulte [estilos de clase](#class-styles).

Para quitar una clase global de la aplicación y liberar el almacenamiento asociado a ella, utilice la función [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) .

### <a name="application-local-classes"></a>Clases locales de la aplicación

Una [clase local de aplicación](#application-local-classes) es cualquier clase de ventana que un archivo ejecutable o. dll registre para su uso exclusivo. Aunque puede registrar cualquier número de clases locales, es habitual registrar solo una. Esta clase de ventana admite el procedimiento de ventana de la ventana principal de la aplicación.

El sistema destruye una clase local cuando se cierra el módulo que la registró. Una aplicación también puede usar la función [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) para quitar una clase local y liberar el almacenamiento asociado a ella.

## <a name="how-the-system-locates-a-window-class"></a>Cómo localiza el sistema una clase de ventana

El sistema mantiene una lista de estructuras para cada uno de los tres tipos de clases de ventana. Cuando una aplicación llama a la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) para crear una ventana con una clase especificada, el sistema utiliza el procedimiento siguiente para localizar la clase.

1.  Busque en la lista de clases locales de la aplicación una clase con el nombre especificado cuyo identificador de instancia coincide con el identificador de instancia del módulo. (Varios módulos pueden usar el mismo nombre para registrar clases locales en el mismo proceso).
2.  Si el nombre no está en la lista clase local de la aplicación, busque en la lista de clases globales de la aplicación.
3.  Si el nombre no está en la lista de clases globales de la aplicación, busque en la lista de clases del sistema.

Todas las ventanas creadas por la aplicación usan este procedimiento, incluidas las ventanas creadas por el sistema en el nombre de la aplicación, como los cuadros de diálogo. Es posible invalidar las clases del sistema sin afectar a otras aplicaciones. Es decir, una aplicación puede registrar una clase local de aplicación que tenga el mismo nombre que una clase de sistema. Esto reemplaza la clase del sistema en el contexto de la aplicación, pero no impide que otras aplicaciones utilicen la clase del sistema.

## <a name="registering-a-window-class"></a>Registrar una clase de ventana

Una clase de ventana define los atributos de una ventana, como su estilo, icono, cursor, menú y procedimiento de ventana. El primer paso en el registro de una clase de ventana consiste en rellenar una estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) con la información de la clase de ventana. Para obtener más información, vea [elementos de una clase de ventana](#elements-of-a-window-class). A continuación, pase la estructura a la función [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Para obtener más información, vea [usar clases de ventana](using-window-classes.md).

Para registrar una clase global de aplicación, especifique el \_ estilo CS GLOBALCLASS en el miembro **Style** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Al registrar una clase local de la aplicación, no especifique el estilo **CS \_ GLOBALCLASS** .

Si registra la clase de ventana mediante la versión ANSI de [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa), **RegisterClassExA**, la aplicación solicita que el sistema pase los parámetros de texto de los mensajes a las ventanas de la clase creada mediante el juego de caracteres ANSI; Si registra la clase con la versión Unicode de **RegisterClassEx**, **RegisterClassExW**, la aplicación solicita que el sistema pase los parámetros de texto de los mensajes a las ventanas de la clase creada mediante el juego de caracteres Unicode. La función [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) permite que las aplicaciones consulten la naturaleza de cada ventana. Para obtener más información sobre las funciones ANSI y Unicode, vea [convenciones de los prototipos de función](/windows/desktop/Intl/conventions-for-function-prototypes).

El archivo ejecutable o DLL que registró la clase es el propietario de la clase. El sistema determina la propiedad de la clase del miembro **hInstance** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) que se pasa a la función [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) cuando se registra la clase. En el caso de los archivos dll, el miembro **hInstance** debe ser el identificador de la instancia de. dll.

La clase no se destruye cuando se descarga el archivo. dll al que pertenece. Por consiguiente, si el sistema llama al procedimiento de ventana de una ventana de esa clase, se producirá una infracción de acceso porque el archivo. dll que contiene el procedimiento de ventana ya no está en la memoria. El proceso debe destruir todas las ventanas que usan la clase antes de que se descargue. dll y llamar a la función [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) .

## <a name="elements-of-a-window-class"></a>Elementos de una clase de ventana

Los elementos de una clase de ventana definen el comportamiento predeterminado de las ventanas que pertenecen a la clase. La aplicación que registra una clase de ventana asigna elementos a la clase estableciendo los miembros adecuados en una estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) y pasando la estructura a la función [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Las funciones [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa) y [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) recuperan información sobre una clase de ventana determinada. La función [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) cambia los elementos de una clase local o global que la aplicación ya ha registrado.

Aunque una clase de ventana completa consta de muchos elementos, el sistema solo requiere que una aplicación proporcione un nombre de clase, la dirección del procedimiento de ventana y un identificador de instancia. Utilice los otros elementos para definir los atributos predeterminados para las ventanas de la clase, como la forma del cursor y el contenido del menú de la ventana. Debe inicializar los miembros no utilizados de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en cero o **null**. Los elementos de la clase Window son como se muestra en la tabla siguiente.



| Elemento                                               | Propósito                                                                                                                                                                                                                                       |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nombre de la clase](#class-name)                             | Distingue la clase de otras clases registradas.                                                                                                                                                                                        |
| [Dirección del procedimiento de ventana](#window-procedure-address) | Puntero a la función que procesa todos los mensajes enviados a Windows en la clase y define el comportamiento de la ventana.                                                                                                                      |
| [Identificador de instancia](#instance-handle)                   | Identifica la aplicación o. dll que registró la clase.                                                                                                                                                                                 |
| [Cursor de clase](#class-cursor)                         | Define el cursor del mouse que el sistema muestra para una ventana de la clase.                                                                                                                                                                  |
| [Iconos de clase](#class-icons)                           | Define el icono grande y el icono pequeño.                                                                                                                                                                                                    |
| [Pincel de fondo de clase](#class-background-brush)     | Define el color y el modelo que rellenan el área cliente cuando la ventana se abre o se pinta.                                                                                                                                                 |
| [Menú clase](#class-menu)                             | Especifica el menú predeterminado para ventanas que no definen explícitamente un menú.                                                                                                                                                                  |
| [Estilos de clase](#class-styles)                         | Define cómo actualizar la ventana después de moverla o cambiar su tamaño, cómo procesar los doble clics del mouse, cómo asignar espacio para el contexto del dispositivo y otros aspectos de la ventana.                                                       |
| [Memoria de clase adicional](#extra-class-memory)             | Especifica la cantidad de memoria adicional, en bytes, que el sistema debe reservar para la clase. Todas las ventanas de la clase comparten la memoria adicional y pueden utilizarla para cualquier propósito definido por la aplicación. El sistema inicializa esta memoria en cero. |
| [Memoria de ventana adicional](#extra-window-memory)           | Especifica la cantidad de memoria adicional, en bytes, que el sistema debe reservar para cada ventana que pertenece a la clase. La memoria adicional se puede usar para cualquier propósito definido por la aplicación. El sistema inicializa esta memoria en cero.          |



 

### <a name="class-name"></a>Class Name (Nombre de clase)

Cada clase de ventana necesita un [nombre de clase](#class-name) para distinguir una clase de otra. Asigne un nombre de clase estableciendo el miembro **lpszClassName** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en la dirección de una cadena terminada en null que especifique el nombre. Dado que las clases de ventana son específicas del proceso, los nombres de clase de ventana solo deben ser únicos dentro del mismo proceso. Además, dado que los nombres de clase ocupan espacio en la tabla de Atom privada del sistema, debe mantener las cadenas de nombre de clase lo más cortas posible.

La función [**getClassName**](/windows/win32/api/winuser/nf-winuser-getclassname) recupera el nombre de la clase a la que pertenece una ventana determinada.

### <a name="window-procedure-address"></a>Dirección del procedimiento de ventana

Cada clase necesita una dirección de procedimiento de ventana para definir el punto de entrada del procedimiento de ventana que se usa para procesar todos los mensajes de Windows en la clase. El sistema pasa los mensajes al procedimiento cuando requiere que la ventana lleve a cabo tareas, como pintar su área cliente o responder a la entrada del usuario. Un proceso asigna un procedimiento de ventana a una clase copiando su dirección en el miembro **lpfnWndProc** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Para más información, vea [Procedimientos de ventanas](window-procedures.md).

### <a name="instance-handle"></a>Identificador de instancia

Cada clase de ventana requiere un identificador de instancia para identificar la aplicación o. dll que registró la clase. El sistema requiere que los identificadores de instancia realicen el seguimiento de todos los módulos. El sistema asigna un identificador a cada copia de un archivo ejecutable o. dll en ejecución.

El sistema pasa un identificador de instancia a la función de punto de entrada de cada archivo ejecutable (vea [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)) y. dll (vea [**DllMain**](/windows/desktop/Dlls/dllmain)). El archivo ejecutable o. dll asigna este identificador de instancia a la clase copiándolo en el miembro **hInstance** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

### <a name="class-cursor"></a>Cursor de clase

El *cursor de clase* define la forma del cursor cuando está en el área cliente de una ventana en la clase. El sistema establece automáticamente el cursor en la forma especificada cuando el cursor entra en el área cliente de la ventana y garantiza que mantiene esa forma mientras permanece en el área cliente. Para asignar una forma de cursor a una clase de ventana, cargue una forma de cursor predefinida mediante la función [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) y, a continuación, asigne el identificador de cursor devuelto al miembro **hCursor** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . También puede proporcionar un recurso de cursor personalizado y usar la función **LoadCursor** para cargarlo desde los recursos de la aplicación.

El sistema no requiere un cursor de clase. Si una aplicación establece el miembro **hCursor** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en **null**, no se define ningún cursor de clase. El sistema asume que la ventana establece la forma del cursor cada vez que el cursor se mueve a la ventana. Una ventana puede establecer la forma de cursor mediante una llamada a la función [**setCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) siempre que la ventana reciba el mensaje de [**\_ MOUSEMOVE de WM**](/windows/desktop/inputdev/wm-mousemove) . Para obtener más información sobre los cursores, vea [cursores](/windows/desktop/menurc/cursors).

### <a name="class-icons"></a>Iconos de clase

Un *icono de clase* es una imagen que el sistema usa para representar una ventana de una clase determinada. Una aplicación puede tener dos iconos de clase: uno grande y otro pequeño. El sistema muestra el icono de *clase grande* de una ventana en la ventana del modificador de tarea que aparece cuando el usuario presiona Alt + Tab y en las vistas de iconos grandes de la barra de tareas y el explorador. El *icono de clase pequeña* aparece en la barra de título de una ventana y en las vistas de iconos pequeños de la barra de tareas y el explorador.

Para asignar un icono grande y pequeño a una clase de ventana, especifique los identificadores de los iconos en los miembros **hIcon** y **hIconSm** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Las dimensiones de los iconos deben ajustarse a las dimensiones necesarias para los iconos de clase grandes y pequeños. Para un icono de clase grande, puede determinar las dimensiones necesarias especificando los valores **SM \_ CXICON** y **SM \_ CYICON** en una llamada a la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Para un icono de clase pequeña, especifique los valores **SM \_ CXSMICON** y **SM \_ CYSMICON** . Para obtener más información, consulte [iconos](/windows/desktop/menurc/icons).

Si una aplicación establece los miembros **hIcon** y **hIconSm** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en **null**, el sistema utiliza el icono de la aplicación predeterminada como iconos de clase grande y pequeña para la clase de ventana. Si especifica un icono de clase grande pero no un pequeño, el sistema crea un icono de clase pequeña basado en el grande. Sin embargo, si especifica un icono de clase pequeña pero no un valor grande, el sistema usa el icono de la aplicación predeterminada como el icono de clase grande y el icono especificado como el icono de clase pequeña.

Puede invalidar el icono de clase grande o pequeña para una ventana determinada mediante el mensaje de [**\_ SETICON de WM**](wm-seticon.md) . Puede recuperar el icono de clase grande o pequeña actual mediante el mensaje [**de \_ GETICON de WM**](wm-geticon.md) .

### <a name="class-background-brush"></a>Pincel de fondo de clase

Un *pincel de fondo de clase* prepara el área cliente de una ventana para el dibujo subsiguiente por la aplicación. El sistema utiliza el pincel para rellenar el área cliente con un color sólido o un patrón, con lo que se quitan todas las imágenes anteriores de esa ubicación, tanto si pertenecen a la ventana como si no. El sistema notifica a una ventana que se debe pintar el fondo enviando el mensaje [**de \_ ERASEBKGND de WM**](wm-erasebkgnd.md) a la ventana. Para obtener más información, consulte [brushes](/windows/desktop/gdi/brushes).

Para asignar un pincel de fondo a una clase, cree un pincel con las funciones GDI apropiadas y asigne el identificador de pincel devuelto al miembro **hbrBackground** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

En lugar de crear un pincel, una aplicación puede establecer el miembro **hbrBackground** en uno de los valores de color estándar del sistema. Para obtener una lista de los valores de color estándar del sistema, vea [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors).

Para usar un color estándar del sistema, la aplicación debe aumentar en uno el valor de color de fondo. Por ejemplo, **color \_ background** + 1 es el color de fondo del sistema. Como alternativa, puede usar la función [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) para recuperar un identificador de un pincel que se corresponda con un color estándar del sistema y, a continuación, especificar el identificador en el miembro **hbrBackground** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

El sistema no requiere que una clase de ventana tenga un pincel de fondo de clase. Si este parámetro se establece en **null**, la ventana debe pintar su propio fondo cada vez que reciba el mensaje de [**\_ ERASEBKGND de WM**](wm-erasebkgnd.md) .

### <a name="class-menu"></a>Menú clase

Un *menú clase* define el menú predeterminado que usarán las ventanas de la clase si no se especifica ningún menú explícito cuando se crean las ventanas. Un menú es una lista de comandos desde los que un usuario puede elegir acciones para que la aplicación lleve a cabo.

Puede asignar un menú a una clase estableciendo el miembro **lpszMenuName** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en la dirección de una cadena terminada en null que especifica el nombre del recurso del menú. Se supone que el menú es un recurso de la aplicación especificada. El sistema carga automáticamente el menú cuando sea necesario. Si el recurso de menú se identifica con un entero y no con un nombre, la aplicación puede establecer el miembro **lpszMenuName** en ese entero aplicando la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) antes de asignar el valor.

El sistema no requiere un menú clase. Si una aplicación establece el miembro **lpszMenuName** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) en **null**, las ventanas de la clase no tienen barras de menús. Aunque no se proporcione ningún menú de clase, una aplicación puede seguir definiendo una barra de menús para una ventana cuando se crea la ventana.

Si se proporciona un menú para una clase y se crea una ventana secundaria de esa clase, se omite el menú. Para obtener más información, vea [menús](/windows/desktop/menurc/menus).

### <a name="class-styles"></a>Estilos de clase

Los estilos de clase definen elementos adicionales de la clase de ventana. Se pueden combinar dos o más estilos mediante el operador bit a bit OR ( \| ). Para asignar un estilo a una clase de ventana, asigne el estilo al miembro de **estilo** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Para obtener una lista de estilos de clase, consulte [**estilos de clase de ventana**](window-class-styles.md).

### <a name="classes-and-device-contexts"></a>Clases y contextos de dispositivos

Un *contexto de dispositivo* es un conjunto especial de valores que las aplicaciones usan para dibujar en el área de cliente de sus ventanas. El sistema requiere un contexto de dispositivo para cada ventana de la pantalla, pero permite cierta flexibilidad en el modo en que el sistema almacena y trata ese contexto de dispositivo.

Si no se proporciona explícitamente ningún estilo de contexto de dispositivo, el sistema asume que cada ventana usa un contexto de dispositivo recuperado de un grupo de contextos mantenidos por el sistema. En tales casos, cada ventana debe recuperar e inicializar el contexto del dispositivo antes de pintar y liberarlo después de pintar.

Para evitar la recuperación de un contexto de dispositivo cada vez que necesita pintar dentro de una ventana, una aplicación puede especificar el estilo **CS \_ OWNDC** para la clase de ventana. Este estilo de clase dirige el sistema para crear un contexto de dispositivo privado, es decir, para asignar un contexto de dispositivo único para cada ventana de la clase. La aplicación solo necesita recuperar el contexto una vez y usarlo para todo el dibujo subsiguiente.

### <a name="extra-class-memory"></a>Memoria de clase adicional

El sistema mantiene internamente una estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) para cada clase de ventana del sistema. Cuando una aplicación registra una clase de ventana, puede dirigir el sistema para que asigne y anexe un número de bytes de memoria adicionales al final de la estructura **WNDCLASSEX** . Esta memoria se denomina *memoria de clase adicional* y la comparten todas las ventanas que pertenecen a la clase. Utilice la memoria de clase adicional para almacenar cualquier información relacionada con la clase.

Dado que se asigna memoria adicional desde el montón local del sistema, una aplicación debe usar la memoria de clase adicional con moderación. Se produce un error en la función [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) si la cantidad de memoria de clase adicional solicitada es superior a 40 bytes. Si una aplicación requiere más de 40 bytes, debe asignar su propia memoria y almacenar un puntero a la memoria en la memoria de clase adicional.

Las funciones [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword) y [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) copian un valor en la memoria de clase adicional. Para recuperar un valor de la memoria de clase adicional, utilice las funciones [**GetClassWord**](/windows/win32/api/winuser/nf-winuser-getclassword) y [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) . El miembro **cbClsExtra** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) especifica la cantidad de memoria de clase adicional que se va a asignar. Una aplicación que no usa memoria de clase adicional debe inicializar el miembro **cbClsExtra** en cero.

### <a name="extra-window-memory"></a>Memoria de ventana adicional

El sistema mantiene una estructura de datos interna para cada ventana. Al registrar una clase de ventana, una aplicación puede especificar un número de bytes de memoria adicionales, denominado *memoria de ventana adicional*. Al crear una ventana de la clase, el sistema asigna y anexa la cantidad especificada de memoria de la ventana adicional al final de la estructura de la ventana. Una aplicación puede utilizar esta memoria para almacenar datos específicos de la ventana.

Dado que se asigna memoria adicional desde el montón local del sistema, una aplicación debe usar la memoria de ventana adicional con moderación. Se produce un error en la función [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) si la cantidad de memoria de ventana adicional solicitada es superior a 40 bytes. Si una aplicación requiere más de 40 bytes, debe asignar su propia memoria y almacenar un puntero a la memoria en la memoria de ventana adicional.

La función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) copia un valor en la memoria adicional. La función [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) recupera un valor de la memoria adicional. El miembro **cbWndExtra** de la estructura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) especifica la cantidad de memoria de ventana adicional que se va a asignar. Una aplicación que no usa la memoria debe inicializar **cbWndExtra** en cero.

 

 
