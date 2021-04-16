---
title: Entrada de teclado (introducción a Win32 y C++)
description: Entrada de teclado
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82065d4024428b48d4d3061da31a5384cab417d2
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "105678611"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a>Entrada de teclado (introducción a Win32 y C++)

El teclado se usa para varios tipos de entrada distintos, entre los que se incluyen:

-   Entrada de caracteres. Texto que el usuario escribe en un documento o cuadro de edición.
-   Métodos abreviados de teclado. Trazos de tecla que invocan funciones de aplicación. por ejemplo, CTRL + O para abrir un archivo.
-   Comandos del sistema. Trazos de tecla que invocan funciones del sistema; por ejemplo, ALT + TAB para cambiar de ventana.

Al pensar en la entrada de teclado, es importante recordar que un trazo de tecla no es lo mismo que un carácter. Por ejemplo, al presionar la tecla se podría producir cualquiera de los siguientes caracteres.

-   a
-   A
-   á (si el teclado admite la combinación de signos diacríticos)

Además, si se mantiene presionada la tecla ALT, al presionar la tecla se produce ALT + A, que el sistema no trata como un carácter, sino como un comando del sistema.

## <a name="key-codes"></a>Códigos de tecla

Al presionar una tecla, el hardware genera un *código de digitalización*. Los códigos de análisis varían de un teclado a otro, y hay códigos de exploración independientes para los eventos de clave y de clave. Casi nunca le interesarán los códigos de examen. El controlador de teclado traduce los códigos de análisis en *códigos de tecla virtual*. Los códigos de tecla virtual son independientes del dispositivo. Al presionar la tecla de cualquier teclado, se genera el mismo código de tecla virtual.

En general, los códigos de tecla virtual no corresponden a códigos ASCII ni a ningún otro estándar de codificación de caracteres. Esto es obvio si se piensa en él, ya que la misma clave puede generar caracteres diferentes (a, A, á á) y algunas teclas, como las teclas de función, no se corresponden con ningún carácter.

Dicho esto, los siguientes códigos de clave virtual se asignan a equivalentes ASCII:

-   de 0 a 9 claves = ASCII ' 0 ' – ' 9 ' (0x30 – 0x39)
-   De la a a la Z = ASCII ' A ' – ' Z ' (0x41 – 0x5A)

En algunos aspectos esta asignación es inestable, ya que nunca debe pensar en los códigos de tecla virtual como caracteres, por los motivos descritos.

El archivo de encabezado WinUser. h define constantes para la mayoría de los códigos de tecla virtual. Por ejemplo, el código de tecla virtual de la tecla de dirección izquierda es **VK \_ izquierdo** (0x25). Para obtener una lista completa de los códigos de tecla virtual, consulte [**códigos de clave virtual**](/windows/desktop/inputdev/virtual-key-codes). No se ha definido ninguna constante para los códigos de tecla virtual que coincidan con los valores ASCII. Por ejemplo, el código de tecla virtual de una clave es 0x41, pero no hay ninguna constante denominada **VK \_ A**. En su lugar, basta con usar el valor numérico.

## <a name="key-down-and-key-up-messages"></a>Mensajes de Key-Down y Key-Up

Al presionar una tecla, la ventana que tiene el foco de teclado recibe uno de los mensajes siguientes.

-   [**SYSKEYDOWN de WM \_**](/windows/desktop/inputdev/wm-syskeydown)
-   [**KEYDOWN de WM \_**](/windows/desktop/inputdev/wm-keydown)

El mensaje de [**\_ SYSKEYDOWN de WM**](/windows/desktop/inputdev/wm-syskeydown) indica una *clave del sistema*, que es un trazo de clave que invoca un comando del sistema. Hay dos tipos de clave del sistema:

-   ALT + cualquier tecla
-   F10

La tecla F10 activa la barra de menús de una ventana. Varias combinaciones de teclas ALT invocan comandos del sistema. Por ejemplo, ALT + TAB cambia a una nueva ventana. Además, si una ventana tiene un menú, se puede utilizar la tecla ALT para activar los elementos de menú. Algunas combinaciones de teclas ALT no hacen nada.

El resto de los trazos de clave se consideran claves que no son del sistema y generan el mensaje de [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) . Esto incluye las teclas de función que no son F10.

