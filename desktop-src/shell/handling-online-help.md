---
description: La ayuda en línea puede estar en una gran variedad de formas, desde información conceptual detallada hasta definiciones rápidas. En este tema se incluyen las siguientes secciones.
title: Controlar la ayuda en línea
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2a3f6034-6ba6-4204-a2e1-59995fbf40fe
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f1c125df135068c2eee37cb33a8a9d2b281b1f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997716"
---
# <a name="handling-online-help"></a>Controlar la ayuda en línea

La ayuda en línea puede estar en una gran variedad de formas, desde información conceptual detallada hasta definiciones rápidas. En este tema se incluyen las siguientes secciones.

-   [Acerca de la ayuda](#about-help)
    -   [Solicitudes de ayuda](#help-requests)
    -   [Pantalla de ayuda y ayuda de Windows](#help-display-and-windows-help)
-   [Uso de la ayuda](#using-help)
    -   [Proporcionar ayuda en un cuadro de diálogo](#providing-help-in-a-dialog-box)
    -   [Establecer la apariencia de una ventana de ayuda secundaria](#setting-the-appearance-of-a-secondary-help-window)

## <a name="about-help"></a>Acerca de la ayuda

Un elemento importante de una aplicación fácil de leer está disponible en la ayuda en pantalla. Windows proporciona funciones y mensajes que, cuando se usan junto con la aplicación de ayuda de Windows, facilitan la implementación de la ayuda en línea en la aplicación. En esta información general se describen los elementos de Windows que admiten la ayuda en pantalla. Describe cómo usar estos elementos para proporcionar a los usuarios un medio de solicitar ayuda y explica cómo usar la aplicación de ayuda de Windows para mostrar la ayuda.

### <a name="help-requests"></a>Solicitudes de ayuda

La mayoría de las aplicaciones basadas en Windows proporcionan información de ayuda en línea en una gran variedad de formas, desde ayuda conceptual que explica el propósito de las características de una aplicación a la ayuda emergente que proporciona definiciones rápidas de elementos individuales en la interfaz de usuario de la aplicación. Las funciones y los mensajes se utilizan para proporcionar a los usuarios diversas formas de solicitar acceso a esta información. En las secciones siguientes se describen estas solicitudes de ayuda.

### <a name="help-menu"></a>Menú Ayuda

La mayoría de las aplicaciones proporcionan acceso de usuario a la información de ayuda mediante la inclusión de un menú **ayuda** en la ventana principal. Cuando el usuario selecciona un elemento de un menú **ayuda** , el procedimiento de ventana correspondiente recibe un mensaje de [**\_ comando de WM**](../menurc/wm-command.md) que identifica el elemento seleccionado. La aplicación responde mostrando la información de ayuda adecuada, como una lista de temas de ayuda, un índice o una introducción a la aplicación.

### <a name="help-from-the-keyboard"></a>Ayuda del teclado

Windows proporciona acceso de usuario a la información de ayuda del teclado mediante la notificación a la aplicación cada vez que el usuario presiona la tecla F1. El sistema envía un mensaje de [**\_ ayuda de WM**](wm-help.md) a la ventana que tenía el foco de teclado cuando el usuario presionó la tecla. Si la ventana es una ventana secundaria (por ejemplo, un control en un cuadro de diálogo), la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pasa el mensaje a la ventana primaria. Si un menú está activo cuando se presiona F1, el sistema envía el mensaje a la ventana asociada con el menú. La aplicación responde mostrando información de ayuda asociada a la ventana, el control o el menú que tiene el foco o está activo. Por ejemplo, si el usuario selecciona un control en un cuadro de diálogo y presiona F1, la aplicación muestra información de ayuda para ese control.

El parámetro *lParam* de [**la \_ ayuda de WM**](wm-help.md) es un puntero a una estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contiene información detallada sobre el elemento para el que se solicita ayuda. Utilice esta información para determinar el tema de ayuda que se va a mostrar. La estructura **HELPINFO** también incluye las coordenadas del cursor del mouse en el momento en que el usuario presionó la tecla. Puede usar esta información para proporcionar ayuda en función de la ubicación del cursor del mouse.

### <a name="help-from-the-mouse"></a>Ayuda del mouse

Windows proporciona al usuario acceso a la información de ayuda desde el mouse mediante una notificación a la aplicación cada vez que el usuario hace clic con el botón secundario del mouse o hace clic en una ventana, control o menú después de hacer clic en el botón pregunta (?). La aplicación responde mostrando información de ayuda asociada a la ventana, control o menú dados.

El sistema envía un mensaje de [**\_ CONTEXTMENU de WM**](../menurc/wm-contextmenu.md) cuando el usuario hace clic con el botón secundario del mouse. La ventana en la que se hizo clic recibe el mensaje. Si la ventana es una ventana secundaria, como un control, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pasa el mensaje a la ventana primaria. El mensaje de **\_ CONTEXTMENU de WM** especifica las coordenadas del cursor del mouse. La coordenada x está en la palabra de orden inferior del parámetro *lParam* y la coordenada y está en la palabra de orden superior. Si el usuario hizo clic en un control, el parámetro *wParam* es el identificador del control que recibió el clic.

El sistema envía un mensaje de [**\_ ayuda de WM**](wm-help.md) cuando el usuario hace clic en un elemento de una ventana después de hacer clic en el botón pregunta (?) que aparece en la barra de título de la ventana. Puede Agregar un botón de pregunta a una barra de título especificando el estilo **WS \_ ex \_ CONTEXTHELP** en la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) al crear la ventana. El parámetro *lParam* de **la \_ ayuda de WM** es un puntero a una estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que contiene información detallada sobre el elemento para el que se solicita ayuda, incluidas las coordenadas del cursor del mouse en el momento en que el usuario hizo clic con el botón del mouse.

Se recomienda usar el botón de pregunta solo en cuadros de diálogo. En el pasado, las aplicaciones proporcionaban acceso de usuario a la información de ayuda sobre un cuadro de diálogo proporcionando un botón **ayuda** en el cuadro de diálogo. Este método ya no se recomienda. En su lugar, use el botón pregunta.

### <a name="help-display-and-windows-help"></a>Pantalla de ayuda y ayuda de Windows

Una vez que una aplicación recibe una solicitud de ayuda, debe mostrar la información de ayuda adecuada. Dado que la aplicación de ayuda de Windows proporciona una interfaz de usuario coherente, se recomienda que las aplicaciones usen la ayuda de Windows en lugar de otros métodos. Para indicar a la ayuda de Windows que muestre información de ayuda, una aplicación utiliza la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) y especifica detalles como la información que se va a mostrar y el formulario de la ventana en la que se va a mostrar. En las secciones siguientes se explica cómo usar **WinHelp** para mostrar información de ayuda.

### <a name="help-files"></a>archivos de ayuda

Para ver la información de ayuda, debe especificar un archivo de ayuda al llamar a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) . El archivo de ayuda debe tener el formato de archivo de ayuda de Windows (. hlp) y uno o más temas. Cada tema es una unidad distinta de información, como una descripción conceptual, un conjunto de instrucciones, una imagen, una definición de Glosario, etc. Los temas se deben identificar de forma exclusiva para que la ayuda de Windows pueda encontrarlos cada vez que se soliciten. Internamente, la ayuda de Windows utiliza identificadores de tema para buscar temas, pero las aplicaciones suelen usar identificadores de contexto (valores enteros únicos) para especificar los temas que se van a mostrar. El autor del archivo de ayuda debe asignar explícitamente los identificadores de contexto a los identificadores de tema en la \[ \] sección Map del archivo de proyecto que se usa para generar el archivo de ayuda.

Cuando se especifica un archivo de ayuda pero no se especifica una ruta de acceso, [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) busca el archivo de ayuda en el directorio de ayuda o en el directorio especificado por la variable de entorno PATH. Además, **WinHelp** puede encontrar un archivo de ayuda cuyo nombre se muestra en la siguiente ubicación del registro:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Help
```

Para aprovechar las ventajas del registro, debe crear un nombre de valor que tenga el mismo nombre que el archivo de ayuda. El valor asignado a ese nombre debe ser el directorio donde reside el archivo de ayuda.

Si [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) no encuentra el archivo de ayuda especificado, muestra un cuadro de diálogo que permite al usuario especificar la ubicación del archivo de ayuda. Dado que **WinHelp** guarda la información de ubicación en el registro, no vuelve a preguntar la ubicación del mismo archivo de ayuda.

Para obtener más información sobre cómo crear y compilar un archivo de ayuda, consulte la documentación que se proporciona con las herramientas de desarrollo.

### <a name="starting-windows-help"></a>Iniciar la ayuda de Windows

En el ejemplo siguiente se usa la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para iniciar la aplicación de ayuda de Windows y abrir el archivo de ayuda en su tema de contenido.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_CONTENTS, 0L);
```



En el siguiente ejemplo se abre el archivo de ayuda del usuario, se busca en el archivo el tema asociado a una cadena de palabra clave y, a continuación, se muestra el tema.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_KEY, (DWORD) "finding topics");
```



### <a name="help-topics-dialog-box"></a>Temas de ayuda (cuadro de diálogo)

Puede mostrar el cuadro de diálogo **temas de ayuda** mediante una llamada a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con el comando **\_ Finder** de la ayuda. El cuadro de diálogo **temas de ayuda** permite que el usuario seleccione los temas que se muestran al ver los títulos de los temas, las palabras clave asociadas a los temas o las palabras y frases que se encuentran en los temas. Normalmente, las aplicaciones muestran este cuadro de diálogo cuando el usuario elige un comando, como los temas de ayuda, en el menú ayuda. Una aplicación también puede mostrar este cuadro de diálogo si el usuario presiona la tecla cuando no hay ninguna ventana, control o menú específico en la aplicación que tenga el foco o esté activo.

En el pasado, las aplicaciones usaban los comandos **\_ contenido** de la ayuda y **\_ Índice** de la ayuda con la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para mostrar el tema contenido y el índice de palabras clave del archivo de ayuda. Estos comandos ya no se recomiendan. En su lugar, use el comando **\_ Finder** de la ayuda.

### <a name="information-topics"></a>Temas de información

Puede mostrar un tema concreto llamando a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con el comando de \_ contexto de ayuda y especificando el identificador de contexto para el tema. Normalmente, las aplicaciones usan el \_ comando de contexto de ayuda en respuesta a las solicitudes de los usuarios para temas que contienen información conceptual o ayuda de procedimientos, en lugar de información sobre un control o menú específico. En tales casos, el usuario puede continuar explorando el archivo de ayuda buscando información relacionada antes de volver a la aplicación.

El \_ comando de contexto de ayuda invoca una instancia normal de la ayuda de Windows, lo que permite al usuario buscar otros temas en el archivo de ayuda. Normalmente muestra la ventana principal de ayuda, que incluye una barra de título, un menú del sistema, botones minimizar y maximizar, un menú principal, una barra de navegación opcional, un borde de ajuste de tamaño y un área cliente. El texto del tema seleccionado aparece en el área cliente y el usuario puede desplazarse por el archivo de ayuda mediante el uso de vínculos activos o botones de navegación en la ventana principal. La instancia normal de la ayuda de Windows también se puede usar para mostrar la ayuda en una o varias ventanas secundarias en lugar de en la ventana principal.

### <a name="pop-up-topics"></a>Temas emergentes

Puede mostrar un tema emergente que contenga información de un control o un menú concretos llamando a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con el comando Help \_ WM \_ Help o Help \_ CONTEXTMENU. Estos comandos muestran un tema en una ventana emergente cerca del control o menú correspondiente. Para permitir que el usuario vuelva inmediatamente a trabajar en la aplicación, la ventana emergente se destruye en cuanto el usuario presiona una tecla o hace clic en el botón primario del mouse.

El \_ comando help WM Help se usa \_ al procesar los mensajes de [**\_ ayuda de WM**](wm-help.md) para las ventanas de control. Dado que la mayoría de los controles pasan el mensaje de **\_ ayuda de WM** a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , el procedimiento de cuadro de diálogo correspondiente (o el procedimiento de ventana principal) procesa este mensaje. En lugar de proporcionar un identificador de contexto específico, el procedimiento del cuadro de diálogo debe pasar una matriz de pares de identificador de control y de contexto a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) junto con el identificador de control especificado en el miembro **hItemHandle** de la estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) pasada con el mensaje de **\_ ayuda de WM** . La función determina el identificador del control para el que se generó el mensaje de **\_ ayuda de WM** y usa el identificador de contexto correspondiente para mostrar el tema correspondiente.

El comando HELP ContextMenu se usa \_ al procesar mensajes de [**WM \_ ContextMenu**](../menurc/wm-contextmenu.md) . Dado que la mayoría de los controles pasan el mensaje de **\_ CONTEXTMENU de WM** a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , el procedimiento de cuadro de diálogo correspondiente (o el procedimiento de ventana principal) procesa este mensaje. El procedimiento especifica una matriz de pares de identificador de control y de contexto; también especifica el identificador en el parámetro *wParam* al llamar a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para que la función pueda seleccionar el identificador de contexto adecuado de la matriz y mostrar el tema correspondiente. A diferencia del comando ayuda de \_ WM \_ ayuda, la ayuda \_ de CONTEXTMENU primero muestra el comando **¿Qué es esto?** en un menú. Si el usuario elige el comando, **WinHelp** muestra el tema. De lo contrario, se cancela la solicitud.

También puede mostrar los temas emergentes mediante el \_ comando help CONTEXTPOPUP y especificando un identificador de contexto del tema. Este comando es similar al comando de \_ contexto de ayuda, pero invoca la instancia emergente de la ayuda de Windows que usa Help \_ WM \_ Help y Help \_ CONTEXTMENU. Las aplicaciones pueden usar este comando en respuesta a los mensajes de [**\_ ayuda de WM**](wm-help.md) para mostrar la ayuda de los menús y las ventanas que no son controles en un cuadro de diálogo. Para usar este comando de manera más eficaz, la aplicación debe asignar identificadores de contexto a estos menús y ventanas.

Puede asignar un identificador de contexto a cualquier ventana o menú de la aplicación. Cuando se genera un mensaje de [**\_ ayuda de WM**](wm-help.md) , el sistema incluye el identificador de contexto en la estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) que se pasa a la ventana primaria del mensaje de **\_ ayuda de WM** . La ventana primaria puede pasar el identificador de contexto a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para mostrar el tema de ayuda solicitado.

Utilice la función [**SetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid) para asignar un identificador de contexto a una ventana o un control y la función [**SetMenuContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid) para asignar un identificador de contexto a un menú. Puede recuperar el identificador de contexto de una ventana o menú mediante la función [**GetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid) o [**GetMenuContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid) .

### <a name="keyword-searches"></a>Búsquedas de palabras clave

Puede permitir que el usuario busque y vea los temas asignando palabras clave a los temas del archivo de ayuda. Una palabra clave es simplemente una cadena que está asociada a uno o más temas. La ayuda de Windows recopila todas las palabras clave de un archivo de ayuda, las coloca en una tabla y las muestra en la lista índice del cuadro de diálogo **temas de ayuda** . Cuando el usuario selecciona una palabra clave, la ayuda de Windows muestra el tema de ayuda asociado o, si hay más de un tema asociado a la palabra clave, muestra una lista de temas entre los que el usuario puede elegir.

En una aplicación, puede usar los \_ comandos tecla de ayuda, \_ PARTIALKEY de ayuda o \_ relaciones de ayuda con la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para buscar y Mostrar temas de ayuda basados en palabras clave completas o parciales. Especifique el comando, la cadena de palabra clave, el archivo de ayuda y el identificador de la ventana propietaria. En todos los casos, si se encuentra una sola coincidencia, **WinHelp** muestra el tema correspondiente. Si se encuentra más de una coincidencia, la función muestra el cuadro de diálogo temas encontrados y el usuario puede elegir qué tema desea ver. Si no se encuentra ninguna coincidencia, **WinHelp** muestra la lista de índices (para la clave de ayuda \_ y la ayuda \_ PARTIALKEY) o muestra un mensaje de error (para ayuda \_ relaciones).

La aplicación puede buscar varias palabras clave en una única llamada a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) separando las palabras clave con punto y coma. (No se admite la búsqueda de varias palabras clave para los archivos de ayuda creados para Windows versión 3. *x*) también puede buscar palabras clave en varios archivos de ayuda si el archivo de ayuda que se especifica tiene un archivo de contenido (. CNT) que contiene los comandos: index o: Link. Con el \_ comando tecla de ayuda, **WinHelp** busca palabras clave en todos los archivos especificados por estos comandos. Con los \_ comandos Help relaciones y Help \_ PARTIALKEY, la función busca en todos los archivos excepto en los especificados por: Link Commands.

De forma predeterminada, la ayuda de Windows solo reconoce la tabla de palabras clave identificada por el carácter de nota al pie K en el archivo de código fuente de la ayuda. Puede dirigir la ayuda de Windows para crear tablas de palabras clave adicionales agregando un carácter de nota al pie que no sea K, con la definición de palabra clave, en el archivo de código fuente de la ayuda. (Sin embargo, el carácter de NOTA A pie A, está reservado). Debe definir las tablas de palabras clave adicionales mediante instrucciones relaciones en la \[ \] sección de opciones del archivo de proyecto al compilar el archivo de ayuda.

Una aplicación puede usar el \_ comando help SETINDEX con la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) para indicar a la ayuda de Windows que muestre una tabla de palabras clave que no sea K en su lista de índices. Para indicar a la ayuda de Windows que busque una palabra clave en una tabla de palabras clave alternativa, una aplicación puede usar el \_ comando help relaciones. La palabra clave y la tabla de palabras clave se especifican en una estructura [**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) , que se pasa a **WinHelp**.

Cuando [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) muestra un tema, lo muestra en la ventana especificada en la nota al pie ">" del tema, en la ventana especificada por el comando: base del archivo de contenido o en la ventana principal. Si la ventana principal ya está abierta a un archivo de ayuda diferente cuando se llama a **WinHelp**, la función oculta la ventana principal durante la búsqueda. En este caso, la cancelación de los cuadros de diálogo **temas encontrados** y **temas de ayuda** cierra la ventana principal.

### <a name="secondary-help-windows"></a>Ventanas de ayuda secundarias

La ventana principal de la aplicación de ayuda de Windows se denomina ventana principal. La ayuda de Windows también puede mostrar temas de ayuda en una ventana secundaria. A diferencia de la ventana de ayuda principal, una ventana secundaria no contiene una barra de menús. Puede incluir una barra de navegación en una ventana secundaria, y puede agregar botones a la barra. También puede hacer que la ayuda de Windows ajuste automáticamente el alto de la ventana secundaria para dar cabida al tema.

Debe definir las ventanas secundarias en \[ la \] sección de Windows del archivo de proyecto de ayuda, proporcionando el nombre y, opcionalmente, el tamaño y la posición iniciales de cada ventana. Puede indicar a la aplicación de ayuda de Windows que muestre un tema en una ventana secundaria anexando un corchete angular (>) y el nombre que haya definido para la ventana secundaria al nombre del archivo de ayuda. A continuación, la cadena resultante se pasa a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .

Una aplicación puede cambiar el tamaño y la posición de una ventana principal o secundaria especificando la dirección de una estructura [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) y el \_ comando help SETWINPOS en una llamada a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). **HELPWININFO** especifica el nombre de la ventana y su nuevo tamaño y posición.

### <a name="training-card-help"></a>Ayuda de la tarjeta de aprendizaje

Con la ayuda de la tarjeta de entrenamiento, una aplicación puede mostrar una secuencia de instrucciones para guiar al usuario a través de los pasos de una tarea. Normalmente, una tarjeta de entrenamiento consta de texto que explica un paso determinado y botones que están asociados a macros TCard, que permiten al usuario indicar a la aplicación qué hacer a continuación. Las tarjetas de entrenamiento solo se pueden mostrar en ventanas secundarias y no deben contener vínculos activos a otros temas del archivo de ayuda.

Una aplicación inicia la instancia de la tarjeta de entrenamiento de la ayuda de Windows mediante una llamada a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) y la especificación del \_ comando help TCARD en combinación con otro comando, como el contexto de ayuda \_ . Posteriormente, cuando el usuario hace clic en un botón de la tarjeta de entrenamiento, hace clic en una zona activa asignada a la macro TCard o cierra la tarjeta de entrenamiento, la ayuda de Windows notifica a la aplicación mediante el envío de un mensaje de [**WM \_ TCard**](wm-tcard.md) . El parámetro *wParam* identifica el botón o la acción del usuario, y el parámetro *lParam* contiene datos adicionales, cuyo significado depende del valor de *wParam*.

### <a name="canceling-help"></a>Cancelar la ayuda

La ayuda de Windows requiere que una aplicación cancele la ayuda explícitamente para que pueda liberar los recursos utilizados para realizar un seguimiento de la aplicación y sus archivos de ayuda. La aplicación puede hacerlo en cualquier momento llamando a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) y especificando el comando Help \_ Quit. Tenga en cuenta que esto no es cierto para la instancia emergente de la ayuda de Windows. Una aplicación no debe intentar cerrar una instancia emergente.

Si una aplicación ha realizado llamadas a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), debe cancelar la ayuda antes de cerrar su ventana principal (por ejemplo, en respuesta al \_ mensaje de destrucción de WM en el procedimiento de ventana principal). Una aplicación debe llamar solo una vez a **WinHelp** para cancelar la ayuda, independientemente del número de archivos de ayuda que haya abierto. La ayuda de Windows permanece en ejecución hasta que todas las aplicaciones o archivos dll tienen la ayuda cancelada.

Para cerrar la instancia de la tarjeta de entrenamiento de la ayuda de Windows, debe especificar los \_ comandos Help TCARD y Help \_ Quit al llamar a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). Una aplicación no necesita cancelar la instancia de la tarjeta de entrenamiento de la ayuda de Windows si el usuario la cancela primero. La ayuda de Windows notifica a una aplicación cuando el usuario cancela la instancia de la tarjeta de entrenamiento enviando el mensaje de [**WM \_ TCARD**](wm-tcard.md) con el parámetro *wParam* establecido en IDCLOSE.

## <a name="using-help"></a>Uso de la ayuda

En esta sección se muestra cómo proporcionar ayuda contextual para un cuadro de diálogo y cómo establecer la apariencia de una ventana de ayuda secundaria.

-   [Proporcionar ayuda en un cuadro de diálogo](#providing-help-in-a-dialog-box)
-   [Establecer la apariencia de una ventana de ayuda secundaria](#setting-the-appearance-of-a-secondary-help-window)

### <a name="providing-help-in-a-dialog-box"></a>Proporcionar ayuda en un cuadro de diálogo

Para proporcionar ayuda contextual en un cuadro de diálogo, debe crear una matriz formada por pares de valores **DWORD** . El primer valor de cada par es el identificador de un control en el cuadro de diálogo y el segundo es el identificador de contexto del tema de ayuda para el control. La matriz debe contener un par de identificadores para cada control en el cuadro de diálogo.

El procedimiento del cuadro de diálogo debe procesar los mensajes de la [**\_ ayuda de WM**](wm-help.md) y de [**WM \_**](../menurc/wm-contextmenu.md) . El procedimiento de cuadro de diálogo recibe **\_ ayuda de WM** cuando el usuario presiona la tecla y el **\_ CONTEXTMENU de WM** cuando el usuario hace clic con el botón secundario del mouse.

El parámetro *lParam* de [**la \_ ayuda de WM**](wm-help.md) contiene la dirección de una estructura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) . El miembro **hItemHandle** de esta estructura identifica el control para el que el usuario ha solicitado ayuda. Debe pasar este identificador a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) junto con el comando Help \_ WM \_ Help, el nombre del archivo de ayuda y un puntero a la matriz de identificadores. La función **WinHelp** busca en la matriz el identificador de control del control especificado y, a continuación, recupera el identificador del contexto de ayuda correspondiente. A continuación, la función pasa el identificador de contexto de ayuda a la ayuda de Windows, que busca el tema correspondiente y lo muestra en una ventana emergente. Si el control tiene un identificador de-1, el sistema busca el siguiente control que es una tabulación y, a continuación, usa su identificador para buscar el identificador de contexto de ayuda. Por esta razón, es importante colocar el texto estático delante de los controles en un archivo de recursos.

Cuando se llama a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) , el procesamiento de un [**\_ CONTEXTMENU de WM**](../menurc/wm-contextmenu.md) es similar al procesamiento de la [**\_ ayuda de WM**](wm-help.md) con estas dos excepciones:

-   Se pasa el parámetro *wParam* desde el control [**\_ CONTEXTMENU de WM**](../menurc/wm-contextmenu.md), que es el identificador del control que envió el mensaje.
-   Especifique el comando **Help \_ CONTEXTMENU** en lugar de Help de ayuda de **\_ WM \_**.

La **ayuda \_** del comando CONTEXTMENU hace que la ayuda de Windows muestre un menú antes de mostrar el tema de ayuda. El menú está definido por el sistema. Permite al usuario Mostrar la ayuda del control o mostrar el cuadro de diálogo **temas de ayuda** .

En el ejemplo siguiente se muestra cómo implementar la ayuda contextual en un cuadro de diálogo.


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



### <a name="setting-the-appearance-of-a-secondary-help-window"></a>Establecer la apariencia de una ventana de ayuda secundaria

Una aplicación puede establecer el tamaño, la posición y el estado de presentación de una ventana de ayuda secundaria pasando el \_ comando help SETWINPOS y la dirección de una estructura [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) . Los miembros de **HELPWININFO** especifican el nombre de la ventana que se va a cambiar y el nuevo tamaño, la posición y el estado de presentación de la ventana.

En el ejemplo siguiente se establece la apariencia de una ventana secundaria denominada " \_ menú WND". El nombre debe definirse en la \[ \] sección ventanas del archivo de proyecto de ayuda.


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



 

 
