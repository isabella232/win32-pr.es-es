---
title: Acerca de los controles Up-Down
description: Un control de flechas es un par de botones de flecha en los que el usuario puede hacer clic para aumentar o disminuir un valor, como una posición de desplazamiento o un número mostrado en un control complementario (denominado ventana relacionada).
ms.assetid: ae2c0283-9cad-40d1-b8a6-a90484a95f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc8dad15a8254b138cae4175cc16b1ef3111745
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794086"
---
# <a name="about-up-down-controls"></a>Acerca de los controles Up-Down

Un control de flechas es un par de botones de flecha en los que el usuario puede hacer clic para aumentar o disminuir un valor, como una posición de desplazamiento o un número mostrado en un control complementario (denominado ventana relacionada).

Para el usuario, un control de flechas y su ventana relacionada suelen tener el mismo control. Puede especificar que un control de flechas se coloque automáticamente junto a su ventana relacionada y que establezca automáticamente la leyenda de la ventana relacionada en su posición actual. Por ejemplo, puede utilizar un control de flechas con un control de edición para solicitar al usuario una entrada numérica. En la ilustración siguiente se muestra un control de flechas con un control de edición como su ventana relacionada, una combinación a la que a veces se hace referencia como control de número.

![captura de pantalla que muestra un control rectangular corto y ancho con flechas arriba y abajo en el borde derecho](images/updown.jpg)

Los temas siguientes se describen en esta sección.

