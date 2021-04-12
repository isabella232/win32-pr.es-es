---
title: Mecánica de inercia
description: Mecánica de inercia
ms.assetid: 188b6936-b36e-4e57-9118-8b61ed134c17
keywords:
- Windows Touch, inercia
- Windows Touch, suave animaciones
- Windows Touch, margen elástico
- inercia, mecánica
- inercia, conceptos básicos de cálculo
- inercia, información general sobre la física
- inercia, Smooth Animation
- inercia, margen elástico
- animación suave
- margen elástico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79b27900c6921c972710e7e922ab42b834afc1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356844"
---
# <a name="inertia-mechanics"></a>Mecánica de inercia

La inercia se usa para realizar cálculos con el fin de animar el movimiento de objetos y habilitar la compatibilidad con la utilización genérica en aplicaciones que incorporan Windows Touch. En esta sección se muestran las siguientes características que están habilitadas por inercia.

-   Información general breve sobre la física de inercia.
-   Animar el objeto Smooth usando las propiedades de velocidad y desaceleración.
-   Animación de objeto Smooth usando una propiedad de desplazamiento.
-   Rebotar desde los bordes de la pantalla mediante límites elásticos.

## <a name="inertia-physics-overview"></a>Información general física de inercia

El procesador de inercia usa un modelo físico simple que incorpora una posición, un valor de desaceleración y una velocidad inicial. Time se usa como entrada dinámica al modelo para determinar la posición actual de un objeto que se está desplazando. El gráfico y la fórmula siguientes describen el modelo físico usado para calcular las posiciones de los objetos.

![Ilustración que muestra el gráfico y la fórmula que se usan para calcular posiciones de objeto](images/velocity.png)

En la fórmula que se usa para calcular la posición actual (x), la velocidad inicial (v) se multiplica por el tiempo transcurrido (t) y se reduce por el factor de desaceleración (d) veces al cuadrado. Esto produce una desaceleración de objeto suave. En la ilustración anterior en la parte inicial (izquierda) de la curva, el objeto se mueve rápidamente porque su velocidad actual es la velocidad inicial. En la parte final (derecha) de la curva, el objeto se ha detenido por completo porque su velocidad es 0. Los cálculos de velocidad de objetos para la velocidad x, la velocidad y y la velocidad de rotación usan esta fórmula para los cálculos.

Toda la distancia utilizada para el procesador de inercia es relativa. Si desea utilizar coordenadas de pantalla, pase las coordenadas de pantalla al procesador de manipulación (o inercia); Si desea utilizar coordenadas absolutas, puede transferirlas al procesador que está utilizando. Independientemente de los valores que use, el procesador de manipulación usará TICs de reloj de milisegundos para procesar la hora. Estos valores se pueden pasar directamente al procesador de inercia mediante el método [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) o el uso de la marca de tiempo predeterminada a través de las llamadas a [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process).

## <a name="smooth-object-animation-using-the-velocity-and-deceleration-properties"></a>Animar la animación de objetos mediante las propiedades de velocidad y desaceleración

Puede habilitar la animación suave interactuando directamente con el modelo físico estableciendo los valores de velocidad y desaceleración en la interfaz del procesador de inercia y después llamando al [**proceso**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process). El **proceso** de llamada desencadenará manipulaciones de objetos que, a su vez, deben producir actualizaciones de la interfaz de usuario. Los valores de velocidad de objeto que se pasan al procesador de inercia se suelen tomar del procesador de manipulación al finalizar. El valor de desaceleración dependerá del tiempo que quiera que se anime el objeto y de las unidades que esté usando para los cálculos. Dado que los valores son dependientes, a veces debe escalar la velocidad de entrada desde el procesador maniplation y usar valores arbitrarios para la desaceleración. Los valores siguientes son típicos para varios escenarios en los que se pasan los valores de centipixel de las propiedades x e y de la estructura [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) al procesador de manipulación.



| Escenario    | Conjunto de propiedades                                                                       | Valor de desaceleración | Escala de entrada de velocidad típica                                  | Notas                                                                                 |
|-------------|------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| Traducción | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,003 f             | Ninguno.                                                           | Si se usa este valor, se producirán animaciones de distancia más largas al usar la entrada táctil.    |
| Traducción | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,001 f             | 1/20 velocidad inicial para entradas táctiles, ninguna para entradas de mouse | El uso de este valor se animará en torno a una segunda entrada de velocidad típica dada.      |
| Traducción | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0.5 f               | None                                                            | El uso de este valor da una sensación natural a la animación en pantallas grandes de Windows Touch.   |
| Rotación    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000015 f          | Radianes convertidos en grados.                                   | El uso de este valor produce animaciones de rotación más largas cuando se usa la entrada táctil.      |
| Rotación    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0,00001 f           | 1/40th de rotación para entradas táctiles, ninguna para entradas de mouse   | Este valor se encuentra en radianes, por lo que debe usar valores de desaceleración muy pequeños y de velocidad. |
| Rotación    | [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000005 f          | None                                                            | Este valor tiene una sensación natural en pantallas grandes de Windows Touch.                        |



 

## <a name="smooth-object-animation-using-the-desired-displacement-property"></a>Animación de objeto Smooth con la propiedad de desplazamiento deseada

En algunos casos, no desea usar la entrada del usuario para el desplazamiento de objetos, pero desea que un objeto se anime sin problemas en la pantalla. En este caso, puede usar las propiedades de desplazamiento en el procesador de inercia para que el procesador calcule la velocidad inicial para mover un objeto a través de la pantalla.

## <a name="controlling-object-position-using-elastic-bounds"></a>Controlar la posición de un objeto mediante límites elásticos

Una vez que tenga un objeto que se mueva por la pantalla, normalmente querrá que se detenga antes de que salga del punto de vista del usuario. El procesador de inercia permite esta funcionalidad a través de las propiedades límite y margen elástico. En la imagen siguiente se muestran las diversas propiedades de límite y margen en una aplicación típica.

![captura de pantalla que muestra las propiedades de margen y límite elástico](images/elastic-illustrated.png)

Los límites izquierdo, superior, derecho e inferior se establecen para la aplicación, y el procesador de inercia controlará el mantenimiento de los elementos de la interfaz de usuario dentro de los límites. Cuando un objeto alcanza un margen elástico, se ralentiza hasta que alcanza el límite. Nunca dejará ese margen de nuevo durante la inercia, sino que se seguirá moviendo hasta que el componente de inercia perpendicular del objeto disminuya a 0. En la ilustración, un círculo se desplazará hacia el límite elástico izquierdo. La flecha sólida muestra la dirección de la manipulación; el círculo sólido es la posición inicial del objeto; la flecha sólida es el cambio que se realiza antes de que el círculo llegue al margen elástico. la Flecha discontinua muestra dónde el procesador de inercia manipula el círculo una vez que alcanza el margen; y los círculos discontinuos muestran dónde se detiene el objeto.

> [!Note]  
> Al establecer las propiedades de margen, se mueven los límites hacia afuera. Por ejemplo, si el límite superior se establece en 50 y, a continuación, establece el margen elástico superior en 10, el límite superior se convertirá en 40 de forma efectiva.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controlar la inercia en código no administrado](handling-inertia-in-unmanaged-code.md)
</dt> <dt>

[Inercia](getting-started-with-inertia.md)
</dt> <dt>

[Manipulaciones](getting-started-with-manipulations.md)
</dt> </dl>

 

 




