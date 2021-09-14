---
title: Entrada de teclado (Introducción con Win32 y C++)
description: Entrada de teclado
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82065d4024428b48d4d3061da31a5384cab417d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159974"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a>Entrada de teclado (Introducción con Win32 y C++)

El teclado se usa para varios tipos distintos de entrada, entre los que se incluyen:

-   Entrada de caracteres. Texto que el usuario escriba en un documento o cuadro de edición.
-   Métodos abreviados de teclado. Trazos de clave que invocan funciones de aplicación; por ejemplo, CTRL + O para abrir un archivo.
-   Comandos del sistema. Trazos de clave que invocan funciones del sistema; por ejemplo, ALT + TAB para cambiar las ventanas.

Al pensar en la entrada de teclado, es importante recordar que un trazo de tecla no es lo mismo que un carácter. Por ejemplo, al presionar la tecla A, podría producirse cualquiera de los caracteres siguientes.

-   a
-   A
-   á (si el teclado admite la combinación de signos diacríticos)

Además, si se mantiene presionada la tecla ALT, al presionar la tecla A se genera ALT+A, que el sistema no trata como un carácter en absoluto, sino como un comando del sistema.

## <a name="key-codes"></a>Códigos de clave

Al presionar una tecla, el hardware genera un código *de examen*. Los códigos de examen varían de un teclado al siguiente y hay códigos de examen independientes para eventos de flecha arriba y abajo. Casi nunca le importarán los códigos de examen. El controlador de teclado traduce los códigos de examen en *códigos de clave virtual.* Los códigos de clave virtual son independientes del dispositivo. Al presionar la tecla A en cualquier teclado, se genera el mismo código de clave virtual.

En general, los códigos de clave virtual no se corresponden con códigos ASCII ni con ningún otro estándar de codificación de caracteres. Esto es obvio si piensa en ello, ya que la misma clave puede generar caracteres diferentes (a, A, á) y algunas claves, como las claves de función, no se corresponden con ningún carácter.

Dicho esto, los siguientes códigos de clave virtual se asignan a equivalentes ASCII:

-   De 0 a 9 claves = ASCII '0' – '9' (0x30 – 0x39)
-   Claves de A a Z = ASCII "A" – "Z" (0x41 – 0x5A)

En algunos aspectos, esta asignación es desafortunada, ya que nunca debe considerar los códigos de clave virtual como caracteres, por las razones que se deban analizar.

El archivo de encabezado WinUser.h define constantes para la mayoría de los códigos de clave virtual. Por ejemplo, el código de clave virtual para la tecla FLECHA IZQUIERDA es **VK \_ LEFT** (0x25). Para obtener la lista completa de códigos de clave virtual, vea [**Códigos de clave virtual**](/windows/desktop/inputdev/virtual-key-codes). No se definen constantes para los códigos de clave virtual que coinciden con los valores ASCII. Por ejemplo, el código de clave virtual de la clave A es 0x41, pero no hay ninguna constante denominada **VK \_ A**. En su lugar, solo tiene que usar el valor numérico.

## <a name="key-down-and-key-up-messages"></a>Key-Down y Key-Up mensajes

Al presionar una tecla, la ventana que tiene el foco de teclado recibe uno de los mensajes siguientes.

-   [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown)
-   [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)

El [**mensaje \_ SYSKEYDOWN de WM**](/windows/desktop/inputdev/wm-syskeydown) indica una clave del *sistema*, que es un trazo de clave que invoca un comando del sistema. Hay dos tipos de clave del sistema:

-   ALT + cualquier tecla
-   F10

La tecla F10 activa la barra de menús de una ventana. Varias combinaciones de teclas ALT invocan comandos del sistema. Por ejemplo, ALT + TAB cambia a una nueva ventana. Además, si una ventana tiene un menú, se puede usar la tecla ALT para activar los elementos de menú. Algunas combinaciones de teclas ALT no hacen nada.

Todos los demás trazos de clave se consideran claves que no son del sistema y generan el [**mensaje \_ KEYDOWN de WM.**](/windows/desktop/inputdev/wm-keydown) Esto incluye las claves de función que no son F10.

Cuando se libera una clave, el sistema envía un mensaje de actualización de claves correspondiente:

-   [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)
-   [**WM \_ SYSKEYUP**](/windows/desktop/inputdev/wm-syskeyup)

Si mantiene presionada una tecla lo suficiente como para iniciar la característica de repetición del teclado, el sistema envía varios mensajes de tecla abajo, seguidos de un único mensaje de tecla arriba.

