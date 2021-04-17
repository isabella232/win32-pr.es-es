---
title: Mensajes de ventana (introducción a Win32 y C++)
description: .
ms.assetid: 90c20456-44ed-4f0f-a6d3-b6c5660f0bc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7ea533a89cb0ccf7053945cd693cc6e1ef5c28
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "105689606"
---
# <a name="window-messages-get-started-with-win32-and-c"></a>Mensajes de ventana (introducción a Win32 y C++)

Una aplicación GUI debe responder a eventos del usuario y del sistema operativo.

- Los **eventos del usuario** incluyen todas las formas en que alguien puede interactuar con el programa: clics del mouse, trazos de tecla, gestos de pantalla táctil, etc.
- Los **eventos del sistema operativo** incluyen todo "fuera" del programa que puede afectar a la forma en que se comporta el programa. Por ejemplo, el usuario podría conectar un nuevo dispositivo de hardware, o bien Windows puede entrar en un estado de menor consumo (suspensión o hibernación).

Estos eventos pueden producirse en cualquier momento mientras el programa se está ejecutando, en casi cualquier orden. ¿Cómo se estructura un programa cuyo flujo de ejecución no se puede predecir de antemano?

Para solucionar este problema, Windows usa un modelo de paso de mensajes. El sistema operativo se comunica con la ventana de la aplicación pasando mensajes a ella. Un mensaje es simplemente un código numérico que designa un evento determinado. Por ejemplo, si el usuario presiona el botón primario del mouse, la ventana recibe un mensaje con el siguiente código de mensaje.

```C++
#define WM_LBUTTONDOWN    0x0201
```

Algunos mensajes tienen datos asociados. Por ejemplo, el mensaje de [**\_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown) incluye la coordenada x y la coordenada y del cursor del mouse.

Para pasar un mensaje a una ventana de, el sistema operativo llama al procedimiento de ventana registrado para esa ventana. (Y ahora sabe para qué sirve el procedimiento de ventana).

## <a name="the-message-loop"></a>El bucle de mensajes

Una aplicación recibirá miles de mensajes mientras se ejecuta. (Tenga en cuenta que cada clic de tecla y botón del mouse genera un mensaje). Además, una aplicación puede tener varias ventanas, cada una con su propio procedimiento de ventana. ¿Cómo recibe el programa todos estos mensajes y los entrega en el procedimiento de ventana correcto? La aplicación necesita un bucle para recuperar los mensajes y enviarlos a las ventanas correctas.

Para cada subproceso que crea una ventana, el sistema operativo crea una cola para los mensajes de ventana. Esta cola contiene mensajes para todas las ventanas que se crean en ese subproceso. La propia cola está oculta en el programa. No se puede manipular la cola directamente. Sin embargo, puede extraer un mensaje de la cola mediante una llamada a la función [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) .

```C++
MSG msg;
GetMessage(&msg, NULL, 0, 0);
```

Esta función quita el primer mensaje del encabezado de la cola. Si la cola está vacía, la función se bloquea hasta que se pone en cola otro mensaje. El hecho de que bloques [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) no haga que el programa deje de responder. Si no hay ningún mensaje, no hay nada que pueda realizar el programa. Si tiene que realizar el procesamiento en segundo plano, puede crear subprocesos adicionales que continúen ejecutándose mientras **GetMessage** espera a otro mensaje. (Vea [evitar cuellos de botella en el procedimiento de ventana](writing-the-window-procedure.md)).

El primer parámetro de [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) es la dirección de una estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) . Si la función se ejecuta correctamente, rellena la estructura **MSG** con información sobre el mensaje. Esto incluye la ventana de destino y el código de mensaje. Los otros tres parámetros permiten filtrar los mensajes que se obtienen de la cola. En casi todos los casos, estos parámetros se establecen en cero.

Aunque la estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) contiene información sobre el mensaje, casi nunca examinará esta estructura directamente. En su lugar, lo pasará directamente a otras dos funciones.

```C++
TranslateMessage(&msg); 
DispatchMessage(&msg);
```

La función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) está relacionada con la entrada de teclado. Convierte las pulsaciones de teclas (tecla abajo, tecla arriba) en caracteres. Realmente no es necesario saber cómo funciona esta función; simplemente Recuerde llamarlo antes de [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). El vínculo a la documentación de MSDN le proporcionará más información, si tiene curiosidad.

