---
title: Acerca de la entrada de teclado
description: En este tema se describe la entrada de teclado.
ms.assetid: de34727e-e8c7-481d-982d-0e42a02704db
keywords:
- entrada de usuario, entrada de teclado
- captura de la entrada del usuario, entrada de teclado
- entrada mediante teclado
- foco de teclado
- mensajes de pulsación de tecla
- mensajes de caracteres
- pulsaciones de teclas del sistema
- pulsaciones de teclas que no son del sistema
- mensajes de caracteres que no son del sistema
- claves fallcidas
- mensajes de caracteres no enviados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec8c9bf3c200ecf24ba3c114807a2bc6db1e0fbee44ef9c7a884c7059759fd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482947"
---
# <a name="about-keyboard-input"></a>Acerca de la entrada de teclado

Las aplicaciones deben aceptar la entrada del usuario desde el teclado, así como desde el mouse. Una aplicación recibe la entrada de teclado en forma de mensajes publicados en sus ventanas.

En esta sección se describen los temas siguientes:

-   [Modelo de entrada de teclado](#keyboard-input-model)
-   [Foco y activación del teclado](#keyboard-focus-and-activation)
-   [Mensajes de pulsación de tecla](#keystroke-messages)
    -   [Pulsaciones de teclas del sistema y no del sistema](#system-and-nonsystem-keystrokes)
    -   [Códigos de clave virtual descritos](#virtual-key-codes-described)
    -   [Marcas de mensaje de pulsación de tecla](#keystroke-message-flags)
-   [Mensajes de caracteres](#character-messages)
    -   [Mensajes de caracteres no del sistema](#nonsystem-character-messages)
    -   [Mensajes de caracteres no enviados](#dead-character-messages)
-   [Estado de clave](#key-status)
-   [Pulsaciones de teclas y traducciones de caracteres](#keystroke-and-character-translations)
-   [Compatibilidad con la tecla de acceso](#hot-key-support)
-   [Teclas de teclado para examinar y otras funciones](#keyboard-keys-for-browsing-and-other-functions)
-   [Simulación de entrada](#simulating-input)
-   [Idiomas, configuraciones regionales y diseños de teclado](#languages-locales-and-keyboard-layouts)

## <a name="keyboard-input-model"></a>Modelo de entrada de teclado

El sistema proporciona compatibilidad con teclado independiente del dispositivo para las aplicaciones mediante la instalación de un controlador de dispositivo de teclado adecuado para el teclado actual. El sistema proporciona compatibilidad con teclado independiente del idioma mediante el diseño de teclado específico del idioma seleccionado actualmente por el usuario o la aplicación. El controlador del dispositivo de teclado recibe códigos de examen del teclado, que se envían al diseño del teclado, donde se traducen en mensajes y se publican en las ventanas adecuadas de la aplicación.

Asignado a cada tecla de un teclado es un valor único denominado código *de* examen , un identificador dependiente del dispositivo para la tecla en el teclado. Un teclado genera dos códigos de examen cuando el usuario pulsa una tecla: una cuando el usuario presiona la tecla y otra cuando el usuario suelta la tecla.

El controlador de dispositivo de teclado interpreta un código de examen y lo traduce (lo asigna) a un código de clave *virtual,* un valor independiente del dispositivo definido por el sistema que identifica el propósito de una clave. Después de traducir un código de examen, el diseño del teclado crea un mensaje que incluye el código de examen, el código de clave virtual y otra información sobre la pulsación de tecla y, a continuación, coloca el mensaje en la cola de mensajes del sistema. El sistema quita el mensaje de la cola de mensajes del sistema y lo envía a la cola de mensajes del subproceso adecuado. Finalmente, el bucle de mensajes del subproceso quita el mensaje y lo pasa al procedimiento de ventana adecuado para su procesamiento. En la ilustración siguiente se muestra el modelo de entrada de teclado.

![modelo de procesamiento de entrada de teclado](images/csinp-01.png)

## <a name="keyboard-focus-and-activation"></a>Foco y activación del teclado

El sistema envía mensajes de teclado a la cola de mensajes del subproceso en primer plano que creó la ventana con el foco del teclado. El *foco del teclado* es una propiedad temporal de una ventana. El sistema comparte el teclado entre todas las ventanas de la pantalla desplazando el foco del teclado, en la dirección del usuario, de una ventana a otra. La ventana que tiene el foco de teclado recibe (de la cola de mensajes del subproceso que lo creó) todos los mensajes de teclado hasta que el foco cambia a otra ventana.

Un subproceso puede llamar a la [**función GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) para determinar cuál de sus ventanas (si existe) tiene actualmente el foco de teclado. Un subproceso puede dar el foco del teclado a una de sus ventanas mediante una llamada a la [**función SetFocus.**](/windows/win32/api/winuser/nf-winuser-setfocus) Cuando el foco del teclado cambia de una ventana a otra, el sistema envía un mensaje [**\_ KILLFOCUS**](wm-killfocus.md) de WM a la ventana que ha perdido el foco y, a continuación, envía un mensaje [**\_ SETFOCUS**](wm-setfocus.md) de WM a la ventana que ha obtenido el foco.

El concepto de foco de teclado está relacionado con el de la ventana activa. La *ventana activa* es la ventana de nivel superior con la que el usuario está trabajando actualmente. La ventana con el foco del teclado es la ventana activa o una ventana secundaria de la ventana activa. Para ayudar al usuario a identificar la ventana activa, el sistema la coloca en la parte superior del orden Z y resalta su barra de título (si tiene una) y el borde.

El usuario puede activar una ventana de nivel superior haciendo clic en ella, seleccionándose mediante la combinación de teclas ALT+TAB o ALT+ESC, o bien seleccionándose en la Lista de tareas. Un subproceso puede activar una ventana de nivel superior mediante la [**función SetActiveWindow.**](/windows/win32/api/winuser/nf-winuser-setactivewindow) Puede determinar si una ventana de nivel superior que creó está activa mediante la [**función GetActiveWindow.**](/windows/win32/api/winuser/nf-winuser-getactivewindow)

Cuando una ventana está desactivada y otra activada, el sistema envía el [**mensaje WM \_ ACTIVATE.**](wm-activate.md) La palabra de orden bajo del parámetro *wParam* es cero si se desactiva la ventana y es distinta de cero si se está activando. Cuando el procedimiento de ventana predeterminado recibe el **mensaje WM \_ ACTIVATE,** establece el foco del teclado en la ventana activa.

Para impedir que los eventos de entrada de teclado y mouse lleguen a las aplicaciones, use [**BlockInput**](/windows/win32/api/winuser/nf-winuser-blockinput). Tenga en cuenta que **la función BlockInput** no interferirá con la tabla de estado de entrada de teclado asincrónica. Esto significa que llamar a la [**función SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) mientras se bloquea la entrada cambiará la tabla de estado de entrada de teclado asincrónica.

## <a name="keystroke-messages"></a>Mensajes de pulsación de tecla

Al presionar una tecla, se coloca un mensaje [**WM \_ KEYDOWN**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) en la cola de mensajes del subproceso adjuntada a la ventana que tiene el foco del teclado. Al liberar una clave, se coloca en la cola un mensaje [**WM \_ KEYUP**](wm-keyup.md) o [**WM \_ SYSKEYUP.**](wm-syskeyup.md)

Los mensajes de flecha arriba y abajo suelen producirse en pares, pero si el usuario mantiene presionada una tecla lo suficiente como para iniciar la característica de repetición automática del teclado, el sistema genera una serie de mensajes [**\_ WM KEYDOWN**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) en una fila. A continuación, genera un único [**mensaje WM \_ KEYUP**](wm-keyup.md) o [**WM \_ SYSKEYUP**](wm-syskeyup.md) cuando el usuario libera la clave.

En esta sección se describen los temas siguientes:

-   [Pulsaciones de teclas del sistema y no del sistema](#system-and-nonsystem-keystrokes)
-   [Códigos de clave virtual descritos](#virtual-key-codes-described)
-   [Marcas de mensaje de pulsación de tecla](#keystroke-message-flags)

### <a name="system-and-nonsystem-keystrokes"></a>Pulsaciones de teclas del sistema y no del sistema

El sistema hace una distinción entre las pulsaciones de teclas del sistema y las pulsaciones de tecla que no son del sistema. Las pulsaciones de tecla del sistema generan mensajes de pulsación de teclas del sistema, [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) [**y WM \_ SYSKEYUP**](wm-syskeyup.md). Las pulsaciones de teclas que no son del sistema generan mensajes de pulsación de teclas que no son del sistema, [**WM \_ KEYDOWN**](wm-keydown.md) [**y WM \_ KEYUP**](wm-keyup.md).

Si el procedimiento de ventana debe procesar un mensaje de pulsación de tecla del sistema, asegúrese de que, después de procesar el mensaje, el procedimiento lo pasa a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) De lo contrario, todas las operaciones del sistema que implican la tecla ALT se deshabilitarán siempre que la ventana tenga el foco del teclado. Es decir, el usuario no podrá acceder a los menús de la ventana ni al menú Sistema, ni usar la combinación de teclas ALT+ESC o ALT+TAB para activar otra ventana.

Los mensajes de pulsación de tecla del sistema son principalmente para su uso por parte del sistema en lugar de por una aplicación. El sistema los usa para proporcionar su interfaz de teclado integrada a los menús y para permitir al usuario controlar qué ventana está activa. Los mensajes de pulsación de tecla del sistema se generan cuando el usuario presiona una tecla en combinación con la tecla ALT o cuando los tipos de usuario y ninguna ventana tienen el foco del teclado (por ejemplo, cuando se minimiza la aplicación activa). En este caso, los mensajes se publican en la cola de mensajes asociada a la ventana activa.

Los mensajes de pulsación de teclas que no son del sistema se usan en las ventanas de la aplicación; La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) no hace nada con ellos. Un procedimiento de ventana puede descartar cualquier mensaje de pulsación de tecla que no sea del sistema que no necesite.

### <a name="virtual-key-codes-described"></a>Virtual-Key descritos

El **parámetro wParam** de un mensaje de pulsación de tecla contiene el código de clave virtual de la clave que se presionó o soltó. Un procedimiento de ventana procesa o omite un mensaje de pulsación de tecla, en función del valor del código de clave virtual.

Un procedimiento de ventana típico procesa solo un pequeño subconjunto de los mensajes de pulsación de tecla que recibe y omite el resto. Por ejemplo, un procedimiento de ventana solo puede procesar mensajes de pulsación de teclas [**\_ WM KEYDOWN**](wm-keydown.md) y solo aquellos que contienen códigos de clave virtual para las teclas de movimiento del cursor, las teclas de desplazamiento (también denominadas teclas de control) y las claves de función. Un procedimiento de ventana típico no procesa mensajes de pulsación de tecla a partir de claves de caracteres. En su lugar, usa la [**función TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) para convertir el mensaje en mensajes de caracteres. Para obtener más información sobre **TranslateMessage** y los mensajes de caracteres, vea [Character Messages](#character-messages).

### <a name="keystroke-message-flags"></a>Marcas de mensaje de pulsación de tecla

El **parámetro lParam** de un mensaje de pulsación de tecla contiene información adicional sobre la pulsación de tecla que generó el mensaje. Esta información incluye el recuento de repeticiones, el código de examen, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición. En la ilustración siguiente se muestran las ubicaciones de estas marcas y valores en **el parámetro lParam.**

![las ubicaciones de las marcas y valores del parámetro lparam de un mensaje de pulsación de tecla](images/csinp-02.png)

Una aplicación puede usar los siguientes valores para manipular las marcas de pulsación de tecla.



| Valor            | Descripción                                                                       |
|------------------|-----------------------------------------------------------------------------------|
| **ALTDOWN DE CTRL \_**  | Manipula la marca de tecla ALT, que indica si se presiona la tecla ALT.     |
| **\_DLGMODE de DLGMODE de DLGMODE**  | Manipula la marca de modo de diálogo, que indica si un cuadro de diálogo está activo. |
| **EXTENSIÓN \_ EXTENDIDO** | Manipula la marca de clave extendida.                                                |
| **MENUMODE DE CONTEXTUAL \_** | Manipula la marca de modo de menú, que indica si un menú está activo.         |
| **KF \_ REPEAT**   | Manipula la marca de estado de clave anterior.                                          |
| **UP de KV \_**       | Manipula la marca de estado de transición.                                            |

Ejemplo de código:

```cpp
case WM_KEYDOWN:
case WM_KEYUP:
case WM_SYSKEYDOWN:
case WM_SYSKEYUP:
{
    WORD vkCode = LOWORD(wParam);                                       // virtual-key code

    BYTE scanCode = LOBYTE(HIWORD(lParam));                             // scan code
    BOOL scanCodeE0 = (HIWORD(lParam) & KF_EXTENDED) == KF_EXTENDED;    // extended-key flag, 1 if scancode has 0xE0 prefix

    BOOL upFlag = (HIWORD(lParam) & KF_UP) == KF_UP;                    // transition-state flag, 1 on keyup
    BOOL repeatFlag = (HIWORD(lParam) & KF_REPEAT) == KF_REPEAT;        // previous key-state flag, 1 on autorepeat
    WORD repeatCount = LOWORD(lParam);                                  // repeat count, > 0 if several keydown messages was combined into one message

    BOOL altDownFlag = (HIWORD(lParam) & KF_ALTDOWN) == KF_ALTDOWN;     // ALT key was pressed

    BOOL dlgModeFlag = (HIWORD(lParam) & KF_DLGMODE) == KF_DLGMODE;     // dialog box is active
    BOOL menuModeFlag = (HIWORD(lParam) & KF_MENUMODE) == KF_MENUMODE;  // menu is active
    
    // ...
}
break;
```

### <a name="repeat-count"></a>Número de repeticiones

Puede comprobar el recuento de repeticiones para determinar si un mensaje de pulsación de tecla representa más de una pulsación de tecla. El sistema incrementa el recuento cuando el teclado genera mensajes [**WM \_ KEYDOWN**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) más rápido de lo que una aplicación puede procesarlos. Esto suele ocurrir cuando el usuario mantiene presionada una tecla el tiempo suficiente para iniciar la característica de repetición automática del teclado. En lugar de rellenar la cola de mensajes del sistema con los mensajes de la tecla abajo resultantes, el sistema combina los mensajes en un único mensaje de tecla hacia abajo e incrementa el recuento de repeticiones. La liberación de una clave no puede iniciar la característica de repetición automática, por lo que el recuento de repeticiones para los mensajes [**WM \_ KEYUP**](wm-keyup.md) y [**WM \_ SYSKEYUP**](wm-syskeyup.md) siempre se establece en 1.

### <a name="scan-code"></a>Examinar código

El código de examen es el valor que el hardware de teclado genera cuando el usuario presiona una tecla. Es un valor dependiente del dispositivo que identifica la tecla presionada, en lugar del carácter representado por la clave. Normalmente, una aplicación omite los códigos de examen. En su lugar, usa los códigos de clave virtual independientes del dispositivo para interpretar los mensajes de pulsación de teclas.

### <a name="extended-key-flag"></a>Extended-Key flag

La marca de tecla extendida indica si el mensaje de pulsación de tecla se originó en una de las teclas adicionales del teclado mejorado. Las teclas extendidas constan de las teclas ALT y CTRL en el lado derecho del teclado; las teclas de dirección INS, DEL, HOME, END, PAGE UP, PAGE DOWN y en los clústeres situados a la izquierda del teclado numérico. tecla NUM LOCK; tecla BREAK (CTRL+PAUSA); la tecla PRINT SCRN; y las claves divide (/) y ENTRAR en el teclado numérico. La marca de clave extendida se establece si la clave es una clave extendida.

Si se especifica, el código de examen estaba precedido de un byte de prefijo con el 0xE0 (224).

### <a name="context-code"></a>Código de contexto

El código de contexto indica si la tecla ALT estaba fuera de línea cuando se generó el mensaje de pulsación de tecla. El código es 1 si la tecla ALT estaba fuera de servicio y 0 si estaba arriba.

### <a name="previous-key-state-flag"></a>Marca Key-State anterior

La marca de estado de clave anterior indica si la clave que generó el mensaje de pulsación de tecla estaba previamente arriba o abajo. Es 1 si la clave estaba anteriormente fuera de servicio y 0 si la clave estaba anteriormente arriba. Puede usar esta marca para identificar los mensajes de pulsación de tecla generados por la característica de repetición automática del teclado. Esta marca se establece en 1 para los mensajes de pulsación de tecla [**WM \_ KEYDOWN**](wm-keydown.md) y [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) generados por la característica de repetición automática. Siempre se establece en 1 para los [**mensajes WM \_ KEYUP**](wm-keyup.md) [**y WM \_ SYSKEYUP.**](wm-syskeyup.md)

### <a name="transition-state-flag"></a>Transition-State flag

La marca de estado de transición indica si al presionar una tecla o liberar una clave se generó el mensaje de pulsación de tecla. Esta marca siempre se establece en 0 para los mensajes [**WM \_ KEYDOWN**](wm-keydown.md) y [**WM \_ SYSKEYDOWN;**](wm-syskeydown.md) siempre se establece en 1 para los mensajes [**WM \_ KEYUP**](wm-keyup.md) y [**WM \_ SYSKEYUP.**](wm-syskeyup.md)

## <a name="character-messages"></a>Mensajes de caracteres

Los mensajes de pulsación de tecla proporcionan mucha información sobre las pulsaciones de teclas, pero no proporcionan códigos de caracteres para las pulsaciones de teclas de caracteres. Para recuperar códigos de caracteres, una aplicación debe incluir la [**función TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) en su bucle de mensajes de subproceso. **TranslateMessage** pasa un mensaje [**WM \_ KEYDOWN**](wm-keydown.md) [**o WM \_ SYSKEYDOWN**](wm-syskeydown.md) al diseño del teclado. El diseño examina el código de clave virtual del mensaje y, si corresponde a una clave de carácter, proporciona el código de carácter equivalente (teniendo en cuenta el estado de las teclas MAYÚS y CAPS LOCK). A continuación, genera un mensaje de caracteres que incluye el código de caracteres y coloca el mensaje en la parte superior de la cola de mensajes. La siguiente iteración del bucle de mensajes quita el mensaje de caracteres de la cola y envía el mensaje al procedimiento de ventana adecuado.

En esta sección se describen los temas siguientes:

-   [Mensajes de caracteres no del sistema](#nonsystem-character-messages)
-   [Mensajes de caracteres no enviados](#dead-character-messages)

### <a name="nonsystem-character-messages"></a>Mensajes de caracteres no del sistema

Un procedimiento de ventana puede recibir los siguientes mensajes de caracteres: [**WM \_ CHAR,**](wm-char.md) [**WM \_ DEADCHAR,**](wm-deadchar.md) [**WM \_ SYSCHAR,**](/windows/desktop/menurc/wm-syschar) [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)y [**WM \_ UNICHAR**](wm-unichar.md). La [**función TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera un mensaje **WM \_ CHAR** **o WM \_ DEADCHAR** cuando procesa un [**mensaje WM \_ KEYDOWN.**](wm-keydown.md) De forma similar, genera un mensaje **\_ SYSCHAR** o **WM \_ SYSDEADCHAR** cuando procesa un [**mensaje \_ SYSKEYDOWN de WM.**](wm-syskeydown.md)

Una aplicación que procesa la entrada de teclado normalmente omite todos los mensajes [**\_ DE WM CHAR**](wm-char.md) y WM [**\_ UNICHAR,**](wm-unichar.md) pasando cualquier otro mensaje a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Tenga en **cuenta que WM \_ CHAR** usa el formato de transformación Unicode (UTF) de 16 bits, mientras **que WM \_ UNICHAR** usa UTF-32. El sistema usa los [**mensajes \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) y [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md) de WM para implementar elementos mnemotécnicos de menú.

El **parámetro wParam** de todos los mensajes de caracteres contiene el código de carácter de la tecla de carácter que se presionó. El valor del código de carácter depende de la clase de ventana de la ventana que recibe el mensaje. Si se usó la versión Unicode de la función [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) para registrar la clase window, el sistema proporciona caracteres Unicode a todas las ventanas de esa clase. De lo contrario, el sistema proporciona códigos de caracteres ASCII. Para obtener más información, vea [Unicode y juegos de caracteres.](/windows/desktop/Intl/unicode-and-character-sets)

El contenido del **parámetro lParam** de un mensaje de caracteres es idéntico al contenido del parámetro **lParam** del mensaje de tecla abajo que se ha traducido para generar el mensaje de caracteres. Para obtener información, vea [Marcas de mensajes de pulsación de teclas](#keystroke-message-flags).

### <a name="dead-character-messages"></a>Dead-Character mensajes

Algunos teclados que no están en inglés contienen teclas de caracteres que no se espera que produzcan caracteres por sí mismos. En su lugar, se usan para agregar un signo diacrítico al carácter generado por la pulsación de tecla posterior. Estas claves se denominan *claves fallcidas.* La tecla de circunflejo de un teclado alemán es un ejemplo de una tecla no ejecutada. Para escribir el carácter que consta de una "o" con una circunflejo, un usuario alemán escribiría la clave de circunflejo seguida de la tecla "o". La ventana con el foco del teclado recibiría la siguiente secuencia de mensajes:

1.  [**WM \_ KEYDOWN**](wm-keydown.md)
2.  [**WM \_ DEADCHAR**](wm-deadchar.md)
3.  [**WM \_ KEYUP**](wm-keyup.md)
4.  [**WM \_ KEYDOWN**](wm-keydown.md)
5.  [**WM \_ CHAR**](wm-char.md)
6.  [**WM \_ KEYUP**](wm-keyup.md)

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera el mensaje [**\_ DEADCHAR de WM**](wm-deadchar.md) cuando procesa el mensaje WM [**\_ KEYDOWN**](wm-keydown.md) a partir de una clave fallada. Aunque el *parámetro wParam* del mensaje **\_ DEADCHAR de WM** contiene el código de carácter del signo diacrítico para la clave fallada, una aplicación normalmente omite el mensaje. En su lugar, procesa el [**mensaje \_ WM CHAR**](wm-char.md) generado por la pulsación de tecla posterior. El *parámetro wParam* del mensaje **CHAR \_ de WM** contiene el código de carácter de la letra con el signo diacrítico. Si la pulsación de tecla posterior genera un carácter que no se puede combinar con un signo diacrítico, el sistema genera dos mensajes **\_ WM CHAR.** El *parámetro wParam* de la primera contiene el código de carácter del signo diacrítico; El *parámetro wParam* del segundo contiene el código de carácter de la clave de carácter posterior.

La [**función TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera el mensaje [**\_ SYSDEADCHAR**](wm-sysdeadchar.md) de WM cuando procesa el mensaje [**\_ SYSKEYDOWN**](wm-syskeydown.md) de WM a partir de una tecla fallida del sistema (una tecla sin respuesta que se presiona en combinación con la tecla ALT). Normalmente, una aplicación omite el **mensaje \_ SYSDEADCHAR de WM.**

## <a name="key-status"></a>Estado de la clave

Al procesar un mensaje de teclado, es posible que una aplicación tenga que determinar el estado de otra tecla además de la que generó el mensaje actual. Por ejemplo, una aplicación de procesamiento de palabras que permita al usuario presionar MAYÚS+END para seleccionar un bloque de texto debe comprobar el estado de la tecla MAYÚS cada vez que reciba un mensaje de pulsación de tecla de la tecla END. La aplicación puede usar la [**función GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) para determinar el estado de una clave virtual en el momento en que se generó el mensaje actual. puede usar la [**función GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) para recuperar el estado actual de una clave virtual.

El diseño del teclado mantiene una lista de nombres. El nombre de una clave que genera un solo carácter es el mismo que el carácter generado por la clave. El nombre de una clave que no sea de caracteres, como TAB y ENTER, se almacena como una cadena de caracteres. Una aplicación puede recuperar el nombre de cualquier clave del controlador de dispositivo llamando a la [**función GetKeyNameText.**](/windows/win32/api/winuser/nf-winuser-getkeynametexta)

## <a name="keystroke-and-character-translations"></a>Pulsaciones de teclas y traducciones de caracteres

El sistema incluye varias funciones de propósito especial que traducen códigos de examen, códigos de caracteres y códigos de clave virtual proporcionados por varios mensajes de pulsación de teclas. Estas funciones incluyen [**MapVirtualKey,**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya) [**ToAscii,**](/windows/win32/api/winuser/nf-winuser-toascii) [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)y [**VkKeyScan.**](/windows/win32/api/winuser/nf-winuser-vkkeyscana)

Además, Microsoft Rich Edit 3.0 admite el [IME HexToUnicode,](/windows/desktop/Intl/hextounicode-ime)que permite a un usuario convertir entre caracteres hexadecimales y Unicode mediante teclas de acceso rápido. Esto significa que cuando Microsoft Rich Edit 3.0 se incorpora a una aplicación, la aplicación heredará las características del IME HexToUnicode.

## <a name="hot-key-support"></a>Hot-Key compatibilidad

Una *tecla de* acceso rápido es una combinación de teclas que genera un mensaje WM [**\_ HOTKEY,**](wm-hotkey.md) un mensaje que el sistema coloca en la parte superior de la cola de mensajes de un subproceso, omitiendo los mensajes existentes en la cola. Las aplicaciones usan teclas de acceso rápido para obtener la entrada de teclado de alta prioridad del usuario. Por ejemplo, al definir una tecla de acceso rápido que consta de la combinación de teclas CTRL+C, una aplicación puede permitir al usuario cancelar una operación larga.

Para definir una tecla de acceso rápido, una aplicación llama a la función [**RegisterHotKey,**](/windows/win32/api/winuser/nf-winuser-registerhotkey) especificando la combinación de claves que genera el mensaje [**WM \_ HOTKEY,**](wm-hotkey.md) el identificador de la ventana para recibir el mensaje y el identificador de la tecla de acceso rápido. Cuando el usuario presiona la tecla de acceso rápido, se coloca un mensaje **\_ WM HOTKEY** en la cola de mensajes del subproceso que creó la ventana. El *parámetro wParam* del mensaje contiene el identificador de la tecla de acceso. La aplicación puede definir varias teclas de acceso rápido para un subproceso, pero cada clave de acceso rápido del subproceso debe tener un identificador único. Antes de que finalice la aplicación, debe usar la [**función UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) para destruir la tecla de acceso rápido.

Las aplicaciones pueden usar un control de tecla de acceso rápido para facilitar al usuario la elección de una tecla de acceso rápido. Los controles de tecla de acceso activo se usan normalmente para definir una tecla de acceso activa que activa una ventana; no usan las funciones [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) y [**UnregisterHotKey.**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) En su lugar, una aplicación que usa un control de tecla de acceso rápido normalmente envía el mensaje [**\_ SETHOTKEY de WM**](wm-sethotkey.md) para establecer la tecla de acceso rápido. Cada vez que el usuario presiona la tecla de acceso rápido, el sistema envía un mensaje [**\_ WM SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) que especifica SC \_ HOTKEY. Para obtener más información sobre los controles de tecla de acceso, vea "Usar controles de tecla de acceso" en [Controles de tecla de acceso.](../controls/hot-key-controls.md)

## <a name="keyboard-keys-for-browsing-and-other-functions"></a>Teclas de teclado para examinar y otras funciones

Windows proporciona compatibilidad con teclados con teclas especiales para funciones del explorador, funciones multimedia, inicio de aplicaciones y administración de energía. [**WM \_ APPCOMMAND admite**](wm-appcommand.md) las teclas de teclado adicionales. Además, la [**función ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) se modifica para admitir las teclas de teclado adicionales.

Es poco probable que una ventana secundaria de una aplicación de componentes pueda implementar directamente comandos para estas teclas de teclado adicionales. Por lo tanto, cuando se presiona una de estas teclas, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) enviará un mensaje [**DE WM \_ APPCOMMAND**](wm-appcommand.md) a una ventana. **DefWindowProc también** mostrará el mensaje **WM \_ APPCOMMAND** en su ventana primaria. Esto es similar a la forma en que se invocan los menús contextuales con el botón derecho del mouse, que es que **DefWindowProc** envía un mensaje [**\_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) DE WM en un clic del botón derecho y lo burbujas a su elemento primario. Además, si **DefWindowProc** recibe un mensaje **DE WM \_ APPCOMMAND** para una ventana de nivel superior, llamará a un enlace de shell con el código **\_ APPCOMMAND de HSHELL**.

Windows también admite Microsoft IntelliMouse Explorer, que es un mouse con cinco botones. Los dos botones adicionales admiten la navegación hacia delante y hacia atrás del explorador. Para obtener más información, [vea XBUTTONs](about-mouse-input.md).

## <a name="simulating-input"></a>Simulación de entrada

Para simular una serie ininterrumpida de eventos de entrada de usuario, use la [**función SendInput.**](/windows/win32/api/winuser/nf-winuser-sendinput) La función acepta tres parámetros. El primer parámetro, *cInputs*, indica el número de eventos de entrada que se simularán. El segundo parámetro, *rgInputs*, es una matriz de estructuras [**INPUT,**](/windows/win32/api/winuser/ns-winuser-input) cada una de las que describe un tipo de evento de entrada e información adicional sobre ese evento. El último parámetro, *cbSize*, acepta el tamaño de la estructura **INPUT,** en bytes.

La [**función SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) funciona insertando una serie de eventos de entrada simulados en el flujo de entrada de un dispositivo. El efecto es similar a llamar al evento [**keybd \_**](/windows/win32/api/winuser/nf-winuser-keybd_event) o a la función de evento de [**mouse \_**](/windows/win32/api/winuser/nf-winuser-mouse_event) repetidamente, salvo que el sistema garantiza que ningún otro evento de entrada se interminpe con los eventos simulados. Cuando se completa la llamada, el valor devuelto indica el número de eventos de entrada que se reproducen correctamente. Si este valor es cero, se bloqueó la entrada.

La [**función SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) no restablece el estado actual del teclado. Por lo tanto, si el usuario tiene presionadas las teclas al llamar a esta función, podrían interferir con los eventos que genera esta función. Si le preocupa la posible interferencia, compruebe el estado del teclado con la [**función GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) y corrija según sea necesario.

## <a name="languages-locales-and-keyboard-layouts"></a>Idiomas, configuraciones regionales y diseños de teclado

Un *idioma* es un idioma natural, como inglés, francés y japonés. Un *subidioma* es una variante de un idioma natural que se habla en una región geográfica específica, como los subidiomaes de inglés que se hablan en el Reino Unido y el Estados Unidos. Las aplicaciones usan valores, [denominados identificadores de idioma,](/windows/desktop/Intl/language-identifiers)para identificar idiomas y sublenguajes de forma única.

Las aplicaciones suelen *usar configuraciones* regionales para establecer el idioma en el que se procesan la entrada y la salida. Establecer la configuración regional del teclado, por ejemplo, afecta a los valores de caracteres generados por el teclado. Establecer la configuración regional de la pantalla o impresora afecta a los glifos mostrados o impresos. Las aplicaciones establecen la configuración regional de un teclado mediante la carga y el uso de diseños de teclado. Establecen la configuración regional de una pantalla o impresora seleccionando una fuente que admita la configuración regional especificada.

Un diseño de teclado no solo especifica la posición física de las teclas en el teclado, sino que también determina los valores de caracteres generados al presionar esas teclas. Cada diseño identifica el idioma de entrada actual y determina qué valores de caracteres se generan mediante las claves y combinaciones de teclas.

Cada diseño de teclado tiene un identificador correspondiente que identifica el diseño y el idioma. La palabra baja del identificador es un identificador de idioma. La palabra alta es un identificador de dispositivo, que especifica el diseño físico o es cero, lo que indica un diseño físico predeterminado. El usuario puede asociar cualquier idioma de entrada a un diseño físico. Por ejemplo, un usuario de habla inglesa que trabaja en francés en ocasiones puede establecer el idioma de entrada del teclado en francés sin cambiar el diseño físico del teclado. Esto significa que el usuario puede escribir texto en francés mediante el conocido diseño en inglés.

Por lo general, no se espera que las aplicaciones manipulen directamente los idiomas de entrada. En su lugar, el usuario configura combinaciones de idioma y diseño y, a continuación, cambia entre ellas. Cuando el usuario hace clic en el texto marcado con un idioma diferente, la aplicación llama a la función [**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) para activar el diseño predeterminado del usuario para ese idioma. Si el usuario edita texto en un idioma que no está en la lista activa, la aplicación puede llamar a la función [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) con el idioma para obtener un diseño basado en ese idioma.

La [**función ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) establece el idioma de entrada para la tarea actual. El *parámetro hkl* puede ser el identificador del diseño del teclado o un identificador de idioma extendido de cero. Los identificadores de diseño de teclado se pueden obtener de [**la función LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) o [**GetKeyboardLayoutList.**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist) Los **valores HKL \_ NEXT** y **HKL \_ PREV** también se pueden usar para seleccionar el teclado siguiente o anterior.

La [**función GetKeyboardLayoutName**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea) recupera el nombre del diseño de teclado activo para el subproceso que realiza la llamada. Si una aplicación crea el diseño activo mediante la función [**LoadKeyboardLayout,**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) **GetKeyboardLayoutName** recupera la misma cadena usada para crear el diseño. De lo contrario, la cadena es el identificador de idioma principal correspondiente a la configuración regional del diseño activo. Esto significa que es posible que la función no diferencie necesariamente entre diseños diferentes con el mismo idioma principal, por lo que no puede devolver información específica sobre el idioma de entrada. Sin [**embargo, la función GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) se puede usar para determinar el idioma de entrada.

La [**función LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) carga un diseño de teclado y hace que el diseño esté disponible para el usuario. Las aplicaciones pueden activar inmediatamente el diseño para el subproceso actual mediante el **valor KLF \_ ACTIVATE.** Una aplicación puede usar el **valor \_ REORDER** de KLF para reordenar los diseños sin especificar también el **valor KLF \_ ACTIVATE.** Las aplicaciones siempre deben usar el valor **KLF \_ SUBSTITUTE \_ OK** al cargar diseños de teclado para asegurarse de que la preferencia del usuario, si existe, está seleccionada.

Para la compatibilidad multilingüe, [**la función LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) proporciona las marcas **\_ KLF REPLACELANG** y **KLF \_ NOTELLSHELL.** La **marca \_ REPLACELANG** de KLF dirige a la función para reemplazar un diseño de teclado existente sin cambiar el idioma. El intento de reemplazar un diseño existente con el mismo identificador de idioma pero sin especificar **KLF \_ REPLACELANG** es un error. La **marca \_ KLF NOTELLSHELL** impide que la función notifique al shell cuando se agrega o reemplaza un diseño de teclado. Esto es útil para las aplicaciones que agregan varios diseños en una serie consecutiva de llamadas. Esta marca debe usarse en todas las llamadas, menos en la última.

La [**función UnloadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout) está restringida en que no puede descargar el idioma de entrada predeterminado del sistema. Esto garantiza que el usuario siempre tenga un diseño disponible para escribir texto con el mismo juego de caracteres que usa el shell y el sistema de archivos.

 

 