Cuando se libera una clave, el sistema envía un mensaje de tecla arriba correspondiente:

-   [**KEYUP de WM \_**](/windows/desktop/inputdev/wm-keyup)
-   [**SYSKEYUP de WM \_**](/windows/desktop/inputdev/wm-syskeyup)

Si mantiene presionada una tecla suficiente para iniciar la característica de repetición del teclado, el sistema envía varios mensajes de tecla presionada, seguidos de un único mensaje de tecla.

En los cuatro mensajes de teclado descritos hasta el momento, el parámetro *wParam* contiene el código de la clave virtual de la clave. El parámetro *lParam* contiene información diversa empaquetada en 32 bits. Normalmente no se necesita la información en *lParam*. Una marca que podría ser útil es el bit 30, la marca "estado de la clave anterior", que se establece en 1 para los mensajes de tecla presionados repetidos.

Como implica el nombre, los trazos de clave del sistema están pensados principalmente para su uso por parte del sistema operativo. Si intercepta el mensaje [**de \_ SYSKEYDOWN de WM**](/windows/desktop/inputdev/wm-syskeydown) , llame a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) después. De lo contrario, impedirá que el sistema operativo controle el comando.

## <a name="character-messages"></a>Mensajes de caracteres

Los trazos de clave se convierten en caracteres por la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) , que primero vimos en el [módulo 1](your-first-windows-program.md). Esta función examina los mensajes de tecla presionada y los convierte en caracteres. Para cada carácter que se genera, la función **TranslateMessage** coloca un mensaje de [**WM \_ Char**](/windows/desktop/inputdev/wm-char) o [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) en la cola de mensajes de la ventana. El parámetro *wParam* del mensaje contiene el carácter UTF-16.

Como puede imaginar, los mensajes de los [**\_ caracteres de WM**](/windows/desktop/inputdev/wm-char) se generan a partir de mensajes [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) , mientras que los mensajes de [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) se generan a partir de mensajes [**\_ SYSKEYDOWN de WM**](/windows/desktop/inputdev/wm-syskeydown) . Por ejemplo, supongamos que el usuario presiona la tecla Mayús seguida de una tecla. Suponiendo una distribución de teclado estándar, obtendría la siguiente secuencia de mensajes:

**WM \_ KEYDOWN**: Shift  
**WM \_ KEYDOWN**: A  
**WM \_ CARÁCTER**: ' A '  


Por otro lado, la combinación ALT + P generaría:

 **WM \_ SYSKEYDOWN**: \_ menú VK  
**WM \_ SYSKEYDOWN**: 0x50  
**WM \_ SYSCHAR**: ' p '  
**WM \_ SYSKEYUP**: 0x50  
**WM \_ KEYUP**: \_ menú VK  


(El código de la clave virtual para la tecla ALT se denomina VK \_ MENÚ para motivos históricos.)

El mensaje de [**\_ SYSCHAR de WM**](/windows/desktop/menurc/wm-syschar) indica un carácter del sistema. Al igual que con [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), normalmente debe pasar este mensaje directamente a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). De lo contrario, puede interferir con los comandos estándar del sistema. En concreto, no trate **WM \_ SYSCHAR** como texto que el usuario ha escrito.

El mensaje de carácter de [**WM \_**](/windows/desktop/inputdev/wm-char) es lo que se suele considerar como entrada de caracteres. El tipo de datos para el carácter es **WCHAR \_ t**, que representa un carácter Unicode UTF-16. La entrada de caracteres puede incluir caracteres fuera del intervalo ASCII, especialmente con distribuciones de teclado que se usan habitualmente fuera del Estados Unidos. Puede probar diferentes distribuciones de teclado si instala un teclado regional y, a continuación, usa la característica de teclado en pantalla.

Los usuarios también pueden instalar un editor de métodos de entrada (IME) para escribir scripts complejos, como caracteres japoneses, con un teclado estándar. Por ejemplo, si se usa un IME japonés para escribir el carácter katakana カ (ka), es posible que aparezcan los siguientes mensajes:

**WM \_ KEYDOWN**: VK \_ PROCESSKEY (tecla proceso de IME)  
**WM \_ KEYUP**: 0x4B  
**WM \_ KEYDOWN**: VK \_ PROCESSKEY  
**WM \_ KEYUP**: 0x41  
**WM \_ KEYDOWN**: VK \_ PROCESSKEY  
**WM \_ CHAR**: カ  
**WM \_ KEYUP**: VK \_ Return  