La función [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) indica al sistema operativo que llame al procedimiento de ventana de la ventana que es el destino del mensaje. En otras palabras, el sistema operativo busca el identificador de ventana en su tabla de ventanas, busca el puntero de función asociado a la ventana e invoca la función.

Por ejemplo, supongamos que el usuario presiona el botón primario del mouse. Esto produce una cadena de eventos:

1. El sistema operativo coloca un mensaje de [**\_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown) en la cola de mensajes.
2. El programa llama a la función [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) .
3. [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) extrae el mensaje de [**\_ LBUTTONDOWN de WM**](/windows/desktop/inputdev/wm-lbuttondown) de la cola y rellena la estructura [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) .
4. El programa llama a las funciones [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) y [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .
5. Dentro de [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), el sistema operativo llama al procedimiento de ventana.
6. El procedimiento de ventana puede responder al mensaje o pasarlo por alto.

Cuando el procedimiento de ventana vuelve, vuelve a [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). Esto vuelve al bucle de mensajes para el siguiente mensaje. Siempre que el programa se esté ejecutando, los mensajes seguirán llegando a la cola. Por lo tanto, debe tener un bucle que extraiga continuamente los mensajes de la cola y los envíe. Puede pensar en el bucle de la manera siguiente:

```C++
// WARNING: Don't actually write your loop this way.

while (1)      
{
    GetMessage(&msg, NULL, 0,  0);
    TranslateMessage(&msg); 
    DispatchMessage(&msg);
}
```

Como está escrito, por supuesto, este bucle nunca finalizaría. Es donde entra el valor devuelto para la función [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) . Normalmente, **GetMessage** devuelve un valor distinto de cero. Si desea salir de la aplicación e interrumpir el bucle de mensajes, llame a la función [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) .

```C++
        PostQuitMessage(0);
```

La función [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) coloca un mensaje de [**\_ salida de WM**](/windows/desktop/winmsg/wm-quit) en la cola de mensajes. **WM \_ QUIT** es un mensaje especial: hace que [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) devuelva cero, señalando el final del bucle de mensajes. Este es el bucle de mensajes revisado.

```C++
// Correct.

MSG msg = { };
while (GetMessage(&msg, NULL, 0, 0) > 0)
{
    TranslateMessage(&msg);
    DispatchMessage(&msg);
}
```

Siempre que [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) devuelva un valor distinto de cero, la expresión en el bucle **While** se evalúa como true. Después de llamar a [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage), la expresión se convierte en false y el programa se rompe fuera del bucle. (Un resultado interesante de este comportamiento es que el procedimiento de ventana nunca recibe un mensaje de [**\_ salida de WM**](/windows/desktop/winmsg/wm-quit) . Por lo tanto, no es necesario tener una instrucción Case para este mensaje en el procedimiento de ventana).

La siguiente pregunta obvia es cuándo llamar a [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage). Volveremos a esta pregunta en el tema de [cierre de la ventana](closing-the-window.md), pero primero tenemos que escribir el procedimiento de ventana.

## <a name="posted-messages-versus-sent-messages"></a>Mensajes publicados frente a mensajes enviados

En la sección anterior se habla sobre los mensajes que pasan a una cola. A veces, el sistema operativo llamará directamente a un procedimiento de ventana, omitiendo la cola.

La terminología de esta distinción puede resultar confusa:

-   *Publicar* un mensaje significa que el mensaje va a la cola de mensajes y se envía a través del bucle de mensajes ([**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) y [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)).
-   El *envío* de un mensaje significa que el mensaje omite la cola y el sistema operativo llama directamente al procedimiento de ventana.

Por ahora, la diferencia no es muy importante. El procedimiento de ventana controla todos los mensajes. Sin embargo, algunos mensajes omiten la cola y van directamente al procedimiento de ventana. Sin embargo, puede hacer una diferencia si la aplicación se comunica entre Windows. Puede encontrar una explicación más detallada de este problema en el tema [sobre mensajes y colas de mensajes](/windows/desktop/winmsg/about-messages-and-message-queues).

## <a name="next"></a>Siguientes

[Escribir el procedimiento de ventana](writing-the-window-procedure.md)
