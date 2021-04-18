---
title: Acerca de la entrada de teclado
description: En este tema se describe la entrada del teclado.
ms.assetid: de34727e-e8c7-481d-982d-0e42a02704db
keywords:
- entrada de usuario, entrada de teclado
- capturar datos proporcionados por el usuario, entrada mediante teclado
- entrada mediante teclado
- foco de teclado
- mensajes de pulsación de teclas
- mensajes de caracteres
- pulsaciones de teclas del sistema
- pulsaciones de teclas que no son del sistema
- mensajes de caracteres que no son de sistema
- claves muertas
- mensajes no enviados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ad481bad6756bb374b98a5510bdc26f1cded6a
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104564352"
---
# <a name="about-keyboard-input"></a>Acerca de la entrada de teclado

Las aplicaciones deben aceptar la entrada del usuario del teclado y del mouse. Una aplicación recibe la entrada del teclado en forma de mensajes enviados a sus ventanas.

En esta sección se describen los temas siguientes:

-   [Modelo de entrada de teclado](#keyboard-input-model)
-   [Foco y activación del teclado](#keyboard-focus-and-activation)
-   [Mensajes de pulsación de teclas](#keystroke-messages)
    -   [Pulsaciones de teclas del sistema y no del sistema](#system-and-nonsystem-keystrokes)
    -   [Códigos de clave virtual descritos](#virtual-key-codes-described)
    -   [Marcas de mensajes de pulsación de teclas](#keystroke-message-flags)
-   [Mensajes de caracteres](#character-messages)
    -   [Mensajes de caracteres que no son de sistema](#nonsystem-character-messages)
    -   [Mensajes no enviados](#dead-character-messages)
-   [Estado de la clave](#key-status)
-   [Traducciones de teclas y de caracteres](#keystroke-and-character-translations)
-   [Compatibilidad con las teclas de acceso rápido](#hot-key-support)
-   [Teclas del teclado para la exploración y otras funciones](#keyboard-keys-for-browsing-and-other-functions)
-   [Simular la entrada](#simulating-input)
-   [Idiomas, configuraciones regionales y distribuciones de teclado](#languages-locales-and-keyboard-layouts)

## <a name="keyboard-input-model"></a>Modelo de entrada de teclado

El sistema proporciona compatibilidad de teclado independiente del dispositivo para las aplicaciones mediante la instalación de un controlador de dispositivo de teclado adecuado para el teclado actual. El sistema proporciona compatibilidad de teclado independiente del lenguaje mediante el uso de la distribución de teclado específica del idioma seleccionada actualmente por el usuario o la aplicación. El controlador de dispositivo de teclado recibe los códigos de digitalización del teclado, que se envían a la distribución del teclado, donde se traducen en mensajes y se publican en las ventanas adecuadas de la aplicación.

Asignada a cada tecla de un teclado es un valor único denominado *código de análisis*, un identificador dependiente del dispositivo para la clave en el teclado. Un teclado genera dos códigos de digitalización cuando el usuario escribe una tecla, uno cuando el usuario presiona la tecla y otra cuando el usuario suelta la tecla.

El controlador de dispositivo de teclado interpreta un código de examen y lo convierte (lo asigna) en un *código de tecla virtual*, un valor independiente del dispositivo definido por el sistema que identifica el propósito de una clave. Después de traducir un código de digitalización, la distribución del teclado crea un mensaje que incluye el código de digitalización, el código de tecla virtual y otra información acerca de la pulsación de teclas y, después, coloca el mensaje en la cola de mensajes del sistema. El sistema quita el mensaje de la cola de mensajes del sistema y lo envía a la cola de mensajes del subproceso adecuado. Finalmente, el bucle de mensajes del subproceso quita el mensaje y lo pasa al procedimiento de ventana adecuado para su procesamiento. En la ilustración siguiente se muestra el modelo de entrada de teclado.

![modelo de procesamiento de entrada de teclado](images/csinp-01.png)

## <a name="keyboard-focus-and-activation"></a>Foco y activación del teclado

El sistema envía mensajes de teclado a la cola de mensajes del subproceso en primer plano que creó la ventana con el foco de teclado. El *foco de teclado* es una propiedad temporal de una ventana. El sistema comparte el teclado entre todas las ventanas de la pantalla desplazando el foco del teclado, en la dirección del usuario, de una ventana a otra. La ventana que tiene el foco de teclado recibe (desde la cola de mensajes del subproceso que la creó) todos los mensajes del teclado hasta que el foco cambia a otra ventana.

Un subproceso puede llamar a la función [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) para determinar cuál de sus ventanas (si existe) tiene actualmente el foco de teclado. Un subproceso puede dar el foco de teclado a una de sus ventanas mediante una llamada a la función [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) . Cuando el foco de teclado cambia de una ventana a otra, el sistema envía un mensaje de [**WM \_ KILLFOCUS**](wm-killfocus.md) a la ventana que ha perdido el foco y, a continuación, envía un mensaje de [**\_ SETFOCUS de WM**](wm-setfocus.md) a la ventana que ha obtenido el foco.

El concepto de foco de teclado está relacionado con el de la ventana activa. La *ventana activa* es la ventana de nivel superior con la que el usuario está trabajando actualmente. La ventana con el foco de teclado es la ventana activa o una ventana secundaria de la ventana activa. Para ayudar al usuario a identificar la ventana activa, el sistema la coloca en la parte superior del orden Z y resalta la barra de título (si tiene una) y el borde.

Para activar una ventana de nivel superior, el usuario puede hacer clic en ella, seleccionarla con la combinación de teclas ALT + TAB o ALT + ESC, o seleccionarla en el Lista de tareas. Un subproceso puede activar una ventana de nivel superior mediante la función [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) . Puede determinar si una ventana de nivel superior que creó está activa mediante la función [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) .

Cuando se desactiva una ventana y otra activada, el sistema envía el mensaje [**de \_ activación de WM**](wm-activate.md) . La palabra de orden inferior del parámetro *wParam* es cero si la ventana se está desactivando y es distinto de cero si se está activando. Cuando el procedimiento de ventana predeterminado recibe el mensaje de **\_ activación de WM** , establece el foco de teclado en la ventana activa.

Para impedir que los eventos de entrada de teclado y del mouse lleguen a aplicaciones, use [**BlockInput**](/windows/win32/api/winuser/nf-winuser-blockinput). Tenga en cuenta que la función **BlockInput** no interfiere con la tabla de estado de entrada de teclado asincrónica. Esto significa que si se llama a la función [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) mientras la entrada está bloqueada, cambiará la tabla de estado de entrada de teclado asincrónica.

## <a name="keystroke-messages"></a>Mensajes de pulsación de teclas

Al presionar una tecla, se coloca un mensaje de [**\_ SYSKEYDOWN**](wm-syskeydown.md) de WM [**\_ KEYDOWN**](wm-keydown.md) o WM en la cola de mensajes de subprocesos asociada a la ventana que tiene el foco de teclado. Al liberar una clave, se coloca un mensaje de [**\_ SYSKEYUP**](wm-syskeyup.md) de [**WM \_**](wm-keyup.md) o de WM en la cola.

Los mensajes de clave arriba y de tecla presionada suelen aparecer en parejas, pero si el usuario mantiene presionada una tecla suficiente para iniciar la característica de repetición automática del teclado, el sistema genera un número de [**mensajes \_ SYSKEYDOWN**](wm-syskeydown.md) de [**WM \_ o de**](wm-keydown.md) WM en una fila. A continuación, genera un único mensaje de [**\_ SYSKEYUP**](wm-syskeyup.md) de [**WM \_**](wm-keyup.md) o WM de WM cuando el usuario libera la clave.

En esta sección se describen los temas siguientes:

-   [Pulsaciones de teclas del sistema y no del sistema](#system-and-nonsystem-keystrokes)
-   [Códigos de clave virtual descritos](#virtual-key-codes-described)
-   [Marcas de mensajes de pulsación de teclas](#keystroke-message-flags)

### <a name="system-and-nonsystem-keystrokes"></a>Pulsaciones de teclas del sistema y no del sistema

El sistema hace una distinción entre las pulsaciones de teclas del sistema y las pulsaciones de tecla que no son del sistema. Las pulsaciones de tecla del sistema generan mensajes de pulsación de tecla del sistema, [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) y [**WM \_ SYSKEYUP**](wm-syskeyup.md). Las pulsaciones de tecla que no son del sistema generan [**mensajes de \_**](wm-keyup.md)pulsación de tecla que no son del sistema, y de [**WM \_**](wm-keydown.md)

Si el procedimiento de ventana debe procesar un mensaje de pulsación de tecla del sistema, asegúrese de que después de procesar el mensaje el procedimiento lo pasa a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . De lo contrario, se deshabilitarán todas las operaciones del sistema que impliquen la tecla ALT cuando la ventana tenga el foco de teclado. Es decir, el usuario no podrá tener acceso a los menús o al menú del sistema de la ventana, ni usar las combinaciones de teclas ALT + ESC o ALT + TAB para activar una ventana diferente.

Los mensajes de pulsación de tecla del sistema son principalmente para su uso por parte del sistema en lugar de una aplicación. El sistema los usa para proporcionar su interfaz de teclado integrada a los menús y permitir al usuario controlar qué ventana está activa. Los mensajes de pulsación de teclas del sistema se generan cuando el usuario escribe una tecla en combinación con la tecla ALT, o cuando el usuario escribe y no tiene el foco de teclado (por ejemplo, cuando la aplicación activa está minimizada). En este caso, los mensajes se publican en la cola de mensajes asociada a la ventana activa.

Los mensajes de pulsación de tecla que no son del sistema son para uso de las ventanas de aplicación la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) no realiza ninguna acción. Un procedimiento de ventana puede descartar cualquier mensaje de pulsación de tecla que no sea de sistema que no necesite.

### <a name="virtual-key-codes-described"></a>Códigos Virtual-Key descritos

El parámetro **wParam** de un mensaje de pulsación de teclas contiene el código de tecla virtual de la tecla que se presionó o se liberó. Un procedimiento de ventana procesa u omite un mensaje de pulsación de tecla, dependiendo del valor del código de la clave virtual.

Un procedimiento de ventana típico solo procesa un pequeño subconjunto de los mensajes de pulsación de tecla que recibe y omite el resto. Por ejemplo, un procedimiento de ventana podría procesar solo los mensajes de pulsación de teclas de la [**\_ KEYDOWN de WM**](wm-keydown.md) , y solo aquellos que contengan códigos de tecla virtual para las teclas de desplazamiento del cursor, teclas de desplazamiento (también denominadas teclas de control) y teclas de función. Un procedimiento de ventana típico no procesa los mensajes de pulsación de tecla de las teclas de caracteres. En su lugar, utiliza la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) para convertir el mensaje en mensajes de caracteres. Para obtener más información sobre **TranslateMessage** y mensajes de caracteres, vea [mensajes de caracteres](#character-messages).

### <a name="keystroke-message-flags"></a>Marcas de mensajes de pulsación de teclas

El parámetro **lParam** de un mensaje de pulsación de tecla contiene información adicional acerca de la pulsación de tecla que generó el mensaje. Esta información incluye el número de repeticiones, el código de examen, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición. En la ilustración siguiente se muestran las ubicaciones de estos marcadores y valores en el parámetro **lParam** .

![las ubicaciones de las marcas y los valores en el parámetro lParam de un mensaje de pulsación de tecla](images/csinp-02.png)

Una aplicación puede usar los valores siguientes para manipular las marcas de pulsaciones de teclas.



| Value            | Descripción                                                                       |
|------------------|-----------------------------------------------------------------------------------|
| **KF \_ ALTDOWN**  | Manipula la marca de tecla ALT, que indica si se presiona la tecla ALT.     |
| **KF \_ DLGMODE**  | Manipula la marca de modo de cuadro de diálogo, que indica si un cuadro de diálogo está activo. |
| **KF \_ extendido** | Manipula la marca de clave extendida.                                                |
| **KF \_ MENUMODE** | Manipula la marca de modo de menú, que indica si un menú está activo.         |
| **KF \_ repetir**   | Manipula la marca de estado de clave anterior.                                          |
| **KF \_**       | Manipula la marca de estado de transición.                                            |



 

### <a name="repeat-count"></a>Número de repeticiones

Puede comprobar el número de repeticiones para determinar si un mensaje de pulsación de tecla representa más de una pulsación de tecla. El sistema incrementa el recuento cuando el teclado genera mensajes de [**WM \_ KEYDOWN**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) más rápido que una aplicación puede procesarlos. Esto suele ocurrir cuando el usuario mantiene presionada una tecla suficiente para iniciar la característica de repetición automática del teclado. En lugar de rellenar la cola de mensajes del sistema con los mensajes de clave desplegables resultantes, el sistema combina los mensajes en un mensaje de una sola tecla y aumenta el número de repeticiones. La liberación de una clave no puede iniciar la característica de repetición automática, por lo que el número de repeticiones de los mensajes de [**\_ SYSKEYUP**](wm-syskeyup.md) y de WM de [**WM \_**](wm-keyup.md) siempre se establece en 1.

### <a name="scan-code"></a>Examinar código

El código de análisis es el valor que genera el hardware del teclado cuando el usuario presiona una tecla. Es un valor dependiente del dispositivo que identifica la tecla presionada, en lugar del carácter representado por la clave. Normalmente, una aplicación omite los códigos de examen. En su lugar, utiliza códigos de tecla virtual independientes del dispositivo para interpretar los mensajes de pulsación de teclas.

### <a name="extended-key-flag"></a>Extended-Key marca

La marca de clave extendida indica si el mensaje de pulsación de tecla se originó en una de las teclas adicionales del teclado mejorado. Las claves extendidas constan de las teclas ALT y CTRL en el lado derecho del teclado. las teclas INS, SUPR, Inicio, fin, Re Pág, Av Pág y flecha en los clústeres a la izquierda del teclado numérico. tecla BLOQ NUM; tecla INTERRUMPIr (CTRL + pausa); tecla Impr Pant; y la división (/) y escriba las teclas en el teclado numérico. La marca de clave extendida se establece si la clave es una clave extendida.

### <a name="context-code"></a>Código de contexto

El código de contexto indica si la tecla ALT estaba presionada cuando se generó el mensaje de pulsación de tecla. El código es 1 si la tecla ALT estaba desactivada y 0 si estaba activo.

### <a name="previous-key-state-flag"></a>Marca de Key-State anterior

La marca de estado de clave anterior indica si la clave que generó el mensaje de pulsación de tecla estaba arriba o baja. Es 1 si la clave estaba inactiva previamente y 0 si la clave estaba antes. Puede usar esta marca para identificar los mensajes de pulsación de tecla generados por la característica de repetición automática del teclado. Esta marca se establece en 1 para los mensajes de pulsación de teclas de [**\_ SYSKEYDOWN**](wm-syskeydown.md) de [**WM \_**](wm-keydown.md) y de WM generados por la característica de repetición automática. Siempre se establece en 1 para los mensajes de [**\_ SYSKEYUP**](wm-syskeyup.md) y de WM [**\_ KEYUP**](wm-keyup.md) .

### <a name="transition-state-flag"></a>Transition-State marca

La marca de estado de transición indica si se presiona una tecla o si se suelta una tecla que genera el mensaje de pulsación de teclas. Esta marca siempre se establece en 0 para los mensajes de [**\_ SYSKEYDOWN**](wm-syskeydown.md) y de WM [**\_ KEYDOWN**](wm-keydown.md) ; siempre se establece en 1 para los mensajes [**de \_ SYSKEYUP**](wm-syskeyup.md) de [**WM \_**](wm-keyup.md) y WM.

## <a name="character-messages"></a>Mensajes de caracteres

Los mensajes de pulsación de tecla proporcionan una gran cantidad de información sobre las pulsaciones de teclas, pero no proporcionan códigos de caracteres para las pulsaciones de caracteres. Para recuperar códigos de carácter, una aplicación debe incluir la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) en su bucle de mensajes de subproceso. **TranslateMessage** pasa un mensaje de [**WM \_ KEYDOWN**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) a la distribución del teclado. El diseño examina el código de tecla virtual del mensaje y, si corresponde a una clave de carácter, proporciona el código de carácter equivalente (teniendo en cuenta el estado de las teclas Bloq Mayús y MAYÚSCULAs). A continuación, genera un mensaje de carácter que incluye el código de carácter y coloca el mensaje en la parte superior de la cola de mensajes. La siguiente iteración del bucle de mensajes quita el mensaje de carácter de la cola y envía el mensaje al procedimiento de ventana adecuado.

En esta sección se describen los temas siguientes:

-   [Mensajes de caracteres que no son de sistema](#nonsystem-character-messages)
-   [Mensajes no enviados](#dead-character-messages)

### <a name="nonsystem-character-messages"></a>Mensajes de caracteres que no son de sistema

Un procedimiento de ventana puede recibir los siguientes mensajes de caracteres: [**WM \_ Char**](wm-char.md), [**WM \_ DEADCHAR**](wm-deadchar.md), [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar), [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)y [**WM \_ UNICHAR**](wm-unichar.md). La función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera un mensaje de **WM \_ Char** o **WM \_ DEADCHAR** cuando procesa un mensaje de [**\_ KEYDOWN de WM**](wm-keydown.md) . De forma similar, genera un mensaje de **WM \_ SYSCHAR** o **WM \_ SYSDEADCHAR** cuando procesa un mensaje de [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) .

Normalmente, una aplicación que procesa la entrada del teclado omite todos los mensajes de [**WM \_ Char**](wm-char.md) y [**WM \_ UNICHAR**](wm-unichar.md) , pasando cualquier otro mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Tenga en cuenta que **WM \_ Char** usa el formato de transformación Unicode de 16 bits (UTF) mientras que **WM \_ unichar** usa UTF-32. El sistema utiliza los mensajes de [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) y [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md) para implementar las teclas de menú.

El parámetro **wParam** de todos los mensajes de caracteres contiene el código de carácter de la tecla que se presionó. El valor del código de carácter depende de la clase de ventana de la ventana que recibe el mensaje. Si se usó la versión Unicode de la función [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) para registrar la clase de ventana, el sistema proporciona caracteres Unicode a todas las ventanas de esa clase. De lo contrario, el sistema proporciona códigos de caracteres ASCII. Para obtener más información, vea [Unicode y juegos de caracteres](/windows/desktop/Intl/unicode-and-character-sets).

El contenido del parámetro **lParam** de un mensaje de carácter es idéntico al contenido del parámetro **lParam** del mensaje de tecla presionado que se ha traducido para generar el mensaje de carácter. Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](#keystroke-message-flags).

### <a name="dead-character-messages"></a>Mensajes de Dead-Character

Algunos teclados que no están en inglés contienen teclas de caracteres que no se espera que generen caracteres por sí mismos. En su lugar, se usan para agregar un diacrítico al carácter producido por la siguiente pulsación de tecla. Estas claves se denominan *claves* inactivas. La tecla acento circunflejo del teclado alemán es un ejemplo de una tecla muerta. Para escribir el carácter que se compone de una "o" con un acento circunflejo, un usuario de alemán escribiría la tecla acento circunflejo seguida de la tecla "o". La ventana con el foco de teclado recibiría la siguiente secuencia de mensajes:

1.  [**KEYDOWN de WM \_**](wm-keydown.md)
2.  [**DEADCHAR de WM \_**](wm-deadchar.md)
3.  [**KEYUP de WM \_**](wm-keyup.md)
4.  [**KEYDOWN de WM \_**](wm-keydown.md)
5.  [**carácter de WM \_**](wm-char.md)
6.  [**KEYUP de WM \_**](wm-keyup.md)

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera el mensaje de [**\_ DEADCHAR de WM**](wm-deadchar.md) cuando procesa el mensaje de [**\_ KEYDOWN de WM**](wm-keydown.md) a partir de una clave muerta. Aunque el parámetro *wParam* del mensaje **de \_ DEADCHAR de WM** contiene el código de carácter del diacrítico de la clave muerta, una aplicación normalmente omite el mensaje. En su lugar, procesa el mensaje de [**\_ carácter de WM**](wm-char.md) generado por la siguiente pulsación de tecla. El parámetro *wParam* del mensaje **WM \_ Char** contiene el código de carácter de la letra con el diacrítico. Si la siguiente pulsación de tecla genera un carácter que no se puede combinar con un diacrítico, el sistema genera dos mensajes de **WM \_ Char** . El parámetro *wParam* de la primera contiene el código de carácter del diacrítico; el parámetro *wParam* del segundo contiene el código de carácter de la siguiente tecla de carácter.

La función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera el mensaje de [**\_ SYSDEADCHAR de WM**](wm-sysdeadchar.md) cuando procesa el mensaje de [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) desde una clave inactiva del sistema (una tecla de inactividad que se presiona en combinación con la tecla Alt). Normalmente, una aplicación omite el mensaje de **\_ SYSDEADCHAR de WM** .

## <a name="key-status"></a>Estado de la clave

Al procesar un mensaje de teclado, es posible que una aplicación necesite determinar el estado de otra clave además de la que generó el mensaje actual. Por ejemplo, una aplicación de procesamiento de texto que permite al usuario presionar Mayús + fin para seleccionar un bloque de texto debe comprobar el estado de la tecla Mayús cada vez que recibe un mensaje de pulsación de tecla de la tecla fin. La aplicación puede usar la función [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) para determinar el estado de una clave virtual en el momento en que se generó el mensaje actual. puede usar la función [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) para recuperar el estado actual de una clave virtual.

La distribución del teclado mantiene una lista de nombres. El nombre de una clave que genera un carácter único es el mismo que el carácter generado por la clave. El nombre de una clave que no sea de caracteres como TAB y entrar se almacena como una cadena de caracteres. Una aplicación puede recuperar el nombre de cualquier clave del controlador de dispositivo mediante una llamada a la función [**GetKeyNameText**](/windows/win32/api/winuser/nf-winuser-getkeynametexta) .

## <a name="keystroke-and-character-translations"></a>Traducciones de teclas y de caracteres

El sistema incluye varias funciones de propósito especial que traducen códigos de análisis, códigos de carácter y códigos de tecla virtual proporcionados por diversos mensajes de pulsación de tecla. Entre estas funciones se incluyen [**MapVirtualKey**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya), [**ToAscii**](/windows/win32/api/winuser/nf-winuser-toascii), [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)y [**VkKeyScan**](/windows/win32/api/winuser/nf-winuser-vkkeyscana).

Además, Microsoft Rich Edit 3,0 admite el [IME de HexToUnicode](/windows/desktop/Intl/hextounicode-ime), que permite a un usuario convertir entre caracteres hexadecimales y Unicode mediante el uso de teclas de acceso rápido. Esto significa que cuando se incorpora Microsoft Rich Edit 3,0 en una aplicación, la aplicación heredará las características de HexToUnicode IME.

## <a name="hot-key-support"></a>Compatibilidad con Hot-Key

Una *tecla de acceso rápido* es una combinación de teclas que genera un mensaje de [**\_ Hotkey de WM**](wm-hotkey.md) , un mensaje que el sistema coloca en la parte superior de la cola de mensajes de un subproceso, omitiendo los mensajes existentes en la cola. Las aplicaciones usan teclas de acceso rápido para obtener la entrada de teclado de alta prioridad del usuario. Por ejemplo, al definir una tecla de acceso rápido que consta de la combinación de teclas CTRL + C, una aplicación puede permitir que el usuario cancele una operación larga.

Para definir una tecla de acceso rápido, una aplicación llama a la función [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) , especificando la combinación de claves que genera el mensaje de [**\_ Hotkey de WM**](wm-hotkey.md) , el identificador de la ventana para recibir el mensaje y el identificador de la tecla de acceso rápido. Cuando el usuario presiona la tecla de acceso rápido, se coloca un mensaje de tecla de acceso **\_ rápido de WM** en la cola de mensajes del subproceso que creó la ventana. El parámetro *wParam* del mensaje contiene el identificador de la tecla de acceso rápido. La aplicación puede definir varias teclas de acceso rápido para un subproceso, pero cada tecla de acceso directo del subproceso debe tener un identificador único. Antes de que finalice la aplicación, debe usar la función [**UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) para destruir la tecla de acceso rápido.

Las aplicaciones pueden utilizar un control de tecla de acceso rápido para facilitar al usuario la elección de una tecla de acceso rápido. Los controles de tecla de acceso rápido se utilizan normalmente para definir una tecla de acceso rápido que activa una ventana; no usan las funciones [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) y [**UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) . En su lugar, una aplicación que usa un control de tecla de acceso rápido envía normalmente el mensaje de [**\_ SETHOTKEY de WM**](wm-sethotkey.md) para establecer la tecla de acceso rápido. Siempre que el usuario presiona la tecla de acceso rápido, el sistema envía un mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) que especifica la tecla de acceso \_ rápido SC. Para obtener más información sobre los controles de tecla de acceso rápido, vea el tema sobre el uso de controles de teclas de acceso rápido en [controles de tecla de acceso](../controls/hot-key-controls.md)rápido.

## <a name="keyboard-keys-for-browsing-and-other-functions"></a>Teclas del teclado para la exploración y otras funciones

Windows proporciona compatibilidad para los teclados con teclas especiales para las funciones del explorador, las funciones multimedia, el inicio de aplicaciones y la administración de energía. El [**\_ APPCOMMAND de WM**](wm-appcommand.md) admite las teclas de teclado adicionales. Además, la función [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) se modifica para admitir las teclas adicionales del teclado.

No es probable que una ventana secundaria en una aplicación de componentes pueda implementar directamente comandos para estas teclas adicionales del teclado. Por tanto, cuando se presiona una de estas teclas, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) enviará un mensaje de [**WM \_ APPCOMMAND**](wm-appcommand.md) a una ventana. **DefWindowProc** también propagará el mensaje de **\_ APPCOMMAND de WM** a su ventana primaria. Esto es similar a la manera en que se invocan los menús contextuales con el botón secundario del mouse, que es que **DefWindowProc** envía un mensaje de [**\_ CONTEXTMENU de WM**](/windows/desktop/menurc/wm-contextmenu) en un clic con el botón secundario y lo propaga a su elemento primario. Además, si **DefWindowProc** recibe un mensaje de **\_ APPCOMMAND de WM** para una ventana de nivel superior, llamará a un enlace de Shell con el código **HSHELL \_ APPCOMMAND**.

Windows también es compatible con el explorador de IntelliMouse de Microsoft, que es un mouse con cinco botones. Los dos botones adicionales admiten la navegación hacia delante y hacia atrás del explorador. Para obtener más información, vea [XBUTTONs](about-mouse-input.md).

## <a name="simulating-input"></a>Simular la entrada

Para simular una serie ininterrumpida de eventos de entrada de usuario, use la función [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) . La función acepta tres parámetros. El primer parámetro, *cInputs*, indica el número de eventos de entrada que se simularán. El segundo parámetro, *rgInputs*, es una matriz de estructuras de [**entrada**](/windows/win32/api/winuser/ns-winuser-input) , cada una de las cuales describe un tipo de evento de entrada e información adicional sobre el evento. El último parámetro, *cbSize*, acepta el tamaño de la estructura de **entrada** , en bytes.

La función [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) inserta una serie de eventos de entrada simulados en el flujo de entrada de un dispositivo. El efecto es similar a llamar a la función de evento [**keybd \_**](/windows/win32/api/winuser/nf-winuser-keybd_event) o de [**\_ evento del mouse**](/windows/win32/api/winuser/nf-winuser-mouse_event) repetidamente, salvo que el sistema garantiza que ningún otro evento de entrada intermingle con los eventos simulados. Cuando se completa la llamada, el valor devuelto indica el número de eventos de entrada reproducidos correctamente. Si este valor es cero, la entrada se bloqueó.

La función [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) no restablece el estado actual del teclado. Por lo tanto, si el usuario tiene presionadas las teclas al llamar a esta función, podrían interferir con los eventos generados por esta función. Si le preocupa la posible interferencia, compruebe el estado del teclado con la función [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) y corríjala según sea necesario.

## <a name="languages-locales-and-keyboard-layouts"></a>Idiomas, configuraciones regionales y distribuciones de teclado

Un *lenguaje* es un lenguaje natural, como inglés, francés y japonés. Un *subidioma* es una variante de un lenguaje natural que se habla en una región geográfica específica, como los sublenguas en inglés que se hablan en el Reino Unido y el Estados Unidos. Las aplicaciones usan valores, denominados [identificadores de idioma](/windows/desktop/Intl/language-identifiers), para identificar de forma única idiomas y subidiomas.

Las aplicaciones suelen usar *configuraciones regionales* para establecer el idioma en el que se procesan la entrada y la salida. El establecimiento de la configuración regional del teclado, por ejemplo, afecta a los valores de caracteres generados por el teclado. El establecimiento de la configuración regional de la pantalla o la impresora afecta a los glifos mostrados o impresos. Las aplicaciones establecen la configuración regional de un teclado mediante la carga y el uso de las distribuciones del teclado. Para establecer la configuración regional de una pantalla o una impresora, seleccione una fuente que admita la configuración regional especificada.

Una distribución del teclado no solo especifica la posición física de las teclas en el teclado, sino que también determina los valores de caracteres generados al presionar esas teclas. Cada diseño identifica el idioma de entrada actual y determina qué valores de caracteres son generados por qué teclas y combinaciones de teclas.

Cada distribución del teclado tiene un identificador correspondiente que identifica el diseño y el idioma. La palabra baja del identificador es un identificador de idioma. La palabra alta es un identificador de dispositivo, que especifica el diseño físico o es cero, lo que indica un diseño físico predeterminado. El usuario puede asociar cualquier idioma de entrada a un diseño físico. Por ejemplo, un usuario en inglés que ocasionalmente trabaja en francés puede establecer el idioma de entrada del teclado en francés sin cambiar el diseño físico del teclado. Esto significa que el usuario puede escribir texto en francés con el diseño en inglés conocido.

Normalmente no se espera que las aplicaciones manipulen los idiomas de entrada directamente. En su lugar, el usuario configura combinaciones de idioma y diseño y, a continuación, cambia entre ellas. Cuando el usuario hace clic en el texto marcado con un idioma diferente, la aplicación llama a la función [**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) para activar el diseño predeterminado del usuario para ese idioma. Si el usuario edita texto en un idioma que no está en la lista activa, la aplicación puede llamar a la función [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) con el lenguaje para obtener un diseño basado en ese idioma.

La función [**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) establece el idioma de entrada para la tarea actual. El parámetro *HKL* puede ser el identificador de la distribución del teclado o un identificador de idioma con extensión cero. Los identificadores de distribución del teclado se pueden obtener a partir de la función [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) o [**GetKeyboardLayoutList**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist) . Los valores de **HKL \_ siguiente** y **HKL \_ Prev** también se pueden usar para seleccionar el teclado siguiente o anterior.

La función [**GetKeyboardLayoutName**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea) recupera el nombre de la distribución de teclado activa para el subproceso que realiza la llamada. Si una aplicación crea el diseño activo mediante la función [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) , **GetKeyboardLayoutName** recupera la misma cadena que se usa para crear el diseño. De lo contrario, la cadena es el identificador de idioma principal correspondiente a la configuración regional del diseño activo. Esto significa que la función no puede diferenciar necesariamente entre distintos diseños con el mismo idioma principal, por lo que no puede devolver información específica sobre el idioma de entrada. La función [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) , sin embargo, se puede usar para determinar el idioma de entrada.

La función [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) carga una distribución del teclado y hace que el diseño esté disponible para el usuario. Las aplicaciones pueden hacer que el diseño esté inmediatamente activo para el subproceso actual mediante el valor de **\_ activación de KLF** . Una aplicación puede usar el valor de **\_ reordenación de KLF** para reordenar los diseños sin especificar también el valor de **KLF \_ Activate** . Las aplicaciones siempre deben usar el valor de **KLF \_ Substitute \_ OK** al cargar las distribuciones de teclado para asegurarse de que la preferencia del usuario, si existe, está seleccionada.

Para la compatibilidad multilingüe, la función [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) proporciona las marcas **KLF \_ REPLACELANG** y **KLF \_ NOTELLSHELL** . La marca **KLF \_ REPLACELANG** indica a la función que reemplace una distribución del teclado existente sin cambiar el idioma. El intento de reemplazar un diseño existente con el mismo identificador de idioma pero sin especificar **KLF \_ REPLACELANG** es un error. La marca **KLF \_ NOTELLSHELL** impide que la función notifique al shell cuando se agrega o reemplaza una distribución del teclado. Esto resulta útil para las aplicaciones que agregan varios diseños en una serie consecutiva de llamadas. Esta marca debe usarse en todas las llamadas excepto en la última.

La función [**UnloadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout) está restringida en que no puede descargar el idioma de entrada predeterminado del sistema. Esto garantiza que el usuario siempre tiene un diseño disponible para escribir texto mediante el mismo juego de caracteres que usa el Shell y el sistema de archivos.

 

 
