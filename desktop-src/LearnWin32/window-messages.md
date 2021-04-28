---
title: Mensajes de ventana (Introducción a Win32 y C++)
description: Mensajes de ventana (Introducción a Win32 y C++)
ms.assetid: 90c20456-44ed-4f0f-a6d3-b6c5660f0bc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00da564396e0f95947e33fb7d8db8b217ac5cdf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103843"
---
# <a name="window-messages-get-started-with-win32-and-c"></a>Mensajes de ventana (Introducción a Win32 y C++)

Una aplicación guia debe responder a eventos del usuario y del sistema operativo.

- **Los eventos del usuario** incluyen todas las formas en que alguien puede interactuar con el programa: clics del mouse, trazos de teclas, gestos de pantalla táctil, y así sucesivamente.
- **Los eventos del sistema operativo incluyen** cualquier cosa "fuera" del programa que pueda afectar a cómo se comporta el programa. Por ejemplo, el usuario podría conectar un nuevo dispositivo de hardware o Windows podría entrar en un estado de menor potencia (suspensión o hibernación).

Estos eventos pueden producirse en cualquier momento mientras se ejecuta el programa, en casi cualquier orden. ¿Cómo se estructura un programa cuyo flujo de ejecución no se puede predecir de antemano?

Para resolver este problema, Windows usa un modelo de paso de mensajes. El sistema operativo se comunica con la ventana de la aplicación pasando mensajes a ella. Un mensaje es simplemente un código numérico que designa un evento determinado. Por ejemplo, si el usuario presiona el botón izquierdo del mouse, la ventana recibe un mensaje que tiene el siguiente código de mensaje.

```C++
#define WM_LBUTTONDOWN    0x0201
```

Algunos mensajes tienen datos asociados. Por ejemplo, el [**mensaje \_ WM LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) incluye la coordenada x e y del cursor del mouse.

Para pasar un mensaje a una ventana, el sistema operativo llama al procedimiento de ventana registrado para esa ventana. (Y ahora sabe para qué es el procedimiento de ventana).

## <a name="the-message-loop"></a>El bucle de mensajes

Una aplicación recibirá miles de mensajes mientras se ejecuta. (Tenga en cuenta que cada pulsación de tecla y clic del botón del mouse genera un mensaje). Además, una aplicación puede tener varias ventanas, cada una con su propio procedimiento de ventana. ¿Cómo recibe el programa todos estos mensajes y los entrega al procedimiento de ventana correcto? La aplicación necesita un bucle para recuperar los mensajes y enviarlos a las ventanas correctas.

Para cada subproceso que crea una ventana, el sistema operativo crea una cola para los mensajes de ventana. Esta cola contiene mensajes para todas las ventanas que se crean en ese subproceso. La propia cola está oculta del programa. No se puede manipular la cola directamente. Sin embargo, puede extraer un mensaje de la cola llamando a la [**función GetMessage.**](/windows/desktop/api/winuser/nf-winuser-getmessage)

```C++
MSG msg;
GetMessage(&msg, NULL, 0, 0);
```

Esta función quita el primer mensaje del principio de la cola. Si la cola está vacía, la función se bloquea hasta que se pone en cola otro mensaje. El hecho de [**que los bloques GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) no hagan que el programa deje de responder. Si no hay ningún mensaje, no hay nada que hacer para el programa. Si tiene que realizar el procesamiento en segundo plano, puede crear subprocesos adicionales que sigan en ejecución mientras **GetMessage** espera otro mensaje. (Vea [Evitar cuellos de botella en el procedimiento de la ventana).](writing-the-window-procedure.md)

El primer parámetro de [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) es la dirección de una [**estructura MSG.**](/windows/win32/api/winuser/ns-winuser-msg) Si la función se realiza correctamente, rellena la estructura **MSG** con información sobre el mensaje. Esto incluye la ventana de destino y el código del mensaje. Los otros tres parámetros permiten filtrar qué mensajes se obtienen de la cola. En casi todos los casos, establecerá estos parámetros en cero.

Aunque la [**estructura MSG**](/windows/win32/api/winuser/ns-winuser-msg) contiene información sobre el mensaje, casi nunca examinará esta estructura directamente. En su lugar, la pasará directamente a otras dos funciones.

```C++
TranslateMessage(&msg); 
DispatchMessage(&msg);
```

La [**función TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) está relacionada con la entrada de teclado. Convierte las pulsaciones de tecla (tecla abajo, tecla arriba) en caracteres. Realmente no tiene que saber cómo funciona esta función. recuerde llamarlo antes de [**DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) El vínculo a la documentación de MSDN le dará más información, si tiene curiosidad.