-   [Estilos de control de flechas](#up-down-control-styles)
-   [Posición y aceleración](#position-and-acceleration)
-   [El Up-Down predeterminado controla el procesamiento de mensajes](#default-up-down-controls-message-processing)

## <a name="up-down-control-styles"></a>Estilos de control de Up-Down

Mediante el uso de estilos de ventana, puede manipular las características de un control de flechas, como la forma en que se coloca en relación con su ventana relacionada, tanto si establece el texto de su ventana relacionada como si procesa las teclas de flecha arriba y flecha abajo.

Un control de flechas con el estilo [**uds \_ ALIGNLEFT**](up-down-control-styles.md) o [**uds \_ ALIGNRIGHT**](up-down-control-styles.md) se alinea con el borde izquierdo o derecho de su ventana relacionada. El ancho de la ventana relacionada se reduce para acomodar el ancho del control de flechas.

Un control de flechas con el estilo [**uds \_ SETBUDDYINT**](up-down-control-styles.md) establece el título de su ventana relacionada cada vez que cambia la posición actual. El control inserta un separador de miles entre cada tres dígitos de una cadena decimal a menos que se especifique el estilo [**uds \_ nomiles**](up-down-control-styles.md) . Si la ventana relacionada es un cuadro de lista, un control de flechas establece su selección actual en lugar de su título.

Puede especificar el estilo [**uds \_ ARROWKEYS**](up-down-control-styles.md) para proporcionar una interfaz de teclado para un control de flechas. Si se especifica este estilo, el control procesa las teclas de dirección arriba y abajo. El control también subclase la ventana relacionada para que pueda procesar estas claves cuando la ventana relacionada tenga el foco.

Si usa un control de flechas para el desplazamiento horizontal, puede especificar el estilo [**uds \_ horizontal**](up-down-control-styles.md) . Este estilo hace que las flechas del control de flechas señalen hacia la izquierda y hacia la derecha en lugar de hacia arriba y hacia abajo.

De forma predeterminada, la posición actual no cambia si el usuario intenta incrementarlo o disminuirlo más allá del valor máximo o mínimo. Puede cambiar este comportamiento mediante el estilo de [**\_ ajuste uds**](up-down-control-styles.md) , de modo que la posición "se ajusta" al extremo opuesto. Por ejemplo, el incremento más allá del límite superior ajusta la posición de nuevo al límite inferior.

## <a name="position-and-acceleration"></a>Posición y aceleración

Después de crear un control de flechas, puede cambiar la posición actual, la posición mínima y la posición máxima del control mediante el envío de mensajes. También puede cambiar la base de base que se usa para mostrar la posición actual en la ventana relacionada y la velocidad a la que cambia la posición actual cuando se hace clic en la flecha arriba o abajo.

Para recuperar la posición actual de un control de flechas, use el mensaje [**\_ GETPOS UDM**](udm-getpos.md) . En el caso de un control de flechas con una ventana relacionada, la posición actual es el número en el título de la ventana relacionada. Dado que el título puede haber cambiado (por ejemplo, el usuario puede haber editado el texto de un control de edición), el control de flechas recupera el título actual y actualiza su posición actual según corresponda.

El título de la ventana del contacto puede ser una cadena decimal o hexadecimal, dependiendo de la base de base (es decir, base 10 o 16) del control de flechas. Puede establecer la base de base mediante el mensaje [**UDM \_ SETBASE**](udm-setbase.md) y recuperar la base de base mediante el mensaje [**\_ GETBASE de UDM**](udm-getbase.md) .

El mensaje [**UDM \_ SETPOS**](udm-setpos.md) establece la posición actual de una ventana relacionada. Tenga en cuenta que, a diferencia de una barra de desplazamiento, un control de flechas cambia automáticamente su posición actual cuando se hace clic en las flechas arriba y abajo. Por lo tanto, una aplicación no necesita establecer la posición actual al procesar el mensaje de [**WM \_ VSCROLL**](wm-vscroll.md) o [**WM \_ HSCROLL**](wm-hscroll.md) .

Puede cambiar las posiciones mínima y máxima de un control de flechas mediante el mensaje de [**\_ SetRange UDM**](udm-setrange.md) . La posición máxima puede ser menor que el mínimo y, en ese caso, al hacer clic en el botón de flecha arriba, se reduce la posición actual. Para colocarlo de otro modo, subir significa moverse hacia la posición máxima. Para recuperar las posiciones mínima y máxima de un control de flechas, use el mensaje [**\_ GETRANGE UDM**](udm-getrange.md) .

Puede controlar la velocidad a la que cambia la posición cuando el usuario mantiene presionado un botón de flecha estableciendo la aceleración del control de flechas. La aceleración se define mediante una matriz de estructuras [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) . Cada estructura especifica un intervalo de tiempo y el número de unidades que se incrementan o disminuyen al final de ese intervalo. Para establecer la aceleración, use el [**mensaje \_ SETACCEL UDM**](udm-setaccel.md) . Para recuperar la información de aceleración, use el mensaje [**\_ GETACCEL UDM**](udm-getaccel.md) .

## <a name="default-up-down-controls-message-processing"></a>El Up-Down predeterminado controla el procesamiento de mensajes

En esta sección se describen los mensajes de Windows estándar procesados por un control de flechas.



| Message                                        | Procesamiento realizado                                                                                                                                                                                         |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**creación de WM \_**](/windows/desktop/winmsg/wm-create)             | Asigna e inicializa una estructura de datos privada y guarda su dirección como datos de ventana.                                                                                                                     |
| [**destrucción de WM \_**](/windows/desktop/winmsg/wm-destroy)           | Libera los datos asignados durante el procesamiento de la [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) .                                                                                                                                   |
| [**\_habilitación de WM**](/windows/desktop/winmsg/wm-enable)             | Invalida la ventana.                                                                                                                                                                                      |
| [**KEYDOWN de WM \_**](/windows/desktop/inputdev/wm-keydown)         | Cambia la posición actual en el caso de una tecla de flecha arriba o flecha abajo.                                                                                                                                   |
| [**KEYUP de WM \_**](/windows/desktop/inputdev/wm-keyup)             | Completa el cambio de posición.                                                                                                                                                                               |
| [**LBUTTONDOWN de WM \_**](/windows/desktop/inputdev/wm-lbuttondown) | Captura el mouse. Si la ventana relacionada es un control de edición o un cuadro de lista, establece el foco en la ventana relacionada. Si el mouse está encima del botón arriba o abajo, comienza a cambiar la posición y establece un temporizador. |
| [**LBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-lbuttonup)     | Completa el cambio de posición y libera la captura del mouse si el control de flechas ha capturado el mouse. Si la ventana relacionada es un control de edición, selecciona todo el texto del control de edición.             |
| [**pintura de WM \_**](/windows/desktop/gdi/wm-paint)                  | Dibuja el control de flechas. Si el parámetro *wParam* no es null, el control supone que el valor es **HDC** y pinta usando ese contexto de dispositivo.                                                    |
| [**temporizador de WM \_**](/windows/desktop/winmsg/wm-timer)               | Cambia la posición actual si se mantiene el mouse sobre un botón y ha transcurrido un intervalo suficiente.                                                                                            |



 

 

 