En los cuatro mensajes de teclado analizados hasta ahora, el *parámetro wParam* contiene el código de clave virtual de la clave. El *parámetro lParam* contiene información varios empaquetada en 32 bits. Normalmente no necesita la información en *lParam*. Una marca que puede ser útil es el bit 30, la marca "estado de clave anterior", que se establece en 1 para los mensajes de tecla abajo repetidos.

Como su nombre implica, los trazos de clave del sistema están diseñados principalmente para su uso por parte del sistema operativo. Si intercepta el mensaje [**\_ SYSKEYDOWN de WM,**](/windows/desktop/inputdev/wm-syskeydown) llame [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) después. De lo contrario, impedirá que el sistema operativo controle el comando.

## <a name="character-messages"></a>Mensajes de caracteres

Los trazos clave se convierten en caracteres mediante la [**función TranslateMessage,**](/windows/desktop/api/winuser/nf-winuser-translatemessage) que vimos por primera vez en [el módulo 1.](your-first-windows-program.md) Esta función examina los mensajes de la tecla abajo y los traduce en caracteres. Para cada carácter que se genera, la función **TranslateMessage** coloca un mensaje [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) o [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) en la cola de mensajes de la ventana. El *parámetro wParam* del mensaje contiene el carácter UTF-16.

Como puede adivinar, los [**mensajes \_ CHAR**](/windows/desktop/inputdev/wm-char) de WM se generan a partir de mensajes [**WM \_ KEYDOWN,**](/windows/desktop/inputdev/wm-keydown) mientras que los [**mensajes \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) de WM se generan a partir [**de mensajes \_ SYSKEYDOWN de WM.**](/windows/desktop/inputdev/wm-syskeydown) Por ejemplo, supongamos que el usuario presiona la tecla MAYÚS seguida de la tecla A. Suponiendo un diseño de teclado estándar, se obtiene la siguiente secuencia de mensajes:

**WM \_ KEYDOWN:** MAYÚS  
**WM \_ KEYDOWN:** A  
**WM \_ CHAR:**'A'  


Por otro lado, la combinación ALT + P generaría:

 **WM \_ SYSKEYDOWN:** MENÚ \_ DE VK  
**WM \_ SYSKEYDOWN:** 0x50  
**WM \_ SYSCHAR:**'p'  
**WM \_ SYSKEYUP**: 0x50  
**WM \_ KEYUP:** MENÚ \_ DE VK  


(El código de clave virtual de la clave ALT se denomina VK \_ MENU por motivos históricos).

El [**mensaje \_ SYSCHAR de WM**](/windows/desktop/menurc/wm-syschar) indica un carácter del sistema. Al igual [**que con WM \_ SYSKEYDOWN,**](/windows/desktop/inputdev/wm-syskeydown)normalmente debería pasar este mensaje directamente a [**DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) De lo contrario, puede interferir con los comandos estándar del sistema. En concreto, no trate **WM \_ SYSCHAR como** texto escrito por el usuario.

El [**mensaje CHAR \_ de WM**](/windows/desktop/inputdev/wm-char) es lo que normalmente se considera como entrada de caracteres. El tipo de datos del carácter **es wchar \_ t**, que representa un carácter Unicode UTF-16. La entrada de caracteres puede incluir caracteres fuera del intervalo ASCII, especialmente con diseños de teclado que se usan normalmente fuera del Estados Unidos. Para probar diseños de teclado diferentes, instale un teclado regional y, a continuación, use la característica Teclado en pantalla.

Los usuarios también pueden instalar un Editor de métodos de entrada (IME) para escribir scripts complejos, como caracteres en japonés, con un teclado estándar. Por ejemplo, si usa un IME japonés para escribir el carácter katakana (ka), es posible que reciba los siguientes mensajes:

**WM \_ KEYDOWN:** CLAVE \_ PROCESSKEY de VK (la clave PROCESS de IME)  
**WM \_ KEYUP**: 0x4B  
**WM \_ KEYDOWN:** CLAVE DE \_ PROCESO DE VK  
**WM \_ KEYUP**: 0x41  
**WM \_ KEYDOWN:** CLAVE DE \_ PROCESO DE VK  
**WM \_ CHAR**:  
**WM \_ KEYUP:** VK \_ RETURN  


