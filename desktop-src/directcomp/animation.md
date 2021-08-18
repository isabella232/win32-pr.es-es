---
title: Animación (DirectComposition)
description: En este tema se de abordan los conceptos básicos de la animación de Microsoft DirectComposition.
ms.assetid: 65DA3971-97C0-4B59-BC67-287AAEAAE340
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b1f021d5a11fac70f47d5fe87f9389d2ad3e3108d224835fb295a8c3216354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119143"
---
# <a name="animation-directcomposition"></a>Animación (DirectComposition)

> [!NOTE]
> Para las aplicaciones Windows 10, se recomienda usar Windows.UI.Composition API en lugar de DirectComposition. Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se de abordan los conceptos básicos de la animación de Microsoft DirectComposition. Incluye los temas siguientes:

-   [¿Qué es una animación?](#what-is-an-animation)
-   [Propiedades que se pueden animar](#properties-that-can-be-animated)
-   [Funciones de animación](#animation-functions)
-   [Segmentos de animación](#animation-segments)
    -   [Segmento cúbica](#cubic-segment)
    -   [Segmento sinusoidal](#sinusoidal-segment)
    -   [Repetir segmento](#repeat-segment)
    -   [Segmento final](#end-segment)
-   [Compatibilidad con Windows Animation Manager](#compatibility-with-windows-animation-manager)
-   [Temas relacionados](#related-topics)

## <a name="what-is-an-animation"></a>¿Qué es una animación?

*La* animación es una esperanza óptica creada al realizar rápidamente cambios incrementales en un objeto visual durante un período de tiempo mientras se vuelve a dibujar el objeto visual después de realizar cada cambio. Dado que los redraws se producen rápidamente, el cerebro percibe los cambios incrementales como una sola escena cambiante, igual que en una película o vídeo de acción en directo.

En la tabla siguiente se describen algunas de las formas típicas de usar la animación.

| Animación                 | Descripción                                                                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Desplazamiento                 | Use la animación para agregar características como el impulso de emulación física a un control de lista de desplazamiento.                                                                                                                                                           |
| Transiciones de escena         | Use la animación para crear transiciones de escena de navegación que proporcionen continuidad entre las tareas de un flujo de trabajo. Las transiciones de la escena de navegación proporcionan contexto que muestra al usuario dónde ha estado, dónde está y dónde debe ir a continuación. |
| Interacciones entre ventanas | Animar elementos de interfaz de usuario de diferentes aplicaciones de forma que se dé la percepción de una continuidad sin problemas entre ellos para ayudar al usuario a completar tareas que implican el cambio de una aplicación a otra.                                         |



 

## <a name="properties-that-can-be-animated"></a>Propiedades que se pueden animar

En DirectComposition, se anima un objeto visual aplicando animación a propiedades individuales de los objetos que definen el objeto visual. Por ejemplo, si desea mover un objeto visual horizontalmente a través de la pantalla, aplicaría animación a la propiedad OffsetX del objeto visual. De forma similar, si quisiera realizar una rotación 2D animada simple de un objeto visual, aplicaría animación a la propiedad Ángulo de un objeto de transformación 2D y, a continuación, aplicaría el objeto de transformación 2D a la propiedad Transform del objeto visual.

DirectComposition permite aplicar animación a cualquier propiedad de objeto que toma un valor escalar. Puede aplicar animaciones simultáneas a varias propiedades y varios objetos.

DirectComposition ejecuta animaciones en un subproceso independiente. Puede iniciar una animación o un conjunto de animaciones y, a continuación, realizar otro trabajo en los subprocesos de aplicación, o incluso poner subprocesos en modo de suspensión, mientras el motor de composición ejecuta las animaciones a la velocidad de fotogramas adecuada.

## <a name="animation-functions"></a>Funciones de animación

DirectComposition anima una propiedad de objeto basada en una función de animación que defina. Una *función de* animación es una construcción que especifica cómo cambia el valor de una propiedad de objeto durante un período de tiempo. Por ejemplo, podría definir una función de animación que cambie el valor de una propiedad de 1 a 360 en el transcurso de 4 segundos. A continuación, si aplica la función de animación a la propiedad Angle de un objeto de transformación de rotación 2D y, a continuación, aplica el objeto de transformación a la propiedad Transform de un objeto visual, la función de animación giraría el objeto visual en un círculo completo en el transcurso de 4 segundos.

Una función de animación se representa mediante un *objeto de animación* creado por una llamada al método [**IDCompositionDevice::CreateAnimation.**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) Para crear una función de animación, use los métodos de la interfaz [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) de un objeto de animación para anexar segmentos de animación *,* de uno en uno, a la matriz que define la función de animación. Al anexar un segmento, se especifica un desplazamiento de base cero que marca la hora de inicio del segmento, con respecto al principio de la función de animación. Los segmentos de animación se deben anexar en orden creciente de las horas de inicio. Se producirá un error al intentar anexar un segmento de animación cuya hora de inicio sea anterior o igual a un segmento anterior. Una función de animación puede tener una hora de finalización especificada, lo que indica cuándo debe concluir la función.

A menos que se especifique lo contrario, se inicia una función de animación Administrador de ventanas de escritorio (DWM) recibe el comando para ejecutar la animación. Cada segmento se ejecuta hasta que se alcanza la hora de inicio del siguiente segmento. Los cambios discontinuos que se producen en el valor de propiedad animado entre segmentos se consideran cambios discretos.

Para aplicar una función de animación a una propiedad, se establece el valor de propiedad en el puntero [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) del objeto de animación que representa la función de animación. El mismo objeto de animación se puede aplicar a varias propiedades del mismo objeto, así como a las propiedades de otros objetos creados por el mismo dispositivo.

## <a name="animation-segments"></a>Segmentos de animación

Los segmentos de animación son las definiciones de control de tiempo fundamentales de una función de animación; son los primitivos a partir de los cuales se construyen funciones de animación más complejas y de nivel superior. Un segmento de animación se construye a partir de una serie de parámetros que describen la función y la hora en que comienza el segmento, con respecto al principio de la función de animación. Para cada segmento, el tiempo (*t*) progresa a lo largo del eje horizontal y comienza *en t* = 0.

### <a name="cubic-segment"></a>Segmento cúbica

El intervalo de un segmento cúbica se define mediante un polinómico cúbica. Para una entrada de hora determinada (*t*), el valor de salida se da mediante la ecuación siguiente:

*x*(*t*) = *at*« + *bt*« + *ct*  +  *d* )

En el diagrama siguiente se muestra una función de animación que contiene dos segmentos cúbicas. El primer segmento pasa un valor de 0 a 16 durante 4 segundos y el segundo cambia linealmente el valor de 16 a 0 durante los próximos 4 segundos. La primera transición se produce a lo largo de este polinómico cúbica:

*x*(*t*) = *t* además de 6 *t* además de 12 *t*

y la segunda transición se produce a lo largo de esta:

*x*(*t*) = - 4 *t* + 16

![diagrama de una función de animación con dos segmentos cúbicas](images/cubicsegment.png)

Agregue un segmento cúbico a una función de animación mediante el [**método IDCompositionAnimation::AddCubic.**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic)

### <a name="sinusoidal-segment"></a>Segmento sinusoidal

La ecuación siguiente define el tiempo de un segmento sinusoidal:

*x*(*t*) = *Bias*  +  *Amplitude* \* sin(*t* \* *Frequency* \* 2 PI + \* *Phase* \* PI/180.0)

Agregue un segmento sinusoidal a una función de animación mediante el método [**IDCompositionAnimation::AddSinusoidal.**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal)

### <a name="repeat-segment"></a>Repetir segmento

Un segmento de repetición repite una parte anterior especificada de una función de animación. Un segmento de repetición hace que la parte especificada de la función de animación se bucle indefinidamente hasta que se encuentra el segmento siguiente o se alcanza el final especificado de la animación. La parte anterior de una animación está hecho de otros segmentos, incluidos otros segmentos de repetición. No se puede usar un segmento de repetición como primer segmento de una función de animación.

En el diagrama siguiente se muestra una función de animación que consta de dos segmentos cúbicas de 4 segundos de duración cada uno, seguidos de un segmento de repetición que dura 12 segundos. El segmento de repetición comienza 8 segundos en la animación y repite los 6 segundos anteriores de la animación dos veces hasta que el segmento final se alcanza en 20 segundos.

![diagrama de una función de animación que contiene dos segmentos cúbicas y un segmento de repetición](images/repeatsegment.png)

Para agregar un segmento de repetición a una función de animación, use el [**método IDCompositionAnimation::AddRepeat.**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat)

### <a name="end-segment"></a>Segmento final

Después de construir una función de animación a partir de segmentos, puede anexar un segmento final para que la función de animación finalice en un momento determinado. Si no anexa un segmento final, el segmento final de la función de animación se ejecuta indefinidamente.

Para anexar un segmento final, llame al método [**IDCompositionAnimation::End,**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) especificando un desplazamiento desde el principio de la función de animación que indica el punto final de la función. El desplazamiento debe ser mayor que el desplazamiento inicial del segmento anterior. Además, no se puede usar un segmento final como primer primitivo en una función de animación.

Al llamar a [**End**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end), también se especifica un valor final para la propiedad que se anima. La propiedad se establece en el valor final especificado en el momento en que se alcanza el punto final de la función de animación.

Después de anexar un segmento final, no puede anexar ningún otro segmento a la función de animación. Es decir, se producirá un error en todas las llamadas de método en el objeto de animación excepto [**IDCompositionAnimation::Reset**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset). Al llamar **a Reset** se devuelve el objeto de animación a un estado limpio en el que la función de animación no contiene segmentos, momento en el que se pueden agregar segmentos de nuevo.

## <a name="compatibility-with-windows-animation-manager"></a>Compatibilidad con Windows Animation Manager

Windows Animation Manager (Windows Animation) genera primitivas de animación en un formato compatible con DirectComposition API. Esto significa que DirectComposition puede crear animaciones basadas en primitivas de animación creadas por Windows Animation.

Para obtener más información, vea [Windows Animation Manager](/windows/desktop/UIAnimation/-main-portal), el método [**IUIAnimationVariable2::GetCurve**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) y [Managing DirectComposition Animation with Windows Animation Manager v2](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