Algunas combinaciones de teclas CTRL se traducen en caracteres de control ASCII. Por ejemplo, CTRL + A se convierte en el carácter ASCII Ctrl-A (SOH) (valor ASCII 0x01). En el caso de la entrada de texto, normalmente debería filtrar los caracteres de control. Además, evite usar [**WM \_ Char**](/windows/desktop/inputdev/wm-char) para implementar métodos abreviados de teclado. En su lugar, use mensajes [**\_ KEYDOWN de WM**](/windows/desktop/inputdev/wm-keydown) o, incluso mejor, use una tabla de aceleradores. Las tablas de aceleradores se describen en el tema siguiente, [tablas de aceleradores](accelerator-tables.md).

En el código siguiente se muestran los mensajes de teclado principales en el depurador. Pruebe a jugar con diferentes combinaciones de teclas y vea qué mensajes se generan.


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a>Mensajes de teclado Misceláneos

La mayoría de las aplicaciones pueden pasar por alto otros mensajes de teclado sin ningún riesgo.

-   El mensaje de [**\_ DEADCHAR de WM**](/windows/desktop/inputdev/wm-deadchar) se envía para una clave combinada, como un diacrítico. Por ejemplo, en un teclado de idioma español, si escribe acento (') seguido de E, se genera el carácter é. El **\_ DEADCHAR de WM** se envía para el carácter de acento.
-   El mensaje de [**WM \_ UNICHAR**](/windows/desktop/inputdev/wm-unichar) está obsoleto. Permite a los programas ANSI recibir entradas de caracteres Unicode.
-   El carácter de carácter [**\_ \_ IME de WM**](/windows/desktop/Intl/wm-ime-char) se envía cuando un IME traduce una secuencia de teclas en caracteres. Se envía además del mensaje de [**\_ carácter**](/windows/desktop/inputdev/wm-char) normal de WM.

## <a name="keyboard-state"></a>Estado del teclado

Los mensajes del teclado están orientados a eventos. Es decir, recibe un mensaje cuando se produce algo interesante, como una pulsación de tecla, y el mensaje le indica lo que ha sucedido. Pero también puede probar el estado de una clave en cualquier momento llamando a la función [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) .

Por ejemplo, considere la posibilidad de detectar la combinación de hacer clic con el botón primario y la tecla ALT. Puede realizar un seguimiento del estado de la tecla ALT escuchando los mensajes de traza de teclas y almacenando una marca, pero [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) le evita los problemas. Cuando reciba el mensaje [**de \_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown) , simplemente llame a **GetKeyState** como se indica a continuación:


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



El mensaje [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) toma un código de clave virtual como entrada y devuelve un conjunto de marcas de bits (en realidad, solo dos marcadores). El valor 0x8000 contiene la marca de bits que comprueba si la tecla está presionada actualmente.

La mayoría de los teclados tienen dos teclas ALT, izquierda y derecha. En el ejemplo anterior se comprueba si alguna de ellas está presionada. También puede usar [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) para distinguir entre las instancias izquierda y derecha de las teclas Alt, Mayús o Ctrl. Por ejemplo, el código siguiente comprueba si se presiona la tecla ALT derecha.


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



La función [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) es interesante porque informa de un estado de teclado *virtual* . Este estado virtual se basa en el contenido de la cola de mensajes y se actualiza a medida que se quitan los mensajes de la cola. Cuando el programa procesa los mensajes de ventana, **GetKeyState** le proporciona una instantánea del teclado en el momento en que se puso en cola cada mensaje. Por ejemplo, si el último mensaje de la cola era [**\_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** notifica el estado del teclado en el momento en que el usuario hizo clic con el botón del mouse.

Dado que [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) se basa en la cola de mensajes, también omite la entrada del teclado que se envió a otro programa. Si el usuario cambia a otro programa, **GetKeyState** omite cualquier pulsación de tecla que se envíe a ese programa. Si realmente desea conocer el estado físico inmediato del teclado, hay una función para eso: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate). Sin embargo, para la mayoría del código de interfaz de usuario, la función correcta es **GetKeyState**.

## <a name="next"></a>Siguientes

[Tablas de aceleradores](accelerator-tables.md)

 

 
