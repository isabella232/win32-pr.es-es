---
title: Acerca de Up-Down controles
description: Un control de flecha arriba es un par de botones de flecha en los que el usuario puede hacer clic para incrementar o disminuir un valor, como una posición de desplazamiento o un número que se muestra en un control complementario (denominado ventana de compañeros).
ms.assetid: ae2c0283-9cad-40d1-b8a6-a90484a95f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 749014a4b9959b8afd6e769919a0dc9df19e99ce4edeabca774e535f26f4cf8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132165"
---
# <a name="about-up-down-controls"></a>Acerca de Up-Down controles

Un control de flecha arriba es un par de botones de flecha en los que el usuario puede hacer clic para incrementar o disminuir un valor, como una posición de desplazamiento o un número que se muestra en un control complementario (denominado ventana de compañeros).

Para el usuario, un control hacia arriba y su ventana de compañeros a menudo parecen un control único. Puede especificar que un control de flecha hacia abajo se coloque automáticamente junto a su ventana de compañeros y que establezca automáticamente el título de la ventana del compañero en su posición actual. Por ejemplo, puede usar un control de arriba a abajo con un control de edición para solicitar al usuario una entrada numérica. En la ilustración siguiente se muestra un control de flechas con un control de edición como ventana de unión, una combinación que a veces se conoce como control de número.

![captura de pantalla que muestra un control rectangular corto y ancho con flechas arriba y abajo en el borde derecho](images/updown.jpg)

En esta sección se tratan los temas siguientes.

