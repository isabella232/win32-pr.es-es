---
title: Información general sobre guiones gráficos
description: Esta información general se centra en cómo se usan las transiciones y los guiones gráficos en la animación de Windows.
ms.assetid: d37718ac-0256-4a24-a26c-d29173593be0
keywords:
- Animación de Windows animación, información general sobre guiones gráficos
- guiones gráficos animación de Windows, descritos
- Animación de transiciones de Windows, descripción
- Animación de transiciones de Windows, personalizado
- interpoladores animación de Windows, descritos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d8e0af3937cd31ccdc43216a9d3426bad0e7b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792226"
---
# <a name="storyboard-overview"></a>Información general sobre guiones gráficos

Esta información general se centra en cómo se usan las transiciones y los guiones gráficos en la animación de Windows. Para obtener información general sobre los componentes de la animación de Windows, consulte [información general sobre animaciones de Windows](scenic-animation-api-overview.md).

Este tema contiene las siguientes secciones:

-   [Transiciones](#custom-transitions)
    -   [Biblioteca de transición](#transition-library)
    -   [Transiciones personalizadas](#custom-transitions)
-   [Storyboards](#storyboards)
    -   [Crear un guión gráfico simple](#building-a-simple-storyboard)
    -   [Usar una duración de Context-Sensitive](#using-a-context-sensitive-duration)
    -   [Crear un guión gráfico más complejo](#building-a-more-complex-storyboard)
    -   [Usar fotogramas clave](#using-keyframes)
    -   [Almacenar variables](#holding-variables)
    -   [Programar un guion gráfico](#scheduling-a-storyboard)
-   [Temas relacionados](#related-topics)

## <a name="transitions"></a>Transiciones

Una transición define cómo cambia una variable de animación única en un intervalo de tiempo determinado. La animación de Windows incluye una biblioteca de transiciones comunes que los desarrolladores pueden aplicar a una o varias variables de animación. Los distintos tipos de transiciones tienen diferentes conjuntos de parámetros, que pueden incluir el valor de la variable cuando se completa la transición, la duración de la transición o cantidades únicas de la función matemática subyacente, como la aceleración o el intervalo de oscilación.

Todas las transiciones comparten dos parámetros implícitos: el valor inicial y la velocidad inicial (pendiente) de la función matemática. La aplicación puede especificarlos explícitamente, pero el administrador de animaciones los establece normalmente en el valor y la velocidad de la variable de animación cuando comienza la transición.

-   [Biblioteca de transición](#transition-library)
-   [Transiciones personalizadas](#custom-transitions)

### <a name="transition-library"></a>Biblioteca de transición

La biblioteca de transición proporciona actualmente las siguientes transiciones. Si una aplicación requiere un efecto que no se puede especificar mediante la biblioteca de transición, los desarrolladores pueden crear otros tipos de transiciones implementando un interpolador personalizado para la aplicación o usando una biblioteca de transición de un tercero.



| Nombre de la transición                        | Descripción                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| acelere: deceleración<br/>       | La variable de animación se acelera y después se ralentiza a lo largo de una duración determinada.<br/>                                                                                                               |
| constant<br/>                    | La variable de animación permanece en su valor inicial a lo largo de la transición.<br/>                                                                                                            |
| cúbicas<br/>                       | La variable de animación cambia de su valor inicial a un valor final especificado, con una velocidad final especificada, a lo largo de una duración determinada.<br/>                                                 |
| discretos<br/>                    | La variable de animación permanece en su valor inicial durante un tiempo de retraso especificado y, a continuación, cambia de forma instantánea a un valor final especificado y permanece en ese valor durante un tiempo de espera determinado.<br/> |
| instantánea<br/>               | La variable de animación cambia de forma instantánea de su valor actual a un valor final especificado.<br/>                                                                                               |
| linear<br/>                      | La variable de animación realiza la transición lineal de su valor inicial a un valor final especificado durante una determinada duración.<br/>                                                                      |
| lineal desde la velocidad<br/>           | La variable de animación realiza la transición lineal de su valor inicial a un valor final especificado con una velocidad especificada.<br/>                                                                     |
| parabólica de la aceleración<br/> | La variable de animación realiza la transición de su valor inicial a un valor final especificado, con una velocidad final especificada, cambiando su velocidad con una aceleración especificada.<br/>               |
| inversión<br/>                    | La variable cambia la dirección durante una determinada duración. El valor final será el mismo que el valor inicial y la velocidad final será el negativo de la velocidad inicial.<br/>          |
| sinusoidal desde el intervalo<br/>       | La variable oscila dentro de un intervalo determinado de valores, con un período de oscilación especificado, para una duración determinada.<br/>                                                                     |
| sinusoidal desde velocidad<br/>    | La variable oscila con un período de oscilación especificado para una duración determinada. La amplitud de oscilación viene determinada por la velocidad inicial de la variable.<br/>                      |
| detención suave<br/>                 | La variable de animación llega a una parada suave en el valor final especificado, dentro de un período de tiempo máximo.<br/>                                                                              |



 

La tabla siguiente contiene ilustraciones para cada una de estas transiciones.



|                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Ilustración de una transición instantánea](images/instantaneoustransition.png)  ![Ilustración de una transición constante](images/constanttransition.png)  ![Ilustración de una transición lineal](images/lineartransition.png)  ![Ilustración de una transición de lineat desde la velocidad](images/lineartransitionfromspeed.png)  ![Ilustración de una transición discreta](images/discretetransition.png) |
| ![Ilustración de una transición de parabólica desde la aceleración](images/parabolictransitionfromacceleration.png)  ![Ilustración de una transición cúbica](images/cubictransition.png)  ![Ilustración de una transición de detención suave](images/smoothstoptransition.png)                                                                                                                                       |
| ![Ilustración de una transición de inversión](images/reversaltransition.png)  ![Ilustración de una transición sinusoidal de velocidad](images/sinusolidaltransitionfromvelocity.png)  ![Ilustración de una transición sinusoidal desde el intervalo](images/sinusolidaltransitionfromrange.png)                                                                                                                  |
| ![Ilustración de las transiciones Accellerate y Decelerate](images/acceleratedeceleratetransition.png)                                                                                                                                                                                                                                                                                               |



 

### <a name="custom-transitions"></a>Transiciones personalizadas

Un *interpolador* define la función matemática que determina cómo cambia una variable de animación con el tiempo a medida que progresa de su valor inicial a un valor final. Cada transición de la biblioteca de transición tiene un objeto interpolador asociado proporcionado por el sistema e implementa la función interpolator. Si una aplicación requiere un efecto que no se puede especificar mediante la biblioteca de transición, puede implementar una o varias transiciones personalizadas implementando un objeto interpolador para cada nueva transición. Los objetos interpolator no se pueden usar directamente en las aplicaciones y, en su lugar, se deben encapsular en una transición asociada. Un *generador de transición* se utiliza para generar transiciones desde un objeto interpolador. Consulte [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) y [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory) para obtener más información.

Tenga en cuenta que la mayoría de las aplicaciones tendrán todas las transiciones que necesitan mediante la biblioteca de transición y, por consiguiente, no tendrían que implementar un interpolador.

## <a name="storyboards"></a>Storyboards

Un guion gráfico es una colección de transiciones que se aplican a una o varias variables de animación a lo largo del tiempo. Se garantiza que las transiciones de un guión gráfico permanecen sincronizadas entre sí, y el guión gráfico se programa o se cancela como una unidad. Después de crear las transiciones deseadas, una aplicación crea un guion gráfico mediante el administrador de animaciones, agrega las transiciones al guion gráfico, configura el guión gráfico de forma adecuada y lo programa para que se reproduzca lo antes posible. El administrador de animaciones determina la hora de inicio real del guión gráfico, ya que puede haber contención con otros guiones gráficos animando actualmente las mismas variables.

La duración total de un guión gráfico depende de las duraciones de las transiciones dentro del guion gráfico. No es necesario corregir la duración de una transición; se puede determinar mediante el valor y la velocidad de las variables animadas cuando comienza la transición. Por lo tanto, la duración de un guión gráfico también puede depender del estado de las variables que anima.

En los ejemplos siguientes se supone que se han creado un administrador de animaciones, una biblioteca de transición y un temporizador. Para obtener más información, vea [crear los objetos de animación principales](adding-animation-to-an-application.md). Los ejemplos también suponen que la aplicación ha creado tres variables de animación (X, Y y Z) mediante el método [**IUIAnimationManager:: CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) y cinco transiciones (T1, T2, T3, T4 y T5) mediante el uso de uno de los métodos de la interfaz [**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary) .

-   [Crear un guión gráfico simple](#building-a-simple-storyboard)
-   [Usar una duración de Context-Sensitive](#using-a-context-sensitive-duration)
-   [Crear un guión gráfico más complejo](#building-a-more-complex-storyboard)
-   [Usar fotogramas clave](#using-keyframes)
-   [Almacenar variables](#holding-variables)
-   [Programar un guion gráfico](#scheduling-a-storyboard)

### <a name="building-a-simple-storyboard"></a>Crear un guión gráfico simple

Para compilar un guion gráfico simple, use el método [**IUIAnimationManager:: CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) para crear un nuevo guion gráfico, el método [**IUIAnimationTransitionLibrary:: CreateLinearTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition) para crear una transición lineal, T1 y el método [**IUIAnimationStoryboard:: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) para aplicar la transición T1 a la variable X y agregar la transición resultante al guion gráfico.

Este proceso produce un guion gráfico simple, como se muestra en la ilustración siguiente. El guión gráfico contiene una transición, T1, de modo que el valor de la variable X cambia de forma lineal durante un período de tiempo fijo.

![Ilustración que muestra un guión gráfico simple con una duración fija](images/simplestoryboardfixedduration.png)

Tenga en cuenta que para este escenario sencillo, una opción alternativa es usar el método [**IUIAnimationManager:: ScheduleTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-scheduletransition) .

### <a name="using-a-context-sensitive-duration"></a>Usar una duración de Context-Sensitive

Aunque algunas transiciones tienen una duración fija, la duración de otras depende del valor inicial o la velocidad de la variable animada cuando comienza la transición. Por ejemplo, el método [**IUIAnimationTransitionLibrary:: CreateLinearTransitionFromSpeed**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed) crea una transición con una duración proporcional a la diferencia entre el valor inicial de la variable de animación y el valor final especificado. En esta ilustración, y las ilustraciones restantes, tales transiciones con duraciones arbitrarias se muestran con un signo de interrogación (?) y sus duraciones reales se determinan cuando se reproduce el guion gráfico.

![Ilustración en la que se muestra un guión gráfico simple con una duración desconocida](images/simplestoryboardunknownduration.png)

### <a name="building-a-more-complex-storyboard"></a>Crear un guión gráfico más complejo

Después de crear un guion gráfico y agregar una sola transición, T1, puede anexar una segunda transición para la variable X llamando de nuevo al método [**IUIAnimationStoryboard:: AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) , pero con T2 en lugar de T1.

Suponiendo que la transición T2 tiene una duración que es contextual, el guión gráfico ahora contiene dos transiciones inversas de duración arbitraria que afectan a la variable X.

![Ilustración que muestra un guion gráfico que contiene dos transiciones en la misma variable](images/appendingwithaddtransition.png)

Al llamar a [**AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) de nuevo con la variable y y la transición T3, se agrega una tercera transición al inicio del guion gráfico. Dependiendo de los valores de X e y cuando se reproduzca el guión gráfico, T3 puede finalizar después de T1 o incluso después de T2.

![Ilustración en la que se muestra un guion gráfico que contiene transiciones entre varias variables](images/multivariablestoryboard.png)

### <a name="using-keyframes"></a>Usar fotogramas clave

Para agregar una transición en un desplazamiento desde el inicio del guion gráfico, primero debe agregar un fotograma clave. Los fotogramas clave representan instantáneas en el tiempo y, por sí mismos, no tienen ningún efecto en el comportamiento del guion gráfico. Cada guión gráfico tiene un fotograma clave implícito que representa el inicio del guion gráfico, el [**\_ \_ \_ guión gráfico \_ del fotograma clave de la interfaz de usuario comienza**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85)); puede agregar nuevos fotogramas clave a los desplazamientos desde el principio llamando al método [**IUIAnimationStoryboard:: AddKeyframeAtOffset**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset) con el **\_ \_ guión gráfico de fotogramas clave \_ \_ de la interfaz de usuario Inicio**.

El desplazamiento en el que se agrega un fotograma clave siempre es relativo a otro fotograma clave. En el diagrama siguiente se muestra el resultado de agregar keyframe1 y la transición T4, que se aplica a la variable Z, alineada con keyframe1, y se crea con una duración fija. Por supuesto, dado que las duraciones de las otras transiciones todavía no se conocen, T4 podría no ser la última transición para finalizar.

![Ilustración que muestra la adición de una transición alineada en un fotograma clave](images/addtransitionatkeyframe.png)

Los fotogramas clave también se pueden colocar en los extremos de las transiciones mediante el método [**IUIAnimationStoryboard:: AddKeyframeAfterTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition) . En el diagrama siguiente se muestra el resultado de agregar keyframe2 después de T1 y keyframe3 después de T2.

![Ilustración en la que se muestra la adición de fotogramas clave después de varias transiciones](images/addkeyframeaftertransition.png)

Dado que no se conocen las duraciones T1 y T2 hasta que se reproduce el guión gráfico, los desplazamientos de keyframe2 y keyframe3 tampoco se determinan hasta entonces. Por consiguiente, keyframe2 e incluso keyframe3 pueden producirse antes de keyframe1.

Tanto el inicio como el final de una transición se pueden alinear con fotogramas clave mediante el método [**IUIAnimationStoryboard:: AddTransitionBetweenKeyframes**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes) . En el diagrama siguiente se muestra el resultado de agregar una quinta transición, T5, en la variable Y, entre keyframe2 y keyframe3. Esto modifica la duración de T5, lo que es mayor o menor en función de los desplazamientos relativos de keyframe2 y keyframe3.

![Ilustración que muestra además de una transición entre fotogramas clave](images/addtransitionbetweenkeyframes.png)

### <a name="holding-variables"></a>Almacenar variables

Si T4 termina después de T2 y T5, el guion gráfico deja de animar las variables X e y, de forma que estén disponibles para que otros guiones gráficos puedan animarse. Sin embargo, la aplicación puede llamar al método [**IUIAnimationStoryboard:: HoldVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-holdvariable) para solicitar que el guion gráfico contenga algunas o todas las variables que anima en sus valores finales hasta que se haya completado el guión gráfico. En el diagrama siguiente se muestra el resultado de mantener X y Z cuando T4 finaliza en último lugar. Observe que el guión gráfico contiene X en su valor final hasta que se haya completado el guión gráfico. La suspensión no tiene ningún efecto en Z porque el guión gráfico finaliza cuando se completa T4.

![Ilustración en la que se muestra la retención de variables en valores finales hasta que se completa el guión gráfico](images/holdvariable.png)

Aunque Y no se retienen en este guión gráfico, su valor no cambia después de que se complete T5 a menos que otro guion gráfico lo anime. Dado que no se mantiene Y, cualquier otro guión gráfico, independientemente de la prioridad, puede animar Y después de que haya finalizado T5. Por el contrario, dado que se mantiene X, un guión gráfico de menor prioridad no puede animar X hasta que finalice este guión gráfico.

Todas estas ilustraciones han asumido un conjunto arbitrario de valores actuales para las variables cuando se inicia la reproducción del guión gráfico. Si se encuentran otros valores, es probable que las duraciones de las transiciones contextuales sean diferentes, como se muestra en la siguiente ilustración.

![Ilustración que muestra el resultado de cambiar las condiciones iniciales utilizadas para la ilustración anterior](images/holdvariablez.png)

En este escenario, T5 comienza antes de que T3 finalice y, por tanto, T3 se recorta. Dado que T4 finaliza antes de T2 y T5, el valor de Z se mantiene hasta el final del guión gráfico. En general, los valores y las velocidades de las variables cuando se inicia la reproducción de un guion gráfico pueden afectar al orden de los fotogramas clave y a la longitud y la forma generales del guión gráfico.

### <a name="scheduling-a-storyboard"></a>Programar un guion gráfico

Al programar un guion gráfico, su hora de inicio se determina mediante su esquema y los contornos de los guiones gráficos que están actualmente en la programación. En concreto, el primer y el último momento en que el guion gráfico anima cada variable individual determinan si dos guiones gráficos están en conflicto, pero los detalles internos de las transiciones en no son importantes.

En la ilustración siguiente se muestra el contorno de un guión gráfico con cinco transiciones que animan tres variables.

![Ilustración en la que se muestra un guión gráfico con cinco transiciones animando tres variables](images/storyboardwithoutline.png)

Una piedra angular de la plataforma de animación de Windows es su compatibilidad para permitir que una animación se complete antes de que comience otra, cuando sea necesario. Aunque esto elimina muchos problemas lógicos, también introduce una latencia arbitraria en la interfaz de usuario. Para solucionar esto, las aplicaciones pueden especificar el *retraso aceptable más largo* para que se inicie un guion gráfico, mediante el método [**IUIAnimationStoryboard:: SetLongestAcceptableDelay**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay) , y el administrador de animaciones usa esta información para programar el guión gráfico antes de que transcurra el período de latencia especificado. Cuando se programa un guion gráfico, el administrador de animaciones determina si otros guiones gráficos se deben cancelar primero, recortar, concluir o comprimir.

Una aplicación puede registrar un controlador que se llamará cuando cambie el estado de un guión gráfico. Esto permite a la aplicación responder cuando se inicia la reproducción del guion gráfico, se ejecuta hasta su finalización, se quita completamente de la programación o se evita que se complete debido a la interrupción de un guión gráfico de prioridad superior. Para identificar los guiones gráficos que se pasan a los controladores de eventos de guiones gráficos (o comparaciones de prioridad), una aplicación puede usar el método [**IUIAnimationStoryboard:: SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-settag) para aplicar etiquetas a guiones gráficos, similares a los que se pueden usar para identificar variables. Al igual que con la reutilización de guiones gráficos, los desarrolladores deben tener cuidado al usar etiquetas para identificar guiones gráficos y asegurarse de que no surjan ambigüedades cuando las acciones del usuario dan lugar a la puesta en cola de muchos guiones gráficos.

En los siguientes ejemplos se muestran dos variaciones de un intento de programar el guion gráfico creado en las secciones anteriores de este tema.

En este escenario, los seis guiones gráficos, de la a a la F, ya se han programado para animar las variables W, X, y y Z, pero solo A y B han empezado a reproducirse. El nuevo guión gráfico, con la etiqueta G, tiene el retraso aceptable más largo establecido en la duración que se muestra en la ilustración siguiente.

![Ilustración que muestra la adición de un nuevo guión gráfico a la programación existente](images/existingschedule1withlines.png)

La aplicación tiene comparaciones de prioridad registradas que incluyen la lógica siguiente:

-   G solo puede cancelar C y E, y solo para evitar errores.
-   G solo puede recortar a, C, E y F, y solo para evitar errores.
-   Cualquier guion gráfico puede comprimir cualquier otro guión gráfico (la compresión siempre se realiza solo para evitar errores).

> [!Note]  
> El calificador "solo para evitar errores" significa que las comparaciones de prioridad registradas devuelven S \_ solo cuando el parámetro *priorityEffect* es **\_ \_ \_ \_ un error de efecto de prioridad de animación de IU**. Vea el método [**IUIAnimationPriorityComparison:: HasPriority**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationprioritycomparison-haspriority) para obtener más información.

 

Para iniciar G antes de que haya transcurrido el retraso aceptable más largo, el administrador de animaciones debe hacer lo siguiente:

-   Trim F
-   Cancelar E

Cuando se cancela E, D y F se descubrirán y volverán a su esquema original:

![Ilustración que muestra los contornos originales](images/existingschedule1bwithlines.png)

No es necesario que el administrador de animaciones cancele o recorte C para programar antes de que haya transcurrido el retraso más largo aceptable, por lo que la reunión de C y G determina cuándo se inicia G.

![Ilustración en la que se muestra que f se ha recortado para permitir que c y g cumplan](images/schedule1withgwithlines.png)

Una vez que G se ha programado correctamente, se pueden determinar las duraciones de las transiciones y, por lo tanto, se conoce el resto del esquema. Sin embargo, el esquema puede cambiar si se quita otro guión gráfico de la programación.

Como segundo ejemplo, considere un escenario como el anterior, pero con un retraso más corto que se haya especificado para G.

![Ilustración en la que se muestra el escenario anterior, pero con un retraso aceptable más corto para g](images/existingschedule2withlines.png)

En este caso, se realizan las siguientes acciones:

-   Trim F
-   Cancelar E
-   Cancelar C

Además, el administrador de animaciones debe comprimir D por la cantidad que se muestra para permitir que G se inicie después de su retraso más largo aceptable, y no más tarde.

![Ilustración donde d debe comprimirse para permitir que g se inicie en su retraso aceptable más largo](images/trimmedandcancelledwithlines.png)

Para conservar el tiempo relativo, también se comprimen los A, B y F.

![Ilustración que muestra un, b, d y f comprimidos](images/schedule2withgwithlines.png)

Sin embargo, los guiones gráficos de variables no relacionadas (no mostradas) no se comprimirán.

Una vez más, ahora se conoce el esquema de G y es diferente del resultado en el primer escenario, ya que las variables tienen valores diferentes cuando se inicia G.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationPriorityComparison**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)
</dt> <dt>

[**IUIAnimationStoryboard**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> </dl>

 

