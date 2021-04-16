---
title: Animación (DirectComposition)
description: En este tema se describen los conceptos básicos de la animación DirectComposition de Microsoft.
ms.assetid: 65DA3971-97C0-4B59-BC67-287AAEAAE340
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7462a10fd83b45c1b90450fdde806ef306a2f6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105685820"
---
# <a name="animation-directcomposition"></a>Animación (DirectComposition)

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describen los conceptos básicos de la animación DirectComposition de Microsoft. Incluye los temas siguientes:

-   [¿Qué es una animación?](#what-is-an-animation)
-   [Propiedades que se pueden animar](#properties-that-can-be-animated)
-   [Funciones de animación](#animation-functions)
-   [Segmentos de animación](#animation-segments)
    -   [Segmento cúbico](#cubic-segment)
    -   [Segmento sinusoidal](#sinusoidal-segment)
    -   [Repetir segmento](#repeat-segment)
    -   [Fin del segmento](#end-segment)
-   [Compatibilidad con el administrador de animaciones de Windows](#compatibility-with-windows-animation-manager)
-   [Temas relacionados](#related-topics)

## <a name="what-is-an-animation"></a>¿Qué es una animación?

La *animación* es un efecto óptico que se crea mediante la realización rápida de cambios incrementales en un visual durante un período de tiempo mientras se redibuja el visual después de realizar cada cambio. Dado que los redibujos se producen rápidamente, el cerebro percibe los cambios incrementales como una sola escena cambiante, al igual que en una película o vídeo de acción en directo.

En la tabla siguiente se describen algunas de las formas típicas de usar la animación.

| Animación                 | Descripción                                                                                                                                                                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Desplazamiento                 | Use la animación para agregar características como el momento de emulación física a un control de lista de desplazamiento.                                                                                                                                                           |
| Transiciones de escena         | Use la animación para crear transiciones de escena de navegación que proporcionen continuidad entre las tareas de un flujo de trabajo. Las transiciones de escena de navegación proporcionan contexto que muestra el usuario en el que se encontraban, dónde están y dónde deben ir a continuación. |
| Interacciones entre ventanas | Animar elementos de interfaz de usuario de diferentes aplicaciones de forma que ofrezca una continuidad sin problemas entre ellos para ayudar al usuario a completar tareas que impliquen el cambio de una aplicación a otra.                                         |



 

## <a name="properties-that-can-be-animated"></a>Propiedades que se pueden animar

En DirectComposition, se anima un objeto visual aplicando animación a las propiedades individuales de los objetos que definen el objeto visual. Por ejemplo, si desea desplace un visual horizontalmente por la pantalla, aplicaría la animación a la propiedad OffsetX del visual. Del mismo modo, si desea realizar una rotación 2D animada simple de un objeto visual, aplicaría la animación a la propiedad Angle de un objeto de transformación 2D y, a continuación, aplicaría el objeto de transformación 2D a la propiedad transform del objeto visual.

DirectComposition permite aplicar animaciones a cualquier propiedad de objeto que toma un valor escalar. Puede aplicar animaciones simultáneas a varias propiedades y a varios objetos.

DirectComposition ejecuta animaciones en un subproceso independiente. Puede iniciar una animación o un conjunto de animaciones y luego realizar otro trabajo en los subprocesos de la aplicación, o incluso poner los subprocesos en suspensión, mientras que el motor de composición ejecuta las animaciones con la velocidad de fotogramas adecuada.

## <a name="animation-functions"></a>Funciones de animación

DirectComposition anima una propiedad de objeto basándose en una función de animación que defina. Una *función de animación* es una construcción que especifica cómo cambia el valor de una propiedad de objeto en un período de tiempo. Por ejemplo, podría definir una función de animación que cambia el valor de una propiedad de 1 a 360 en el transcurso de 4 segundos. A continuación, si se aplica la función de animación a la propiedad Angle de un objeto de transformación de giro 2D y, a continuación, se aplica el objeto de transformación a la propiedad de transformación de un objeto visual, la función de animación rotará el objeto visual en un círculo completo en el transcurso de 4 segundos.

Una función de animación se representa mediante un *objeto Animation* creado por una llamada al método [**IDCompositionDevice:: CreateAnimation**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createanimation) . Puede crear una función de animación mediante los métodos de la interfaz [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) de un objeto Animation para anexar *segmentos de animación*, de uno en uno, a la matriz que define la función de animación. Al anexar un segmento, se especifica un desplazamiento de base cero que marca la hora de inicio del segmento con respecto al principio de la función de animación. Los segmentos de animación deben agregarse en orden ascendente de horas de inicio. Se producirá un error al intentar anexar un segmento de animación cuya hora de inicio sea anterior o igual a un segmento anterior. Una función de animación puede tener una hora de finalización especificada, que indica cuándo debe concluir la función.

A menos que se especifique lo contrario, se inicia una función de animación cuando el Administrador de ventanas de escritorio (DWM) recibe el comando para ejecutar la animación. Cada segmento se ejecuta hasta que se alcanza la hora de inicio del segmento siguiente. Los cambios descontinuos que se producen en el valor de propiedad animada entre segmentos se consideran cambios discretos.

Para aplicar una función de animación a una propiedad, establezca el valor de la propiedad en el puntero [**IDCompositionAnimation**](/windows/desktop/api/DcompAnimation/nn-dcompanimation-idcompositionanimation) del objeto Animation que representa la función de animación. Se puede aplicar el mismo objeto de animación a varias propiedades del mismo objeto, así como a las propiedades de otros objetos creados por el mismo dispositivo.

## <a name="animation-segments"></a>Segmentos de animación

Los segmentos de animación son las definiciones de tiempo fundamentales de una función de animación. son los primitivos de los que se compilan funciones de animación más complejas y de nivel superior. Un segmento de animación se construye a partir de una serie de parámetros que describen la función y la hora a la que comienza el segmento, con respecto al principio de la función de animación. Para cada segmento, el tiempo (*t*) progresa a lo largo del eje horizontal y comienza en *t* = 0.

### <a name="cubic-segment"></a>Segmento cúbico

La temporización de un segmento cúbico se define mediante una polinómica cúbica. Para una entrada de hora determinada (*t*), el valor de salida se proporciona mediante la siguiente ecuación:

*x*(*t*) = *at*³ + *BT*² + *CT*  +  *d*

En el diagrama siguiente se muestra una función de animación que contiene dos segmentos cúbicos. El primer segmento realiza la transición de un valor de 0 a 16 en 4 segundos y el segundo cambia el valor linealmente de 16 a 0 en los próximos 4 segundos. La primera transición se produce a lo largo de este polinomio cúbico:

*x*(*t*) = *t*³-6 *t*² + 12 *t*

y la segunda transición se produce a lo largo de esta:

*x*(*t*) =-4 *t* + 16

![diagrama de una función de animación con dos segmentos cúbicos](images/cubicsegment.png)

Puede Agregar un segmento cúbico a una función de animación mediante el método [**IDCompositionAnimation:: AddCubic**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addcubic) .

### <a name="sinusoidal-segment"></a>Segmento sinusoidal

La duración de un segmento sinusoidal se define mediante la siguiente ecuación:

*x*(*t*) = amplitud de *Bias*  +   \* sin (frecuencia de *t* \*  \* 2 \* PI + *fase* \* PI/180.0)

Puede Agregar un segmento sinusoidal a una función de animación mediante el método [**IDCompositionAnimation:: AddSinusoidal**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addsinusoidal) .

### <a name="repeat-segment"></a>Repetir segmento

Un segmento de repetición repite la parte anterior especificada de una función de animación. Un segmento de repetición hace que la parte especificada de la función de animación se repita indefinidamente hasta que se encuentre el segmento siguiente o hasta que se alcance el final de la animación. La parte anterior de una animación se realiza en otros segmentos, incluidos otros segmentos de repetición. No se puede usar un segmento de repetición como primer segmento en una función de animación.

En el diagrama siguiente se muestra una función de animación que consta de dos segmentos cúbicos de una duración de 4 segundos cada uno, seguido de un segmento de repetición que dura 12 segundos. El segmento de repetición comienza 8 segundos en la animación y repite los 6 segundos anteriores de la animación dos veces hasta que se alcanza el segmento final en 20 segundos.

![diagrama de una función de animación que contiene dos segmentos cúbicos y un segmento de repetición](images/repeatsegment.png)

Para agregar un segmento de repetición a una función de animación, use el método [**IDCompositionAnimation:: AddRepeat**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-addrepeat) .

### <a name="end-segment"></a>Fin del segmento

Después de crear una función de animación a partir de segmentos, puede anexar un segmento final para que la función de animación finalice en un momento determinado. Si no anexa un segmento final, el segmento final de la función de animación se ejecuta indefinidamente.

Para anexar un segmento final, llame al método [**IDCompositionAnimation:: end**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end) y especifique un desplazamiento desde el principio de la función de animación que indica el punto final de la función. El desplazamiento debe ser mayor que el desplazamiento inicial del segmento anterior. Además, no se puede usar un segmento final como el primer primitivo en una función de animación.

Cuando se llama a [**End**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-end), también se especifica un valor final para la propiedad que se anima. La propiedad se establece en el valor final especificado en el momento en que se alcanza el punto final de la función de animación.

Después de anexar un segmento final, no se pueden anexar otros segmentos a la función de animación. Es decir, se produce un error en todas las llamadas a métodos en el objeto Animation excepto [**IDCompositionAnimation:: RESET**](/windows/desktop/api/DcompAnimation/nf-dcompanimation-idcompositionanimation-reset). La llamada a **RESET** devuelve el objeto Animation al estado Clean en el que la función Animation no contiene segmentos, momento en el que puede Agregar segmentos de nuevo.

## <a name="compatibility-with-windows-animation-manager"></a>Compatibilidad con el administrador de animaciones de Windows

El administrador de animaciones de Windows (animación de Windows) genera primitivas de animación en un formato compatible con la API de DirectComposition. Esto significa que DirectComposition puede crear animaciones basadas en primitivas de animación creadas por la animación de Windows.

Para obtener más información, vea [Administrador de animaciones de Windows](/windows/desktop/UIAnimation/-main-portal), el método [**IUIAnimationVariable2:: GetCurve**](/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve) y [administrar la animación DirectComposition con el administrador de animaciones de Windows V2](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 
