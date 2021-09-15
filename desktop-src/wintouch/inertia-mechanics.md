---
title: Mecanismos de inercia
description: Mecanismos de inercia
ms.assetid: 188b6936-b36e-4e57-9118-8b61ed134c17
keywords:
- Windows Táctil, inercia
- Windows Animación táctil y suave
- Windows Táctil, margen elástico
- inercia, mecánica
- inercia, conceptos básicos de cálculo
- inercia, introducción a la física
- inercia, animación suave
- inercia, margen elástico
- animación suave
- margen elástico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79b27900c6921c972710e7e922ab42b834afc1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466229"
---
# <a name="inertia-mechanics"></a>Mecanismos de inercia

La inercia se usa para realizar cálculos para animar el movimiento de objetos y para habilitar la compatibilidad con la facilidad de uso genérica en aplicaciones que incorporan Windows Touch. En esta sección se muestran las siguientes características habilitadas por la inercia.

-   Breve introducción a la física de inercia.
-   Animación de objetos smooth mediante las propiedades de velocidad y deceleración.
-   Animación de objetos smooth mediante una propiedad de desplazamiento.
-   Saltar de los bordes de la pantalla mediante límites elásticos.

## <a name="inertia-physics-overview"></a>Introducción a la física de inercia

El procesador de inercia usa un modelo físico simple que incorpora una posición, un valor de deceleración y una velocidad inicial. La hora se usa como entrada dinámica en el modelo para determinar la posición actual de un objeto que se desplaza. El gráfico y la fórmula siguientes describen el modelo físico utilizado para calcular las posiciones de los objetos.

![ilustración que muestra el gráfico y la fórmula usados para calcular las posiciones de objeto](images/velocity.png)

En la fórmula usada para calcular la posición actual (x), la velocidad inicial (v) se multiplica por el tiempo transcurrido (t) y se reduce por el factor de deceleración (d) veces el tiempo al cuadrado. Esto da como resultado una aceleración de objetos sin problemas. En la ilustración anterior en la parte inicial (más a la izquierda) de la curva, el objeto se mueve rápidamente porque su velocidad actual es la velocidad inicial. En la parte final (más a la derecha) de la curva, el objeto se ha detenido completamente porque su velocidad es 0. Los cálculos de velocidad de objetos para la velocidad X, la velocidad Y y la velocidad de rotación usan esta fórmula para los cálculos.

Toda la distancia usada para el procesador de inercia es relativa. Si desea usar coordenadas de pantalla, pase las coordenadas de pantalla al procesador de manipulación (o inercia); Si desea usar coordenadas absolutas, las pasa al procesador que está usando. Independientemente de los valores que use, el procesador de manipulación usará tics de reloj de milisegundos para procesar la hora. Estos valores se pueden pasar directamente al procesador de inercia mediante el método [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) o mediante la marca de tiempo predeterminada a través de llamadas a [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process).

## <a name="smooth-object-animation-using-the-velocity-and-deceleration-properties"></a>Animación de objetos smooth mediante las propiedades de velocidad y deceleración

Puede habilitar la animación fluida si interactúa directamente con el modelo físico estableciendo los valores de velocidad y deceleración en la interfaz del procesador de inercia y, a continuación, llamando a [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process). El proceso **de llamada** desencadenará manipulaciones de objetos que, a su vez, deberían provocar actualizaciones de la interfaz de usuario. Los valores de velocidad de objetos pasados al procesador de inercia normalmente se toman del procesador de manipulación tras la finalización. El valor de la deceleración dependerá de cuánto tiempo quiera animar el objeto y de las unidades que use para los cálculos. Dado que los valores son dependientes, a veces debe escalar la velocidad de entrada desde el procesador de maniplation y usar valores arbitrarios para la deceleración. Los valores siguientes son típicos para varios escenarios en los que se pasan valores centipixel de las propiedades x e y de la [**estructura TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) al procesador de manipulación.



| Escenario    | Conjunto de propiedades                                                                       | Valor de deceleración | Escalado de entrada de velocidad típico                                  | Notas                                                                                 |
|-------------|------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| Traducción | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,003f             | Ninguno.                                                           | El uso de este valor dará como resultado animaciones de distancia más larga al usar la entrada táctil.    |
| Traducción | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,001f             | Velocidad inicial 1/20 para las entradas táctiles, ninguna para las entradas del mouse | El uso de este valor animará para aproximadamente un segundo dadas entradas de velocidad típicas.      |
| Traducción | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,5f               | None                                                            | El uso de este valor proporciona una sensación natural a la animación en pantallas Windows táctil.   |
| Rotación    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0,000015f          | Radianes convertidos en grados.                                   | El uso de este valor da como resultado animaciones de rotación más largas cuando se usa la entrada táctil.      |
| Rotación    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0,00001f           | Delta de rotación 1/40 para entradas táctiles, ninguna para las entradas del mouse   | Este valor está en radianes, por lo que debe usar valores de velocidad y deceleración muy pequeños. |
| Rotación    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0,000005f          | None                                                            | Este valor tiene una sensación natural en pantallas táctiles Windows pantallas táctiles.                        |



 

## <a name="smooth-object-animation-using-the-desired-displacement-property"></a>Animación de objetos smooth mediante la propiedad De desplazamiento deseado

En algunos casos, no quiere usar la entrada del usuario para el desplazamiento de objetos, pero sigue deseando que un objeto se animara sin problemas a través de la pantalla. En este caso, puede usar propiedades de desplazamiento en el procesador de inercia para que el procesador calcule la velocidad inicial para mover un objeto a través de la pantalla.

## <a name="controlling-object-position-using-elastic-bounds"></a>Controlar la posición del objeto mediante límites elásticos

Después de tener un objeto que se mueve por la pantalla, normalmente querrá que se detenga antes de que salga del punto de vista del usuario. El procesador de inercia habilita esta funcionalidad a través de las propiedades de límite y margen elástico. En la imagen siguiente se muestran las distintas propiedades de límite y margen en una aplicación típica.

![Captura de pantalla que muestra las propiedades de límite y margen elástico](images/elastic-illustrated.png)

Establezca los límites izquierdo, superior, derecho e inferior y los márgenes elásticos de la aplicación, y el procesador de inercia controlará el mantenimiento de los elementos de la interfaz de usuario dentro de los límites. Cuando un objeto alcanza un margen elástico, se ralentizará hasta que alcance el límite. Nunca volverá a dejar ese margen durante la inercia, pero se moverá hasta que el componente de inercia del objeto se desacelera a 0. En la ilustración, un círculo se desplaza hacia el límite elástico izquierdo. La flecha sólida muestra la dirección de la manipulación; el círculo sólido es la posición inicial del objeto; la flecha sólida son los cambios realizados antes de que el círculo llegue al margen elástico; la flecha discontinua muestra dónde manipula el procesador de inercia el círculo después de que alcanza el margen; y los círculos discontinuos muestran dónde se detiene el objeto.

> [!Note]  
> Al establecer las propiedades del margen, los límites se moverán hacia fuera. Por ejemplo, si el límite superior está establecido en 50 y, a continuación, establece el margen elástico superior en 10, el límite superior se convertirá de hecho en 40.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de la inercia en código no administrado](handling-inertia-in-unmanaged-code.md)
</dt> <dt>

[Inercia](getting-started-with-inertia.md)
</dt> <dt>

[Manipulaciones](getting-started-with-manipulations.md)
</dt> </dl>

 

 