La [**función DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) indica al sistema operativo que llame al procedimiento de ventana de la ventana que es el destino del mensaje. En otras palabras, el sistema operativo busca el identificador de ventana en su tabla de ventanas, busca el puntero de función asociado a la ventana e invoca la función.

Por ejemplo, suponga que el usuario presiona el botón izquierdo del mouse. Esto provoca una cadena de eventos:

1. El sistema operativo coloca un [**mensaje \_ WM LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) en la cola de mensajes.
2. El programa llama a la [**función GetMessage.**](/windows/desktop/api/winuser/nf-winuser-getmessage)
3. [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) extrae el mensaje [**\_ WM LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) de la cola y rellena la [**estructura MSG.**](/windows/win32/api/winuser/ns-winuser-msg)
4. El programa llama a [**las funciones TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) [**y DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)
5. Dentro [**de DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), el sistema operativo llama al procedimiento de ventana.
6. El procedimiento de ventana puede responder al mensaje o omitirlo.

Cuando se devuelve el procedimiento de ventana, vuelve a [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage). Esto devuelve al bucle de mensajes para el mensaje siguiente. Mientras el programa se esté ejecutando, los mensajes seguirán llegando a la cola. Por lo tanto, debe tener un bucle que extraiga continuamente los mensajes de la cola y los envíe. Puede pensar que el bucle hace lo siguiente:

```C++
// WARNING: Don't actually write your loop this way.

while (1)      
{
    GetMessage(&msg, NULL, 0,  0);
    TranslateMessage(&msg); 
    DispatchMessage(&msg);
}
```

Como se ha escrito, por supuesto, este bucle nunca terminaría. Aquí es donde entra en funcionamiento el valor devuelto para la función [**GetMessage.**](/windows/desktop/api/winuser/nf-winuser-getmessage) Normalmente, **GetMessage** devuelve un valor distinto de cero. Si desea salir de la aplicación y salir del bucle de mensajes, llame a la [**función PostQuitMessage.**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)

```C++
        PostQuitMessage(0);
```

La [**función PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) coloca un mensaje [**WM \_ QUIT**](/windows/desktop/winmsg/wm-quit) en la cola de mensajes. **WM \_ QUIT** es un mensaje especial: hace que [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) devuelva cero, lo que indica el final del bucle de mensajes. Este es el bucle de mensajes revisado.

```C++
// Correct.

MSG msg = { };
while (GetMessage(&msg, NULL, 0, 0) > 0)
{
    TranslateMessage(&msg);
    DispatchMessage(&msg);
}
```

Siempre que [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) devuelva un valor distinto de cero, la expresión del **bucle while** se evalúa como true. Después de llamar a [**PostQuitMessage,**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)la expresión se convierte en false y el programa se interrumpe del bucle. (Un resultado interesante de este comportamiento es que el procedimiento de ventana nunca recibe un [**mensaje DE SALIDA \_ de WM.**](/windows/desktop/winmsg/wm-quit) Por lo tanto, no es necesario tener una instrucción case para este mensaje en el procedimiento de la ventana).

La siguiente pregunta obvia es cuándo llamar a [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage). Volveremos a esta pregunta en el tema Cerrar la [ventana,](closing-the-window.md)pero primero tenemos que escribir nuestro procedimiento de ventana.

## <a name="posted-messages-versus-sent-messages"></a>Mensajes publicados frente a mensajes enviados

En la sección anterior se ha hablado de los mensajes que van a una cola. A veces, el sistema operativo llamará directamente a un procedimiento de ventana, omitiendo la cola.

La terminología de esta distinción puede ser confusa:

-   *Publicar* un mensaje significa que el mensaje entra en la cola de mensajes y se envía a través del bucle de mensajes ([**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) y [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)).
-   *Enviar* un mensaje significa que el mensaje omite la cola y el sistema operativo llama directamente al procedimiento de ventana.

Por ahora, la diferencia no es muy importante. El procedimiento de ventana controla todos los mensajes. Sin embargo, algunos mensajes omiten la cola y van directamente al procedimiento de la ventana. Sin embargo, puede marcar una diferencia si la aplicación se comunica entre ventanas. Puede encontrar una explicación más exhaustiva de este problema en el tema Acerca de [mensajes y colas de mensajes.](/windows/desktop/winmsg/about-messages-and-message-queues)

## <a name="next"></a>Siguientes

[Escribir el procedimiento de ventana](writing-the-window-procedure.md)