-   [Estilos de control hacia abajo](#up-down-control-styles)
-   [Posición y aceleración](#position-and-acceleration)
-   [Control predeterminado Up-Down el procesamiento de mensajes](#default-up-down-controls-message-processing)

## <a name="up-down-control-styles"></a>Up-Down estilos de control

Con los estilos de ventana, puede manipular las características de un control de flecha arriba, como cómo se coloca en relación con su ventana de compañeros, si establece el texto de su ventana de compañeros y si procesa las teclas FLECHA ARRIBA y FLECHA ABAJO.

Un control hacia abajo con el estilo [**\_ ALIGNLEFT**](up-down-control-styles.md) o [**UDS \_ ALIGNRIGHT**](up-down-control-styles.md) se alinea con el borde izquierdo o derecho de la ventana del compañero. El ancho de la ventana del compañero se reduce para dar cabida al ancho del control de arriba a abajo.

Un control hacia arriba con el estilo [**\_ SETBUDDYINT de UDS**](up-down-control-styles.md) establece el título de su ventana de compañeros cada vez que cambia la posición actual. El control inserta un separador de miles entre cada tres dígitos de una cadena decimal, a menos que se especifique el estilo [**\_ NOTHOUSANDS**](up-down-control-styles.md) de UDS. Si la ventana del compañero es un cuadro de lista, un control hacia abajo establece su selección actual en lugar de su título.

Puede especificar el estilo [**\_ ARROWKEYS de UDS**](up-down-control-styles.md) para proporcionar una interfaz de teclado para un control de flecha hacia abajo. Si se especifica este estilo, el control procesa las teclas de dirección arriba y abajo. El control también subclases la ventana del compañero para que pueda procesar estas claves cuando la ventana del compañero tiene el foco.

Si usa un control de flecha hacia abajo para el desplazamiento horizontal, puede especificar el estilo [**\_ HORZ de UDS.**](up-down-control-styles.md) Este estilo hace que las flechas del control de flechas hacia abajo apunten a la izquierda y a la derecha en lugar de hacia arriba y hacia abajo.

De forma predeterminada, la posición actual no cambia si el usuario intenta incrementarla o disminuirla más allá del valor máximo o mínimo. Puede cambiar este comportamiento mediante el estilo [**DE \_ ENCAPSULADO de UDS,**](up-down-control-styles.md) por lo que la posición se "ajusta" al extremo opuesto. Por ejemplo, si se incrementa más allá del límite superior, se vuelve a ajustar la posición al límite inferior.

## <a name="position-and-acceleration"></a>Posición y aceleración

Después de crear un control de flechas, puede cambiar la posición actual, la posición mínima y la posición máxima del control mediante el envío de mensajes. También puede cambiar la base de base radix utilizada para mostrar la posición actual en la ventana del compañero y la velocidad a la que cambia la posición actual cuando se hace clic en la flecha arriba o abajo.

Para recuperar la posición actual de un control de arriba a abajo, use el [**mensaje \_ UDM GETPOS.**](udm-getpos.md) Para un control de arriba hacia abajo con una ventana de compañeros, la posición actual es el número en el título de la ventana del compañero. Dado que el título puede haber cambiado (por ejemplo, el usuario puede haber editado el texto de un control de edición), el control de flechas recupera el título actual y actualiza su posición actual en consecuencia.

El título de la ventana del compañero puede ser una cadena decimal o hexadecimal, dependiendo de la base de base (es decir, base 10 o 16) del control de arriba a abajo. Puede establecer la base de base mediante el mensaje [**UDM \_ SETBASE**](udm-setbase.md) y recuperar la base de base mediante el mensaje [**\_ UDM GETBASE.**](udm-getbase.md)

El [**mensaje UDM \_ SETPOS**](udm-setpos.md) establece la posición actual de una ventana de compañeros. Tenga en cuenta que, a diferencia de una barra de desplazamiento, un control hacia abajo cambia automáticamente su posición actual cuando se hace clic en las flechas arriba y abajo. Por lo tanto, una aplicación no necesita establecer la posición actual al procesar el mensaje [**\_ WM VSCROLL**](wm-vscroll.md) o [**WM \_ HSCROLL.**](wm-hscroll.md)

Puede cambiar las posiciones mínima y máxima de un control de flecha hacia abajo mediante el mensaje [**\_ SETRANGE de UDM.**](udm-setrange.md) La posición máxima puede ser menor que la mínima y, en ese caso, al hacer clic en el botón de flecha arriba se reduce la posición actual. Para ponerlo de otro modo, subir significa moverse hacia la posición máxima. Para recuperar las posiciones mínima y máxima de un control de flechas, use el mensaje [**\_ UDM GETRANGE.**](udm-getrange.md)

Puede controlar la velocidad a la que cambia la posición cuando el usuario mantiene presionado un botón de flecha estableciendo la aceleración del control de flecha hacia abajo. La aceleración se define mediante una matriz [**de estructuras UDACCEL.**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) Cada estructura especifica un intervalo de tiempo y el número de unidades por las que incrementar o disminuir al final de ese intervalo. Para establecer la aceleración, use el [**mensaje \_ SETACCEL de UDM.**](udm-setaccel.md) Para recuperar información de aceleración, use el [**mensaje \_ GETACCEL de UDM.**](udm-getaccel.md)

## <a name="default-up-down-controls-message-processing"></a>Procesamiento de mensajes Up-Down controles predeterminados

En esta sección se describe el Windows los mensajes procesados por un control de flechas.



| Message                                        | Procesamiento realizado                                                                                                                                                                                         |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create)             | Asigna e inicializa una estructura de datos privada y guarda su dirección como datos de ventana.                                                                                                                     |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)           | Libera los datos asignados durante el [**procesamiento de WM \_ CREATE.**](/windows/desktop/winmsg/wm-create)                                                                                                                                   |
| [**WM \_ ENABLE**](/windows/desktop/winmsg/wm-enable)             | Invalida la ventana.                                                                                                                                                                                      |
| [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)         | Cambia la posición actual en el caso de una tecla FLECHA ARRIBA o FLECHA ABAJO.                                                                                                                                   |
| [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)             | Completa el cambio de posición.                                                                                                                                                                               |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) | Captura el mouse. Si la ventana del compañero es un control de edición o un cuadro de lista, establece el foco en la ventana del compañero. Si el mouse está sobre el botón arriba o abajo, comienza a cambiar la posición y establece un temporizador. |
| [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup)     | Completa el cambio de posición y libera la captura del mouse si el control de arriba hacia abajo ha capturado el mouse. Si la ventana del compañero es un control de edición, selecciona todo el texto del control de edición.             |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)                  | Pinta el control de arriba a abajo. Si el *parámetro wParam* no es NULL, el control supone que el valor es un **HDC** y pinta con ese contexto de dispositivo.                                                    |
| [**TEMPORIZADOR \_ WM**](/windows/desktop/winmsg/wm-timer)               | Cambia la posición actual si se mantiene el mouse sobre un botón y ha transcurrido un intervalo suficiente.                                                                                            |



 

 

 