---
description: En este tema se describen los elementos de programación que utilizan las aplicaciones para crear y usar Windows; administrar relaciones entre ventanas; y tamaño, movimiento y mostrar ventanas.
ms.assetid: e325f8dc-004f-44a9-9122-3be5e44764d6
title: Acerca de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2df510deea689d70bd1ebf5e59cafc92b0389d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276888"
---
# <a name="about-windows"></a>Acerca de Windows

En este tema se describen los elementos de programación que utilizan las aplicaciones para crear y usar Windows; administrar relaciones entre ventanas; y tamaño, movimiento y mostrar ventanas.

La información general incluye los temas siguientes.

-   [Ventana de escritorio](#desktop-window)
-   [Ventanas de aplicación](#application-windows)
    -   [Área de cliente](#client-area)
    -   [Área no cliente](#nonclient-area)
-   [Controles y cuadros de diálogo](#controls-and-dialog-boxes)
-   [Atributos de ventana](#window-attributes)
    -   [Nombre de la clase](#class-name)
    -   [Nombre de la ventana](#window-name)
    -   [Estilo de ventana](#window-style)
    -   [Estilo de ventana extendido](#extended-window-style)
    -   [Position](#position)
    -   [Tamaño](#size)
    -   [Identificador de ventana principal o propietaria](#parent-or-owner-window-handle)
    -   [Identificador de menú o identificador de Child-Window](#menu-handle-or-child-window-identifier)
    -   [Identificador de instancia de aplicación](#application-instance-handle)
    -   [Datos de creación](#creation-data)
    -   [Identificador de ventana](#window-handle)
-   [Creación de ventanas](#creation-data)
    -   [Creación de la ventana principal](#main-window-creation)
    -   [Mensajes de creación de ventanas](#window-creation-messages)
    -   [Aplicaciones multiproceso](#multithread-applications)

## <a name="desktop-window"></a>Ventana de escritorio

Al iniciar el sistema, se crea automáticamente la ventana del escritorio. La *ventana de escritorio* es una ventana definida por el sistema que pinta el fondo de la pantalla y sirve como base para todas las ventanas que se muestran en todas las aplicaciones.

La ventana de escritorio usa un mapa de bits para pintar el fondo de la pantalla. El patrón creado por el mapa de bits se denomina *papel tapiz del escritorio*. De forma predeterminada, la ventana de escritorio usa el mapa de bits de un archivo. bmp especificado en el registro como papel tapiz del escritorio.

La función [**GetDesktopWindow**](/windows/win32/api/winuser/nf-winuser-getdesktopwindow) devuelve un identificador a la ventana del escritorio.

Una aplicación de configuración del sistema, como un elemento del panel de control, cambia el papel tapiz del escritorio mediante la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con el parámetro *WAction* establecido en **SPI \_ SETDESKWALLPAPER** y el parámetro *lpvParam* especificando un nombre de archivo de mapa de bits. **SystemParametersInfo** carga el mapa de bits del archivo especificado, usa el mapa de bits para pintar el fondo de la pantalla y especifica el nuevo nombre de archivo en el registro.

## <a name="application-windows"></a>Ventanas de aplicación

Cada aplicación gráfica basada en Windows crea al menos una ventana, denominada *ventana principal*, que actúa como la interfaz principal entre el usuario y la aplicación. La mayoría de las aplicaciones también crean otras ventanas, ya sea directa o indirectamente, para realizar tareas relacionadas con la ventana principal. Cada ventana desempeña una parte en la visualización de la salida y la recepción de la entrada del usuario.

Al iniciar una aplicación, el sistema también asocia un botón de la barra de tareas a la aplicación. El *botón* de la barra de tareas contiene el icono y el título del programa. Cuando la aplicación está activa, el botón de la barra de tareas se muestra en estado presionado.

Una ventana de la aplicación incluye elementos como una barra de título, una barra de menús, el menú ventana (anteriormente conocido como menú del sistema), el botón minimizar, el botón maximizar, el botón restaurar, el botón Cerrar, un borde de tamaño, un área de cliente, una barra de desplazamiento horizontal y una barra de desplazamiento vertical. La ventana principal de una aplicación normalmente incluye todos estos componentes. En la ilustración siguiente se muestran estos componentes en una ventana principal típica.

![ventana típica](images/cswin-02.png)

### <a name="client-area"></a>Área de cliente

El *área cliente* es la parte de una ventana donde la aplicación muestra la salida, como texto o gráficos. Por ejemplo, una aplicación de publicación de escritorio muestra la página actual de un documento en el área cliente. La aplicación debe proporcionar una función, denominada procedimiento de ventana, para procesar la entrada en la ventana y mostrar el resultado en el área cliente. Para más información, vea [Procedimientos de ventanas](window-procedures.md).

### <a name="nonclient-area"></a>Área no cliente

La barra de título, la barra de menús, el menú ventana, los botones minimizar y maximizar, el borde de ajuste de tamaño y las barras de desplazamiento se conocen colectivamente como el *área no cliente* de la ventana. El sistema administra la mayoría de los aspectos del área no cliente; la aplicación administra la apariencia y el comportamiento de su área de cliente.

La *barra de título* muestra un icono y una línea de texto definidos por la aplicación. Normalmente, el texto especifica el nombre de la aplicación o indica el propósito de la ventana. Una aplicación especifica el icono y el texto al crear la ventana. La barra de título también permite que el usuario mueva la ventana mediante un mouse u otro dispositivo señalador.

La mayoría de las aplicaciones incluyen una *barra de menús* que enumera los comandos admitidos por la aplicación. Los elementos de la barra de menús representan las categorías principales de los comandos. Al hacer clic en un elemento de la barra de menús, normalmente se abre un menú emergente cuyos elementos corresponden a las tareas de una categoría determinada. Al hacer clic en un comando, el usuario dirige la aplicación para llevar a cabo una tarea.

El sistema crea y administra el *menú ventana* . Contiene un conjunto estándar de elementos de menú que, cuando el usuario elige, establece el tamaño o la posición de una ventana, cierra la aplicación o realiza tareas. Para obtener más información, vea [menús](/windows/desktop/menurc/menus).

Los botones de la esquina superior derecha afectan al tamaño y la posición de la ventana. Al hacer clic en el *botón maximizar*, el sistema amplía la ventana al tamaño de la pantalla y coloca la ventana, por lo que abarca todo el escritorio, menos la barra de tareas. Al mismo tiempo, el sistema reemplaza el botón maximizar con el botón Restaurar. Al hacer clic en el *botón Restaurar*, el sistema restaura la ventana a su tamaño y posición anteriores. Al hacer clic en el *botón minimizar*, el sistema reduce la ventana al tamaño del botón de la barra de tareas, coloca la ventana sobre el botón de la barra de tareas y muestra el botón de la barra de tareas en su estado normal. Para restaurar la aplicación a su tamaño y posición anteriores, haga clic en el botón de la barra de tareas. Al hacer clic en el *botón Cerrar*, la aplicación se cierra.

El *borde de ajuste de tamaño* es un área alrededor del perímetro de la ventana que permite al usuario ajustar el tamaño de la ventana mediante un mouse u otro dispositivo señalador.

La barra de *desplazamiento horizontal* y la *barra de desplazamiento vertical* convierten la entrada del mouse o del teclado en los valores que utiliza una aplicación para desplazar el contenido del área de cliente de forma horizontal o vertical. Por ejemplo, una aplicación de procesamiento de texto que muestra un documento largo normalmente proporciona una barra de desplazamiento vertical para permitir al usuario avanzar y retroceder por el documento.

## <a name="controls-and-dialog-boxes"></a>Controles y cuadros de diálogo

Una aplicación puede crear varios tipos de ventanas además de la ventana principal, incluidos los controles y los cuadros de diálogo.

Un *control* es una ventana que una aplicación usa para obtener una parte específica de la información del usuario, como el nombre de un archivo que se va a abrir o el tamaño de punto deseado de una selección de texto. Las aplicaciones también usan controles para obtener la información necesaria para controlar una característica determinada de una aplicación. Por ejemplo, una aplicación de procesamiento de texto suele proporcionar un control para permitir que el usuario Active y desactive el ajuste de palabras. Para obtener más información, vea [controles de Windows](/windows/desktop/Controls/window-controls).

Los controles siempre se usan junto con otra ventana, normalmente un cuadro de diálogo. Un *cuadro de diálogo* es una ventana que contiene uno o más controles. Una aplicación utiliza un cuadro de diálogo para pedir al usuario una entrada necesaria para completar un comando. Por ejemplo, una aplicación que incluye un comando para abrir un archivo mostraría un cuadro de diálogo que incluye los controles en los que el usuario especifica una ruta de acceso y un nombre de archivo. Normalmente, los cuadros de diálogo no usan el mismo conjunto de componentes de ventana que una ventana principal. La mayoría tienen una barra de título, un menú ventana, un borde (sin ajuste de tamaño) y un área cliente, pero normalmente no tienen una barra de menús, botones minimizar y maximizar o barras de desplazamiento. Para obtener más información, consulte [cuadros de diálogo](/windows/desktop/dlgbox/dialog-boxes).

Un *cuadro de mensaje* es un cuadro de diálogo especial que muestra una nota, precaución o advertencia al usuario. Por ejemplo, un cuadro de mensaje puede informar al usuario de un problema que ha encontrado la aplicación al realizar una tarea. Para obtener más información, consulte [cuadros de mensaje](/windows/desktop/dlgbox/about-dialog-boxes).

## <a name="window-attributes"></a>Atributos de ventana

Una aplicación debe proporcionar la siguiente información al crear una ventana. (Con la excepción del [identificador de ventana](#window-handle), que la función de creación devuelve para identificar de forma única la nueva ventana).

-   [Nombre de la clase](#class-name)
-   [Nombre de la ventana](#window-name)
-   [Estilo de ventana](#window-style)
-   [Estilo de ventana extendido](#extended-window-style)
-   [Position](#position)
-   [Tamaño](#size)
-   [Identificador de ventana principal o propietaria](#parent-or-owner-window-handle)
-   [Identificador de menú o identificador de Child-Window](#menu-handle-or-child-window-identifier)
-   [Identificador de instancia de aplicación](#application-instance-handle)
-   [Datos de creación](#creation-data)
-   [Identificador de ventana](#window-handle)

Estos atributos de ventana se describen en las secciones siguientes.

### <a name="class-name"></a>Class Name (Nombre de clase)

Cada ventana pertenece a una clase de ventana. Una aplicación debe registrar una clase de ventana antes de crear las ventanas de esa clase. La *clase de ventana* define la mayoría de los aspectos de la apariencia y el comportamiento de una ventana. El componente principal de una clase de ventana es el *procedimiento de ventana*, una función que recibe y procesa todas las entradas y solicitudes enviadas a la ventana. El sistema proporciona la entrada y las solicitudes en forma de *mensajes*. Para obtener más información, vea [clases de ventana](window-classes.md), procedimientos de [ventana](window-procedures.md)y [mensajes y colas de mensajes](messages-and-message-queues.md).

### <a name="window-name"></a>Nombre de la ventana

Un *nombre de ventana* es una cadena de texto que identifica una ventana para el usuario. Una ventana principal, un cuadro de diálogo o un cuadro de mensaje normalmente muestra el nombre de la ventana en la barra de título, si está presente. Un control puede mostrar su nombre de ventana, dependiendo de la clase del control. Por ejemplo, botones, controles de edición y controles estáticos muestran los nombres de ventana dentro del rectángulo ocupado por el control. Sin embargo, los controles como cuadros de lista y cuadros combinados no muestran los nombres de las ventanas.

Para cambiar el nombre de la ventana después de crear una ventana, use la función [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) . Esta función utiliza las funciones [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha) y [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) para recuperar la cadena de nombre de ventana actual de la ventana.

### <a name="window-style"></a>Estilo de ventana

Cada ventana tiene uno o varios estilos de ventana. Un estilo de ventana es una constante con nombre que define un aspecto de la apariencia y el comportamiento de la ventana no especificados por la clase de la ventana. Normalmente, una aplicación establece estilos de ventana al crear ventanas. También puede establecer los estilos después de crear una ventana mediante la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

El sistema y, en cierta medida, el procedimiento de ventana para la clase, interpreta los estilos de ventana.

Algunos estilos de ventana se aplican a todas las ventanas, pero la mayoría se aplican a las ventanas de clases de ventana específicas. Los estilos de ventana generales se representan mediante constantes que comienzan por el \_ prefijo WS; se pueden combinar con el operador OR para formar distintos tipos de ventanas, incluidas las ventanas principales, los cuadros de diálogo y las ventanas secundarias. Los estilos de ventana específicos de la clase definen la apariencia y el comportamiento de las ventanas que pertenecen a las clases de control predefinidas. Por ejemplo, la clase **ScrollBar** especifica un control de barra de desplazamiento, pero los estilos [**SBS \_ horizontal**](../controls/scroll-bar-control-styles.md) y **SBS \_ Vert** determinan si se crea un control de barra de desplazamiento horizontal o vertical.

Para obtener listas de estilos que Windows puede usar, vea los temas siguientes:

-   [**Estilos de ventana**](window-styles.md)
-   [Estilos de botón](../controls/button-styles.md)
-   [Estilos de cuadro combinado](../controls/combo-box-styles.md)
-   [Editar estilos de control](../controls/edit-control-styles.md)
-   [Estilos de cuadro de lista](../controls/list-box-styles.md)
-   [Estilos de control Rich Edit](../controls/rich-edit-control-styles.md)
-   [Estilos de control de barra de desplazamiento](../controls/scroll-bar-control-styles.md)
-   [Estilos de control estáticos](../controls/static-control-styles.md)

### <a name="extended-window-style"></a>Estilo de ventana extendido

Cada ventana puede tener opcionalmente uno o varios estilos de ventana extendidos. Un *estilo de ventana extendida* es una constante con nombre que define un aspecto de la apariencia y el comportamiento de la ventana que no se especifica en la clase de ventana ni en los demás estilos de ventana. Normalmente, una aplicación establece estilos extendidos de ventana al crear ventanas. También puede establecer los estilos después de crear una ventana mediante la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

Para obtener más información, vea [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa).

### <a name="position"></a>Posición

La posición de una ventana se define como las coordenadas de la esquina superior izquierda. Estas coordenadas, a veces denominadas coordenadas de ventana, siempre se relacionan con la esquina superior izquierda de la pantalla o, en el caso de una ventana secundaria, la esquina superior izquierda del área de cliente de la ventana primaria. Por ejemplo, una ventana de nivel superior que tiene las coordenadas (10, 10) se coloca 10 píxeles a la derecha de la esquina superior izquierda de la pantalla y 10 píxeles hacia abajo. Una ventana secundaria que tiene las coordenadas (10, 10) se coloca 10 píxeles a la derecha de la esquina superior izquierda del área de cliente de la ventana primaria y 10 píxeles hacia abajo.

La función [**WindowFromPoint**](/windows/win32/api/winuser/nf-winuser-windowfrompoint) recupera un identificador de la ventana que ocupa un punto determinado en la pantalla. Del mismo modo, las funciones [**ChildWindowFromPoint**](/windows/win32/api/winuser/nf-winuser-childwindowfrompoint) y [**ChildWindowFromPointEx**](/windows/win32/api/winuser/nf-winuser-childwindowfrompointex) recuperan un identificador de la ventana secundaria que ocupa un punto determinado en el área cliente de la ventana primaria. Aunque **ChildWindowFromPointEx** puede omitir las ventanas secundarias invisible, deshabilitadas y transparentes, **ChildWindowFromPoint** no puede.

### <a name="size"></a>Tamaño

El tamaño de una ventana (ancho y alto) se proporciona en píxeles. Una ventana puede tener un ancho o un alto nulos. Si una aplicación establece el ancho y el alto de una ventana en cero, el sistema establece el tamaño mínimo predeterminado de la ventana. Para detectar el tamaño mínimo predeterminado de la ventana, una aplicación utiliza la función [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con las marcas **SM \_ CXMIN** y **SM \_ CYMIN** .

Es posible que una aplicación tenga que crear una ventana con un área de cliente de un tamaño determinado. Las funciones [**AdjustWindowRect**](/windows/win32/api/winuser/nf-winuser-adjustwindowrect) y [**AdjustWindowRectEx**](/windows/win32/api/winuser/nf-winuser-adjustwindowrectex) calculan el tamaño necesario de una ventana en función del tamaño deseado del área cliente. La aplicación puede pasar los valores de tamaño resultantes a la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

Una aplicación puede ajustar el tamaño de una ventana para que sea extremadamente grande; sin embargo, no debe cambiar el tamaño de una ventana para que sea mayor que la pantalla. Antes de establecer el tamaño de una ventana, la aplicación debe comprobar el ancho y el alto de la pantalla mediante [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con las marcas **SM \_ CXSCREEN** y **SM \_ CYSCREEN** .

### <a name="parent-or-owner-window-handle"></a>Identificador de ventana principal o propietaria

Una ventana puede tener una ventana primaria. Una ventana que tiene un elemento primario se denomina *ventana secundaria*. La *ventana primaria* proporciona el sistema de coordenadas que se usa para colocar una ventana secundaria. Tener una ventana primaria afecta a aspectos de la apariencia de una ventana; por ejemplo, una ventana secundaria se recorta para que ninguna parte de la ventana secundaria pueda aparecer fuera de los bordes de la ventana primaria.

Una ventana que no tiene un elemento primario, o cuyo elemento primario es la ventana del escritorio, se denomina *ventana de nivel superior*. Una aplicación puede utilizar la función [**EnumWindows**](/windows/win32/api/winuser/nf-winuser-enumwindows) para obtener un identificador de cada ventana de nivel superior de la pantalla. **EnumWindows** pasa el identificador a cada ventana de nivel superior, a su vez, a una función de devolución de llamada definida por la aplicación, [**EnumWindowsProc**](/previous-versions/windows/desktop/legacy/ms633498(v=vs.85)).

Una ventana de nivel superior puede ser propietaria o pertenecer a otra ventana. Una *ventana de propiedad* siempre aparece delante de su ventana propietaria, está oculta cuando su ventana propietaria está minimizada y se destruye cuando se destruye su ventana propietaria. Para obtener más información, consulte [ventanas de propiedad](window-features.md#owned-windows).

### <a name="menu-handle-or-child-window-identifier"></a>Identificador de menú o identificador de Child-Window

Una ventana secundaria puede tener un identificador *de ventana secundaria* , un valor único definido por la aplicación asociado a la ventana secundaria. Los identificadores de las ventanas secundarias son especialmente útiles en las aplicaciones que crean varias ventanas secundarias. Al crear una ventana secundaria, una aplicación especifica el identificador de la ventana secundaria. Después de crear la ventana, la aplicación puede cambiar el identificador de la ventana mediante la función [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) , o bien puede recuperar el identificador mediante la función [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) .

Cada ventana, excepto una ventana secundaria, puede tener un menú. Una aplicación puede incluir un menú proporcionando un identificador de menú al registrar la clase de la ventana o al crear la ventana.

### <a name="application-instance-handle"></a>Identificador de instancia de aplicación

Cada aplicación tiene un identificador de instancia asociado a ella. El sistema proporciona el identificador de instancia para una aplicación cuando se inicia la aplicación. Dado que puede ejecutar varias copias de la misma aplicación, el sistema utiliza identificadores de instancia internamente para distinguir una instancia de una aplicación de otra. La aplicación debe especificar el identificador de instancia en muchas ventanas diferentes, incluidas las que crean Windows.

### <a name="creation-data"></a>Datos de creación

Cada ventana puede tener asociados datos de creación definidos por la aplicación. Cuando se crea la ventana por primera vez, el sistema pasa un puntero a los datos de al procedimiento de ventana de la ventana que se va a crear. El procedimiento de ventana utiliza los datos para inicializar las variables definidas por la aplicación.

### <a name="window-handle"></a>Identificador de ventana

Después de crear una ventana, la función de creación devuelve un *identificador de ventana* que identifica de forma única la ventana. Un identificador de ventana tiene el tipo de datos **hWnd** ; una aplicación debe usar este tipo al declarar una variable que contiene un identificador de ventana. Una aplicación utiliza este identificador en otras funciones para dirigir sus acciones a la ventana.

Una aplicación puede usar la función [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) para detectar si existe una ventana con el nombre de clase o de ventana especificado en el sistema. Si existe una ventana de este tipo, **FindWindow** devuelve un identificador a la ventana. Para limitar la búsqueda a las ventanas secundarias de una aplicación determinada, use la función [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) .

La función [**IsWindow**](/windows/win32/api/winuser/nf-winuser-iswindow) determina si un identificador de ventana identifica una ventana válida existente. Hay constantes especiales que pueden reemplazar un identificador de ventana en determinadas funciones. Por ejemplo, una aplicación puede usar **la \_ difusión HWND** en las funciones [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) y [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) , o **hWnd \_ Desktop** en la función [**MapWindowPoints**](/windows/desktop/api/winuser/nf-winuser-mapwindowpoints) .

## <a name="window-creation"></a>Creación de ventanas

Para crear ventanas de aplicación, use la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Debe proporcionar la información necesaria para definir los atributos de la ventana. **CreateWindowEx** tiene un parámetro, *DwExStyle*, que **CreateWindow** no tiene; de lo contrario, las funciones son idénticas. De hecho, **CreateWindow** simplemente llama a **CreateWindowEx** con el parámetro *dwExStyle* establecido en cero. Por esta razón, el resto de esta información general solo se refiere a **CreateWindowEx**.

Esta sección contiene los siguientes temas:

-   [Creación de la ventana principal](#main-window-creation)
-   [Mensajes de creación de ventanas](#window-creation-messages)
-   [Aplicaciones multiproceso](#multithread-applications)

> [!Note]  
> Hay funciones adicionales para crear ventanas de propósito especial, como cuadros de diálogo y cuadros de mensaje. Para obtener más información, vea [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa), [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga)y [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).

 

### <a name="main-window-creation"></a>Creación de la ventana principal

Cada aplicación basada en Windows debe tener [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) como función de punto de entrada. **WinMain** realiza varias tareas, entre las que se incluye el registro de la clase de ventana para la ventana principal y la creación de la ventana principal. **WinMain** registra la clase de ventana principal mediante una llamada a la función [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) y crea la ventana principal mediante una llamada a la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

La función [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) también puede limitar la aplicación a una sola instancia. Cree una exclusión mutua con nombre mediante la función [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) . Si [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el **error \_ ya \_ existe**, existe otra instancia de la aplicación (creó la exclusión mutua) y debe salir de **WinMain**.

El sistema no muestra automáticamente la ventana principal después de crearla. en su lugar, una aplicación debe usar la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) para mostrar la ventana principal. Después de crear la ventana principal, la función [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) de la aplicación llama a **ShowWindow**, pasándole dos parámetros: un identificador de la ventana principal y una marca que especifica si la ventana principal se debe minimizar o maximizar cuando se muestra por primera vez. Normalmente, la marca se puede establecer en cualquiera de las constantes que comienzan con el \_ prefijo SW. Sin embargo, cuando se llama a **ShowWindow** para mostrar la ventana principal de la aplicación, la marca debe establecerse en **SW \_ SHOWDEFAULT**. Esta marca indica al sistema que muestre la ventana según lo indicado por el programa que inició la aplicación.

Si una clase de ventana se registró con la versión Unicode de [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa), la ventana solo recibe mensajes Unicode. Para determinar si una ventana usa el juego de caracteres Unicode o no, llame a [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode).

### <a name="window-creation-messages"></a>Mensajes de Window-Creation

Al crear una ventana, el sistema envía mensajes al procedimiento de ventana para la ventana. El sistema envía el mensaje de [**WM \_ NCCREATE**](wm-nccreate.md) después de crear el área no cliente de la ventana y el mensaje de [**\_ creación de WM**](wm-create.md) después de crear el área cliente. El procedimiento de ventana recibe ambos mensajes antes de que el sistema muestre la ventana. Ambos mensajes incluyen un puntero a una estructura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) que contiene toda la información especificada en la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Normalmente, el procedimiento de ventana realiza tareas de inicialización al recibir estos mensajes.

Al crear una ventana secundaria, el sistema envía el mensaje de [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) a la ventana primaria después de enviar los mensajes de WM [**\_ NCCREATE**](wm-nccreate.md) y [**WM \_ Create**](wm-create.md) . También envía otros mensajes al crear una ventana. El número y el orden de estos mensajes dependen de la clase de ventana y el estilo, así como de la función utilizada para crear la ventana. Estos mensajes se describen en otros temas de este archivo de ayuda.

### <a name="multithread-applications"></a>Aplicaciones multiproceso

Una aplicación basada en Windows puede tener varios subprocesos de ejecución y cada subproceso puede crear ventanas. El subproceso que crea una ventana debe contener el código para su procedimiento de ventana.

Una aplicación puede usar la función [**EnumThreadWindows**](/windows/win32/api/winuser/nf-winuser-enumthreadwindows) para enumerar las ventanas creadas por un subproceso determinado. Esta función pasa el identificador a cada ventana de subproceso, a su vez, a una función de devolución de llamada definida por la aplicación, [**EnumThreadWndProc**](/previous-versions/windows/desktop/legacy/ms633496(v=vs.85)).

La función [**GetWindowThreadProcessId**](/windows/win32/api/winuser/nf-winuser-getwindowthreadprocessid) devuelve el identificador del subproceso que creó una ventana determinada.

Para establecer el estado de presentación de una ventana creada por otro subproceso, utilice la función [**ShowWindowAsync**](/windows/win32/api/winuser/nf-winuser-showwindowasync) .

 

 
