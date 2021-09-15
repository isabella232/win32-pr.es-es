---
description: La ayuda en línea puede tener una variedad de formas, desde información conceptual detallada hasta definiciones rápidas. En este tema se incluyen las siguientes secciones.
title: Control de la Ayuda en línea
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2a3f6034-6ba6-4204-a2e1-59995fbf40fe
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f1c125df135068c2eee37cb33a8a9d2b281b1f83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572528"
---
# <a name="handling-online-help"></a>Control de la Ayuda en línea

La ayuda en línea puede tener una variedad de formas, desde información conceptual detallada hasta definiciones rápidas. En este tema se incluyen las siguientes secciones.

-   [Acerca de la Ayuda](#about-help)
    -   [Solicitudes de ayuda](#help-requests)
    -   [Ayuda para mostrar y Windows ayuda](#help-display-and-windows-help)
-   [Uso de la Ayuda](#using-help)
    -   [Proporcionar ayuda en un cuadro de diálogo](#providing-help-in-a-dialog-box)
    -   [Establecer la apariencia de una ventana de Ayuda secundaria](#setting-the-appearance-of-a-secondary-help-window)

## <a name="about-help"></a>Acerca de la Ayuda

Un elemento importante de una aplicación fácil de usar está disponible en la ayuda en línea. Windows proporciona funciones y mensajes que, cuando se usan junto con la aplicación Windows Help, facilita la implementación de ayuda en línea en la aplicación. Esta información general describe los elementos de las Windows que admiten la ayuda en línea. Describe cómo usar estos elementos para proporcionar a los usuarios un medio para solicitar ayuda y explica cómo usar la aplicación Windows Ayuda para mostrar ayuda.

### <a name="help-requests"></a>Solicitudes de ayuda

La mayoría de las aplicaciones basadas en Windows proporcionan información de ayuda en línea de diversas formas, desde la ayuda conceptual que explica el propósito de las características de una aplicación hasta la ayuda emergente que proporciona definiciones rápidas de elementos individuales en la interfaz de usuario de la aplicación. Las funciones y los mensajes se usan para proporcionar a los usuarios diversas maneras de solicitar acceso a esta información. En las secciones siguientes se describen estas solicitudes de ayuda.

### <a name="help-menu"></a>Menú Ayuda

La mayoría de las aplicaciones proporcionan acceso de usuario a la información de ayuda mediante la inclusión de **un menú** ayuda en la ventana principal. Cuando el usuario selecciona un  elemento de un menú Ayuda, el procedimiento de ventana correspondiente recibe un [**mensaje WM \_ COMMAND**](../menurc/wm-command.md) que identifica el elemento seleccionado. La aplicación responde mostrando la información de ayuda adecuada, como una lista de temas de ayuda, un índice o una introducción a la aplicación.

### <a name="help-from-the-keyboard"></a>Ayuda del teclado

Windows proporciona acceso de usuario para obtener información de ayuda desde el teclado notificando a la aplicación cada vez que el usuario presiona la tecla F1. El sistema envía un [**mensaje WM \_ HELP**](wm-help.md) a la ventana que tenía el foco del teclado cuando el usuario presionaba la tecla. Si la ventana es una ventana secundaria (por ejemplo, un control en un cuadro de diálogo), la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pasa el mensaje a la ventana primaria. Si un menú está activo cuando se presiona F1, el sistema envía el mensaje a la ventana asociada al menú. La aplicación responde mostrando información de ayuda asociada a la ventana, el control o el menú que tiene el foco o está activo. Por ejemplo, si el usuario selecciona un control en un cuadro de diálogo y presiona F1, la aplicación muestra información de ayuda para ese control.

El *parámetro lParam* de [**WM \_ HELP**](wm-help.md) es un puntero a una estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contiene información detallada sobre el elemento para el que se solicita ayuda. Esta información se usa para determinar el tema de ayuda que se va a mostrar. La **estructura HELPINFO** también incluye las coordenadas del cursor del mouse en el momento en que el usuario presiona la tecla. Puede usar esta información para proporcionar ayuda basada en la ubicación del cursor del mouse.

### <a name="help-from-the-mouse"></a>Ayuda del mouse

Windows proporciona al usuario acceso a la información de ayuda del mouse notificando a la aplicación cada vez que el usuario hace clic en el botón derecho del mouse o hace clic en una ventana, control o menú después de hacer clic en el botón Pregunta (?). La aplicación responde mostrando información de ayuda asociada a la ventana, control o menú dados.

El sistema envía un [**mensaje \_ CONTEXTMENU de WM**](../menurc/wm-contextmenu.md) cuando el usuario hace clic en el botón derecho del mouse. La ventana en la que se hizo clic recibe el mensaje. Si la ventana es una ventana secundaria, como un control , la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pasa el mensaje a la ventana primaria. El **mensaje \_ CONTEXTMENU de WM** especifica las coordenadas del cursor del mouse. La coordenada x está en la palabra de orden bajo del parámetro *lParam* y la coordenada y está en la palabra de orden superior. Si el usuario hizo clic en un control, *el parámetro wParam* es el identificador del control que recibió el clic.

El sistema envía un [**mensaje WM \_ HELP**](wm-help.md) cuando el usuario hace clic en un elemento de una ventana después de hacer clic en el botón Pregunta (?) que aparece en la barra de título de la ventana. Puede agregar un botón Pregunta a una barra de título especificando el estilo **\_ \_ CONTEXTHELP** de WS EX en la [**función CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) al crear la ventana. El parámetro *lParam* de **WM \_ HELP** es un puntero a una estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contiene información detallada sobre el elemento para el que se solicita ayuda, incluidas las coordenadas del cursor del mouse en el momento en que el usuario hizo clic en el botón del mouse.

El botón Pregunta solo se recomienda para su uso en cuadros de diálogo. En el pasado, las aplicaciones han proporcionado acceso de usuario para obtener información de ayuda sobre un cuadro de diálogo proporcionando un **botón Ayuda** en el cuadro de diálogo. Este método ya no se recomienda. En su lugar, use el botón Pregunta.

### <a name="help-display-and-windows-help"></a>Ayuda para mostrar y Windows ayuda

Una vez que una aplicación recibe una solicitud de ayuda, debe mostrar la información de ayuda adecuada. Dado que la Windows ayuda proporciona una interfaz de usuario coherente, se recomienda que las aplicaciones usen Windows ayuda en lugar de otros métodos. Para indicar Windows Ayuda para mostrar información de ayuda, una aplicación usa la función [**WinHelp,**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) especificando detalles como la información que se va a mostrar y el formulario de la ventana en la que se va a mostrar. En las secciones siguientes se explica cómo usar **WinHelp** para mostrar información de ayuda.

### <a name="help-files"></a>archivos de ayuda

Para ver la información de ayuda, debe especificar un archivo de ayuda al llamar a la [**función WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) El archivo de ayuda debe tener el Windows de archivo de ayuda (.hlp) y uno o varios temas. Cada tema es una unidad de información distinta, como una descripción conceptual, un conjunto de instrucciones, una imagen, una definición de glosario, y así sucesivamente. Los temas deben identificarse de forma única para que Windows ayuda pueda localizarlos cada vez que se soliciten. Internamente, Windows ayuda usa identificadores de tema para buscar temas, pero las aplicaciones suelen usar identificadores de contexto (valores enteros únicos) para especificar los temas que se mostrarán. El autor del archivo de ayuda debe asignar explícitamente identificadores de contexto a identificadores de tema en la sección MAP del archivo de proyecto utilizado \[ para compilar el archivo de \] ayuda.

Cuando se especifica un archivo de ayuda, pero no se especifica una ruta de acceso, [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) busca el archivo de ayuda en el directorio de ayuda o en un directorio especificado por la variable de entorno PATH. Además, **WinHelp puede** encontrar un archivo de ayuda cuyo nombre aparece en la siguiente ubicación del Registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Help
```

Para aprovechar las ventajas del Registro, debe crear un nombre de valor que tenga el mismo nombre que el archivo de ayuda. El valor asignado a ese nombre debe ser el directorio donde reside el archivo de ayuda.

Si [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) no encuentra el archivo de ayuda especificado, muestra un cuadro de diálogo que permite al usuario especificar la ubicación del archivo de ayuda. Dado **que WinHelp** guarda la información de ubicación en el Registro, no vuelve a solicitar la ubicación del mismo archivo de ayuda.

Para obtener más información sobre cómo crear y compilar un archivo de ayuda, consulte la documentación proporcionada con las herramientas de desarrollo.

### <a name="starting-windows-help"></a>Inicio de Windows Ayuda

En el ejemplo siguiente se usa [**la función WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para iniciar la aplicación Windows ayuda y abrir el archivo de ayuda en su tema Contenido.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_CONTENTS, 0L);
```



En este ejemplo siguiente se abre el archivo de ayuda del usuario, se busca en el archivo el tema asociado a una cadena de palabra clave y, a continuación, se muestra el tema.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_KEY, (DWORD) "finding topics");
```



### <a name="help-topics-dialog-box"></a>Temas de Ayuda (cuadro de diálogo)

Puede mostrar el cuadro **de diálogo Temas** de Ayuda llamando a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con el **comando HELP \_ FINDER.** El **cuadro de diálogo** Temas de Ayuda permite al usuario seleccionar los temas que se mostrarán viendo los títulos de los temas, las palabras clave asociadas a los temas o las palabras y frases que se encuentran en los temas. Las aplicaciones suelen mostrar este cuadro de diálogo cuando el usuario elige un comando, como Temas de Ayuda, en el menú Ayuda. Una aplicación también puede mostrar este cuadro de diálogo si el usuario presiona la tecla cuando ninguna ventana, control o menú específico de la aplicación tiene el foco o está activo.

En el pasado, las aplicaciones han usado los comandos **\_ HELP CONTENTS** y HELP **\_ INDEX** con la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para mostrar el tema Contenido y el índice de palabras clave del archivo de Ayuda. Estos comandos ya no se recomiendan. En su lugar, use **\_ el comando HELP FINDER.**

### <a name="information-topics"></a>Temas de información

Puede mostrar un tema específico llamando a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con el comando HELP CONTEXT y especificando el identificador \_ de contexto para el tema. Las aplicaciones suelen usar el comando HELP CONTEXT en respuesta a las solicitudes de usuario de temas que contienen información conceptual o ayuda de procedimientos en lugar de información sobre \_ un control o menú específicos. En tales casos, el usuario puede continuar explorando el archivo de ayuda en busca de información relacionada antes de volver a la aplicación.

El comando HELP CONTEXT invoca una instancia normal de Windows Ayuda, lo que permite al usuario buscar otros temas \_ en el archivo de ayuda. Normalmente muestra la ventana de Ayuda principal, que incluye una barra de título, un menú del sistema, botones minimizar y maximizar, un menú principal, una barra de navegación opcional, un borde de ajuste de tamaño y un área de cliente. El texto del tema seleccionado aparece en el área de cliente y el usuario puede navegar por el archivo de ayuda mediante vínculos rápidos o botones de navegación en la ventana principal. La instancia normal de Windows ayuda también se puede usar para mostrar ayuda en una o varias ventanas secundarias en lugar de en la ventana principal.

### <a name="pop-up-topics"></a>Temas emergentes

Puede mostrar un tema emergente que contiene información para un control o menú específico llamando a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con el comando HELP WM HELP o \_ HELP \_ \_ CONTEXTMENU. Estos comandos muestran un tema en una ventana emergente cerca del control o menú correspondiente. Para permitir que el usuario vuelva inmediatamente a trabajar en la aplicación, la ventana emergente se destruye en cuanto el usuario presiona una tecla o hace clic en el botón izquierdo del mouse.

Use el comando HELP \_ WM HELP al procesar mensajes WM \_ [**\_ HELP**](wm-help.md) para ventanas de control. Dado que la mayoría de los controles pasan el **mensaje \_ WM HELP** a la función [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) el procedimiento de cuadro de diálogo correspondiente (o procedimiento de ventana principal) procesa este mensaje. En lugar de proporcionar un identificador de contexto específico, el procedimiento del cuadro de diálogo debe pasar una matriz de pares de identificadores de contexto y control a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) junto con el identificador de control especificado en el **miembro hItemHandle** de la estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) pasada con el **mensaje HELP \_ de WM.** La función determina el identificador del control para el que se generó el mensaje **\_ WM HELP** y usa el identificador de contexto correspondiente para mostrar el tema adecuado.

Use el comando HELP \_ CONTEXTMENU al procesar [**mensajes DE WM \_ CONTEXTMENU.**](../menurc/wm-contextmenu.md) Dado que la mayoría de los controles pasan el **mensaje \_ CONTEXTMENU de WM** a la función [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) el procedimiento de cuadro de diálogo correspondiente (o procedimiento de ventana principal) procesa este mensaje. El procedimiento especifica una matriz de pares de identificadores de control e contexto; también especifica el identificador en el parámetro *wParam* al llamar a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para que la función pueda elegir el identificador de contexto adecuado de la matriz y mostrar el tema adecuado. A diferencia del comando HELP WM HELP, HELP CONTEXTMENU muestra primero un comando \_ \_ \_ **What's This?** en un menú. Si el usuario elige el comando, **WinHelp** muestra el tema. De lo contrario, se cancela la solicitud.

También puede mostrar temas emergentes mediante el comando HELP CONTEXTPOPUP y especificando un \_ identificador de contexto del tema. Este comando es similar al comando HELP CONTEXT, pero invoca la instancia emergente de Windows Help usada por HELP WM HELP y \_ \_ HELP \_ \_ CONTEXTMENU. Las aplicaciones pueden usar este comando en respuesta a los mensajes [**\_ DE AYUDA DE WM**](wm-help.md) para mostrar ayuda para menús y ventanas que no son controles en un cuadro de diálogo. Para usar este comando de forma más eficaz, la aplicación debe asignar identificadores de contexto a estos menús y ventanas.

Puede asignar un identificador de contexto a cualquier ventana o menú de la aplicación. Cuando se [**genera un mensaje WM \_ HELP,**](wm-help.md) el sistema incluye el identificador de contexto en la estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que se pasa a la ventana primaria en el **mensaje DE AYUDA \_ DE WM.** A continuación, la ventana primaria puede pasar el identificador de contexto [**a WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para mostrar el tema de ayuda solicitado.

Use la función [**SetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid) para asignar un identificador de contexto a una ventana o control y la función [**SetMenuContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid) para asignar un identificador de contexto a un menú. Puede recuperar el identificador de contexto de una ventana o menú mediante la [**función GetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid) [**o GetMenuContextHelpId.**](/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid)

### <a name="keyword-searches"></a>Búsquedas de palabras clave

Puede permitir que el usuario busque y vea temas mediante la asignación de palabras clave a temas del archivo de ayuda. Una palabra clave es simplemente una cadena asociada a uno o varios temas. Windows La Ayuda recopila todas las palabras clave de un archivo de ayuda, las coloca en una tabla y las muestra en la lista Índice del cuadro de diálogo **Temas** de Ayuda. Cuando el usuario selecciona una palabra clave, Windows Ayuda muestra el tema de ayuda asociado o, si hay más de un tema asociado a la palabra clave , muestra una lista de temas entre los que el usuario puede elegir.

En una aplicación, puede usar el comando HELP KEY, HELP PARTIALKEY o HELP MULTIKEY con la función WinHelp para buscar y mostrar temas de ayuda basados en palabras clave enteras o \_ \_ \_ parciales. [](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Especifique el comando, la cadena de palabra clave, el archivo de ayuda y el identificador de la ventana de propietario. En todos los casos, si se encuentra una sola coincidencia, **WinHelp** muestra el tema correspondiente. Si se encuentra más de una coincidencia, la función muestra el cuadro de diálogo Temas encontrados y el usuario puede elegir qué tema ver. Si no se encuentra ninguna coincidencia, **WinHelp** muestra la lista Índice (para HELP KEY y HELP PARTIALKEY) o muestra un mensaje de \_ error \_ (para HELP \_ MULTIKEY).

La aplicación puede buscar varias palabras clave en una sola llamada a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) separando las palabras clave con punto y coma. (No se admite la búsqueda de varias palabras clave para los archivos de ayuda creados Windows versión 3. *x*) También puede buscar palabras clave en varios archivos de ayuda si el archivo de ayuda especificado tiene un archivo contents(.cnt) que contiene comandos :Index o :Link. Con el comando HELP KEY, WinHelp busca palabras clave en todos los \_ archivos especificados por estos comandos.  Con los comandos HELP MULTIKEY y HELP PARTIALKEY, la función busca en todos los archivos excepto los \_ \_ especificados por los comandos :Link.

De forma predeterminada, Windows ayuda reconoce solo la tabla de palabras clave identificada por el carácter de nota al pie K en el archivo de origen de ayuda. Puede dirigir Windows ayuda para crear tablas de palabras clave adicionales agregando un carácter de nota al pie distinto de K, con la definición de palabra clave, en el archivo de origen de ayuda. (El carácter de nota al pie A, sin embargo, está reservado). Debe definir las tablas de palabras clave adicionales mediante instrucciones MULTIKEY en la sección OPTIONS del archivo de proyecto \[ al compilar el archivo de \] ayuda.

Una aplicación puede usar el comando HELP SETINDEX con la función WinHelp para dirigir Windows Ayuda para mostrar una tabla de palabras clave que no sea K en su \_ lista de índices. [](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Para dirigir Windows ayuda para buscar una palabra clave en una tabla de palabras clave alternativas, una aplicación puede usar el comando HELP \_ MULTIKEY. Especifique la palabra clave y la tabla de palabras clave en una [**estructura MULTIKEYHELP,**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) que se pasa a **WinHelp.**

Cuando [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) muestra un tema, lo muestra en la ventana especificada por la nota al pie ">" del tema, en la ventana especificada por el comando :Base en el archivo de contenido o en la ventana principal. Si la ventana principal ya está abierta en otro archivo de ayuda al llamar a **WinHelp,** la función oculta la ventana principal durante la búsqueda. En este caso, al cancelar los cuadros de diálogo **Temas** encontrados y **Temas** de Ayuda se cierra la ventana principal.

### <a name="secondary-help-windows"></a>Ventanas de ayuda secundarias

La ventana principal de la aplicación Windows ayuda se denomina ventana principal. Windows La Ayuda también puede mostrar temas de ayuda en una ventana secundaria. A diferencia de la ventana de Ayuda principal, una ventana secundaria no contiene una barra de menús. Puede incluir una barra de navegación en una ventana secundaria y puede agregar botones a la barra. También puede optar por que la ayuda Windows ajustar automáticamente el alto de la ventana secundaria para dar cabida al tema.

Debe definir ventanas secundarias en la sección WINDOWS del archivo de proyecto de ayuda, proporcionando el nombre y, opcionalmente, el tamaño inicial y la \[ \] posición de cada ventana. Puede dirigir a la aplicación Windows Ayuda para que muestre un tema en una ventana secundaria anexando un corchete angular (>) y el nombre que ha definido para la ventana secundaria al nombre del archivo de ayuda. A continuación, la cadena resultante se pasa a la [**función WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)

Una aplicación puede cambiar el tamaño y la posición de una ventana principal o secundaria especificando la dirección de una estructura [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) y el comando HELP SETWINPOS en una llamada \_ a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). **HELPWININFO especifica** el nombre de la ventana y su nuevo tamaño y posición.

### <a name="training-card-help"></a>Ayuda de tarjeta de entrenamiento

Con la ayuda de la tarjeta de entrenamiento, una aplicación puede mostrar una secuencia de instrucciones para guiar al usuario a través de los pasos de una tarea. Normalmente, una tarjeta de entrenamiento consta de texto que explica un paso y botones determinados asociados a las macros de TCard, que permiten al usuario decir a la aplicación qué hacer a continuación. Las tarjetas de entrenamiento solo se pueden mostrar en ventanas secundarias y no deben contener vínculos de acceso rápido a otros temas del archivo de ayuda.

Una aplicación inicia la instancia de tarjeta de entrenamiento de Windows Help llamando a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) y especificando el comando HELP TCARD en combinación con otro comando, como \_ HELP \_ CONTEXT. Posteriormente, cuando el usuario hace clic en un botón de la tarjeta de entrenamiento, hace clic en un punto de acceso rápido asignado a la macro TCard o cierra la tarjeta de entrenamiento, Windows Ayuda notifica a la aplicación enviándole un [**mensaje \_ WM TCARD.**](wm-tcard.md) El *parámetro wParam* identifica el botón o la acción del usuario, y el parámetro *lParam* contiene datos adicionales, cuyo significado depende del valor *de wParam*.

### <a name="canceling-help"></a>Cancelación de ayuda

Windows La ayuda requiere que una aplicación cancele explícitamente la ayuda para que pueda liberar los recursos usados para realizar un seguimiento de la aplicación y sus archivos de ayuda. La aplicación puede hacerlo en cualquier momento llamando a la [**función WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) y especificando el comando HELP \_ QUIT. Tenga en cuenta que esto no es cierto para la instancia emergente de Windows Ayuda. Una aplicación no debe intentar cerrar una instancia emergente.

Si una aplicación ha realizado alguna llamada a [**WinHelp,**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)debe cancelar la ayuda antes de cerrar su ventana principal (por ejemplo, en respuesta al mensaje WM DESTROY en el procedimiento de \_ la ventana principal). Una aplicación debe llamar a **WinHelp solo** una vez para cancelar la ayuda, independientemente de cuántos archivos de ayuda haya abierto. Windows La ayuda permanece en ejecución hasta que todas las aplicaciones o archivos DLL han cancelado la ayuda.

Para cerrar la instancia de tarjeta de entrenamiento de Windows Ayuda, debe especificar los comandos HELP TCARD y HELP QUIT al \_ \_ llamar a [**WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) No es necesario que una aplicación cancele la instancia de la tarjeta de entrenamiento Windows ayuda si el usuario la cancela primero. Windows La Ayuda notifica a una aplicación cuando el usuario cancela la instancia de la tarjeta de entrenamiento mediante el envío del [**mensaje \_ WM TCARD**](wm-tcard.md) con el parámetro *wParam* establecido en IDCLOSE.

## <a name="using-help"></a>Uso de la Ayuda

En esta sección se muestra cómo proporcionar ayuda contextual para un cuadro de diálogo y cómo establecer la apariencia de una ventana de Ayuda secundaria.

-   [Proporcionar ayuda en un cuadro de diálogo](#providing-help-in-a-dialog-box)
-   [Establecer la apariencia de una ventana de Ayuda secundaria](#setting-the-appearance-of-a-secondary-help-window)

### <a name="providing-help-in-a-dialog-box"></a>Proporcionar ayuda en un cuadro de diálogo

Para proporcionar ayuda contextual en un cuadro de diálogo, debe crear una matriz que consta de pares de **valores DWORD.** El primer valor de cada par es el identificador de un control en el cuadro de diálogo y el segundo es el identificador de contexto del tema de ayuda para el control. La matriz debe contener un par de identificadores para cada control del cuadro de diálogo.

El procedimiento del cuadro de diálogo debe procesar los [**mensajes WM \_ HELP**](wm-help.md) y [**WM \_ CONTEXTMENU.**](../menurc/wm-contextmenu.md) El procedimiento del cuadro de diálogo recibe **WM \_ HELP** cuando el usuario presiona la tecla **y WM \_ CONTEXTMENU** cuando el usuario hace clic en el botón derecho del mouse.

El *parámetro lParam* de [**WM \_ HELP**](wm-help.md) contiene la dirección de una [**estructura HELPINFO.**](/windows/win32/api/winuser/ns-winuser-helpinfo) El **miembro hItemHandle** de esta estructura identifica el control para el que el usuario ha solicitado ayuda. Debe pasar este identificador a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) junto con el comando HELP WM HELP, el nombre del archivo de ayuda y un puntero a la matriz \_ de \_ identificadores. La **función WinHelp** busca en la matriz el identificador de control del control especificado y, a continuación, recupera el identificador de contexto de ayuda correspondiente. A continuación, la función pasa el identificador de contexto de ayuda a Windows Ayuda, que busca el tema correspondiente y lo muestra en una ventana emergente. Si el control tiene un identificador de -1, el sistema busca el siguiente control que es una detenerse de tabulación y, a continuación, usa su identificador para buscar el identificador de contexto de ayuda. Por esta razón, es importante colocar texto estático antes de los controles en un archivo de recursos.

Al llamar a [**la función WinHelp,**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) el procesamiento [**de WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) es similar al procesamiento de [**WM \_ HELP**](wm-help.md) con estas dos excepciones:

-   Se pasa el *parámetro wParam* de [**WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md), que es el identificador del control que envió el mensaje.
-   Especifique el comando **HELP \_ CONTEXTMENU en** lugar de HELP WM **\_ \_ HELP**.

El **comando \_ HELP CONTEXTMENU** hace que Windows ayuda muestre un menú antes de mostrar el tema de ayuda. El menú está definido por el sistema. Permite al usuario mostrar ayuda para el control o mostrar el cuadro **de diálogo Temas** de Ayuda.

En el ejemplo siguiente se muestra cómo implementar ayuda contextual en un cuadro de diálogo.


```
LRESULT CALLBACK EditDlgProc(HWND hwndDlg, UINT uMsg, 
                             WPARAM wParam, LPARAM lParam) 
{ 
    // Create an array of control identifiers and context identifiers. 
    static DWORD aIds[ ] = 
    { 
        ID_SAVE,   IDH_SAVE, 
        ID_DELETE, IDH_DELETE, 
        ID_COPY,   IDH_COPY, 
        ID_PASTE,  IDH_PASTE, 
        0,0 
    }; 

    switch (uMsg) 
    { 
        case WM_HELP: 
            WinHelp(((LPHELPINFO)lParam)->hItemHandle, "helpfile.hlp", 
                    HELP_WM_HELP, (DWORD)(LPSTR)aIds); 
            break; 

        case WM_CONTEXTMENU: 
            WinHelp((HWND)wParam, "helpfile.hlp", HELP_CONTEXTMENU, 
                    (DWORD)(LPVOID)aIds); 
            break; 
        
        // Process other messages here. 
    } 
    return FALSE; 
}
```



### <a name="setting-the-appearance-of-a-secondary-help-window"></a>Establecer la apariencia de una ventana de Ayuda secundaria

Una aplicación puede establecer el tamaño, la posición y el estado de una ventana de ayuda secundaria pasando el comando HELP SETWINPOS y la dirección de una estructura \_ [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) a la [**función WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Los miembros de **HELPWININFO** especifican el nombre de la ventana que se va a cambiar y el nuevo tamaño, posición y estado de la ventana.

En el ejemplo siguiente se establece la apariencia de una ventana secundaria denominada "wnd \_ menu". El nombre debe definirse en la sección \[ WINDOWS del archivo de proyecto de \] ayuda.


```
BOOL DoWindowSize(VOID) 
{ 
    HANDLE hhwi; 
    LPHELPWININFO lphwi; 
    WORD wSize; 
    char *szWndName = "wnd_menu"; 
    size_t NameLength;      // Does not include the terminating null character
    HRESULT hr
    BOOL retval;

    hr = StringCbLengthA(szWndName, STRSAFE_MAX_CCH, &NameLength);
    
    if (SUCCEEDED(hr))
    {
        // Add 1 to account for the name string's terminating null character.
        NameLength++;
        
        // The HELPWININFO structure contains a minimal TCHAR array of size [2] 
        // that is used for the window name. Since sizeof(HELPWININFO) 
        // includes those two TCHARS, they must be subtracted from the 
        // total when adding the actual string length to calculate the  
        // size of the structure. 
        wSize = sizeof(HELPWININFO) - 2 + NameLength; 
    }
    else
        // Something's amiss with the string.
        return FALSE;
        
    hhwi  = GlobalAlloc(GHND, wSize); 
    lphwi = (LPHELPWININFO)GlobalLock(hhwi); 

    lphwi->wStructSize = wSize; 
    lphwi->x    = 256;      // horizontal position 
    lphwi->y    = 256;      // vertical position 
    lphwi->dx   = 767;      // width 
    lphwi->dy   = 512;      // height 
    lphwi->wMax = SW_SHOW;  // show the window 
    
    // secondary window
    hr = StringCbCopyA(lphwi->rgchMember, sizeof(lphwi->rgchMember), szWndName);
    
    if (SUCCEEDED(hr))
    {
        WinHelp(hwnd, "myhelp.hlp", HELP_SETWINPOS, (DWORD)lphwi); 
     
        GlobalUnlock(hhwi); 
        GlobalFree(hhwi); 

        return TRUE; 
    }
    else
        // There was a problem copying the window name.
        return FALSE;
}
```



 

 