Algunas combinaciones de teclas CTRL se traducen en caracteres de control ASCII. Por ejemplo, CTRL+A se traduce al carácter ASCII ctrl-A (SOH) (valor ASCII 0x01). En el caso de la entrada de texto, por lo general debe filtrar los caracteres de control. Además, evite usar [**WM \_ CHAR para**](/windows/desktop/inputdev/wm-char) implementar métodos abreviados de teclado. En su lugar, [**use mensajes \_ WM KEYDOWN;**](/windows/desktop/inputdev/wm-keydown) o incluso mejor, use una tabla de aceleradores. Las tablas de aceleradores se describen en el tema siguiente, [Tablas de aceleradores](accelerator-tables.md).

El código siguiente muestra los mensajes de teclado principales en el depurador. Pruebe a reproducir con diferentes combinaciones de pulsaciones de teclas y vea qué mensajes se generan.


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



## <a name="miscellaneous-keyboard-messages"></a>Mensajes de teclado varios

La mayoría de las aplicaciones pueden omitir algunos otros mensajes de teclado de forma segura.

-   El [**mensaje \_ DEADCHAR de WM**](/windows/desktop/inputdev/wm-deadchar) se envía para una clave de combinación, como un diacrítico. Por ejemplo, en un teclado en español, al escribir el acento (') seguido de E se genera el carácter é. El **\_ DEADCHAR de WM** se envía para el carácter de acento.
-   El [**mensaje \_ WM UNICHAR**](/windows/desktop/inputdev/wm-unichar) está obsoleto. Permite que los programas ANSI reciban entradas de caracteres Unicode.
-   El [**carácter CHAR \_ \_ de WM IME**](/windows/desktop/Intl/wm-ime-char) se envía cuando un IME convierte una secuencia de pulsación de tecla en caracteres. Se envía además del mensaje [**WM \_ CHAR**](/windows/desktop/inputdev/wm-char) habitual.

## <a name="keyboard-state"></a>Estado del teclado

Los mensajes de teclado están controlados por eventos. Es decir, recibe un mensaje cuando sucede algo interesante, como una pulsación de tecla, y el mensaje le indica lo que acaba de ocurrir. Pero también puede probar el estado de una clave en cualquier momento mediante una llamada a la [**función GetKeyState.**](/windows/desktop/api/winuser/nf-winuser-getkeystate)

Por ejemplo, considere cómo detectaría la combinación de clic del mouse izquierdo + tecla ALT. Puede realizar un seguimiento del estado de la clave ALT escuchando mensajes de trazo de clave y almacenando una marca, pero [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) le ahorra el problema. Cuando reciba el mensaje [**WM \_ LBUTTONDOWN,**](/windows/desktop/inputdev/wm-lbuttondown) simplemente llame a **GetKeyState** como se indica a continuación:


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



El [**mensaje GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) toma un código de clave virtual como entrada y devuelve un conjunto de marcas de bits (en realidad solo dos marcas). El valor 0x8000 contiene la marca de bits que comprueba si la tecla está presionada actualmente.

La mayoría de los teclados tienen dos teclas ALT, izquierda y derecha. En el ejemplo anterior se comprueba si alguno de ellos está presionado. También puede usar [**GetKeyState para**](/windows/desktop/api/winuser/nf-winuser-getkeystate) distinguir entre las instancias izquierda y derecha de las teclas ALT, MAYÚS o CTRL. Por ejemplo, el código siguiente comprueba si se presiona la tecla ALT derecha.


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



La [**función GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) es interesante porque informa de un estado *de teclado virtual.* Este estado virtual se basa en el contenido de la cola de mensajes y se actualiza a medida que se quitan los mensajes de la cola. A medida que el programa procesa los mensajes de ventana, **GetKeyState** le proporciona una instantánea del teclado en el momento en que se pone en cola cada mensaje. Por ejemplo, si el último mensaje de la cola era [**WM \_ LBUTTONDOWN,**](/windows/desktop/inputdev/wm-lbuttondown) **GetKeyState** notifica el estado del teclado en el momento en que el usuario hizo clic en el botón del mouse.

Dado [**que GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) se basa en la cola de mensajes, también omite la entrada de teclado que se envió a otro programa. Si el usuario cambia a otro programa, **GetKeyState** omite las pulsaciones de tecla que se envían a ese programa. Si realmente desea conocer el estado físico inmediato del teclado, hay una función para eso: [**GetAsyncKeyState.**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) Sin embargo, para la mayoría del código de interfaz de usuario, la función correcta **es GetKeyState.**

## <a name="next"></a>Siguientes

[Tablas de aceleradores](accelerator-tables.md)

 

 
