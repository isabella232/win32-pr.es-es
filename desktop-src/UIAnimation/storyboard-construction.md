---
title: Información general sobre guiones gráficos
description: Esta información general se centra en cómo se usan las transiciones y los guiones gráficos en Windows animación.
ms.assetid: d37718ac-0256-4a24-a26c-d29173593be0
keywords:
- Windows Animation Windows Animation ,storyboard overview
- storyboards Windows Animation ,described
- transitions Windows Animation ,described
- transiciones Windows animation ,custom
- interpoladores Windows animación , descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58210ae98f6d3a96c554276466ad72b3364d72a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242127"
---
# <a name="storyboard-overview"></a>Información general sobre guiones gráficos

Esta información general se centra en cómo se usan las transiciones y los guiones gráficos en Windows animación. Para obtener información general sobre los componentes de Windows Animation, vea Windows Información general [sobre animaciones.](scenic-animation-api-overview.md)

Este tema contiene las siguientes secciones:

-   [Transiciones](#custom-transitions)
    -   [Biblioteca de transición](#transition-library)
    -   [Transiciones personalizadas](#custom-transitions)
-   [Storyboards](#storyboards)
    -   [Creación de un guión gráfico simple](#building-a-simple-storyboard)
    -   [Usar una duración Context-Sensitive datos](#using-a-context-sensitive-duration)
    -   [Creación de un guión gráfico más complejo](#building-a-more-complex-storyboard)
    -   [Uso de fotogramas clave](#using-keyframes)
    -   [Mantener variables](#holding-variables)
    -   [Programar un guión gráfico](#scheduling-a-storyboard)
-   [Temas relacionados](#related-topics)

## <a name="transitions"></a>Transiciones

Una transición define cómo cambia una única variable de animación durante un intervalo de tiempo determinado. Windows La animación incluye una biblioteca de transiciones comunes que los desarrolladores pueden aplicar a una o varias variables de animación. Los distintos tipos de transiciones tienen diferentes conjuntos de parámetros, que pueden incluir el valor de la variable cuando se completa la transición, la duración de la transición o cantidades únicas para la función matemática subyacente, como la aceleración o el intervalo de oscilación.

Todas las transiciones comparten dos parámetros implícitos: el valor inicial y la velocidad inicial (pendiente) de la función matemática. La aplicación puede especificar estos valores explícitamente, pero normalmente lo establece el administrador de animaciones en el valor y la velocidad de la variable de animación cuando comienza la transición.

-   [Biblioteca de transición](#transition-library)
-   [Transiciones personalizadas](#custom-transitions)

### <a name="transition-library"></a>Biblioteca de transición

La biblioteca de transición proporciona actualmente las siguientes transiciones. Si una aplicación requiere un efecto que no se puede especificar mediante la biblioteca de transición, los desarrolladores pueden crear otros tipos de transiciones implementando un interpolador personalizado para la aplicación o usando una biblioteca de transición desde un tercero.



| Nombre de la transición                        | Descripción                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| acelerar y ralentizar<br/>       | La variable de animación se acelera y, a continuación, se ralentiza durante una duración determinada.<br/>                                                                                                               |
| constant<br/>                    | La variable de animación permanece en su valor inicial a lo largo de la transición.<br/>                                                                                                            |
| cúbicas<br/>                       | La variable de animación cambia de su valor inicial a un valor final especificado, con una velocidad final especificada, durante una duración determinada.<br/>                                                 |
| Discreta<br/>                    | La variable de animación permanece en su valor inicial durante un tiempo de retraso especificado y, a continuación, cambia instantáneamente a un valor final especificado y permanece en ese valor durante un tiempo de retención determinado.<br/> |
| Instantánea<br/>               | La variable de animación cambia al instante de su valor actual a un valor final especificado.<br/>                                                                                               |
| linear<br/>                      | La variable de animación pasa linealmente de su valor inicial a un valor final especificado durante una duración determinada.<br/>                                                                      |
| lineal desde la velocidad<br/>           | La variable de animación pasa linealmente de su valor inicial a un valor final especificado con una velocidad especificada.<br/>                                                                     |
| parabólica a partir de la aceleración<br/> | La variable de animación pasa de su valor inicial a un valor final especificado, con una velocidad final especificada, cambiando su velocidad con una aceleración especificada.<br/>               |
| Revocación<br/>                    | La variable cambia de dirección durante una duración determinada. El valor final será el mismo que el valor inicial y la velocidad final será la negativa de la velocidad inicial.<br/>          |
| sinusoidal desde el intervalo<br/>       | La variable oscila dentro de un intervalo determinado de valores, con un período de oscilación especificado, durante una duración determinada.<br/>                                                                     |
| sinusoidal a partir de la velocidad<br/>    | La variable oscila con un período de oscilación especificado, durante una duración determinada. La amplitud de oscilación viene determinada por la velocidad inicial de la variable.<br/>                      |
| smooth stop<br/>                 | La variable de animación se detiene sin problemas en un valor final especificado, dentro de una duración máxima de tiempo.<br/>                                                                              |



 

La tabla siguiente contiene ilustraciones para cada una de estas transiciones.



|    Ilustraciones                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![ilustración de una transición instantánea](images/instantaneoustransition.png)  ![ilustración de una transición constante](images/constanttransition.png)  ![ilustración de una transición lineal](images/lineartransition.png)  ![ilustración de una transición de lineat desde la velocidad](images/lineartransitionfromspeed.png)  ![ilustración de una transición discreta](images/discretetransition.png) |
| ![ilustración de una transición parabólica desde la aceleración](images/parabolictransitionfromacceleration.png)  ![ilustración de una transición cúbica](images/cubictransition.png)  ![ilustración de una transición de detenerse sin problemas](images/smoothstoptransition.png)                                                                                                                                       |
| ![ilustración de una transición de inversión](images/reversaltransition.png)  ![ilustración de una transición sinusoidal desde la velocidad](images/sinusolidaltransitionfromvelocity.png)  ![ilustración de una transición sinusoidal desde el intervalo](images/sinusolidaltransitionfromrange.png)                                                                                                                  |
| ![ilustración de transiciones de aceleración y deceleración](images/acceleratedeceleratetransition.png)                                                                                                                                                                                                                                                                                               |



 

### <a name="custom-transitions"></a>Transiciones personalizadas

Un *interpolador define* la función matemática que determina cómo cambia una variable de animación con el tiempo a medida que progresa de su valor inicial a un valor final. Cada transición de la biblioteca de transición tiene un objeto interpolador asociado proporcionado por el sistema e implementa la función de interpolador. Si una aplicación requiere un efecto que no se puede especificar mediante la biblioteca de transición, puede implementar una o varias transiciones personalizadas implementando un objeto interpolador para cada nueva transición. Las aplicaciones no pueden usar objetos interpoladores directamente y, en su lugar, deben ajustarse en una transición asociada. Se *usa un generador* de transición para generar transiciones desde un objeto interpolador. Consulte [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) e [**IUIAnimationTransitionFactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory) para obtener más detalles.

Tenga en cuenta que la mayoría de las aplicaciones tendrán todas las transiciones que necesitan mediante la biblioteca de transición y, por tanto, no tendrían que implementar un interpolador.

## <a name="storyboards"></a>Storyboards

Un guión gráfico es una colección de transiciones aplicadas a una o varias variables de animación a lo largo del tiempo. Se garantiza que las transiciones de un guión gráfico permanecen sincronizadas entre sí y que el guión gráfico se programa o cancela como una unidad. Después de crear las transiciones deseadas, una aplicación crea un guión gráfico mediante el administrador de animaciones, agrega las transiciones al guión gráfico, configura el guión gráfico correctamente y lo programa para reproducirlo lo antes posible. El administrador de animaciones determina la hora de inicio real del guión gráfico, ya que puede haber contención con otros guiones gráficos que animan actualmente las mismas variables.

La duración general de un guión gráfico depende de las duraciones de las transiciones dentro del guión gráfico. No es necesario solucionar la duración de una transición; puede determinarse por el valor y la velocidad de las variables animadas cuando comienza la transición. Por lo tanto, la duración de un guión gráfico también puede depender del estado de las variables que anima.

En los ejemplos siguientes se supone que se han creado un administrador de animaciones, una biblioteca de transición y un temporizador. Para obtener más información, vea [Crear los objetos de animación principales](adding-animation-to-an-application.md). En los ejemplos también se supone que la aplicación ha creado tres variables de animación (X, Y y Z) mediante el método [**IUIAnimationManager::CreateAnimationVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) y cinco transiciones (T1, T2, T3, T4 y T5) mediante el uso de uno de los métodos de la interfaz [**IUIAnimationTransitionLibrary.**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)

-   [Creación de un guión gráfico simple](#building-a-simple-storyboard)
-   [Usar una duración Context-Sensitive datos](#using-a-context-sensitive-duration)
-   [Creación de un guión gráfico más complejo](#building-a-more-complex-storyboard)
-   [Uso de fotogramas clave](#using-keyframes)
-   [Mantener variables](#holding-variables)
-   [Programar un guión gráfico](#scheduling-a-storyboard)

### <a name="building-a-simple-storyboard"></a>Creación de un guión gráfico simple

Para crear un guión gráfico simple, use el método [**IUIAnimationManager::CreateStoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) para crear un guión gráfico nuevo, el método [**IUIAnimationTransitionLibrary::CreateLinearTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition) para crear una transición lineal, T1 y el método [**IUIAnimationStoryboard::AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) para aplicar la transición T1 a la variable X y agregar la transición resultante al guión gráfico.

Este proceso produce un guión gráfico simple, como se muestra en la ilustración siguiente. El guión gráfico contiene una transición, T1, de modo que el valor de la variable X cambia linealmente durante un período de tiempo fijo.

![ilustración que muestra un guión gráfico simple con una duración fija](images/simplestoryboardfixedduration.png)

Tenga en cuenta que, para un escenario tan sencillo, una opción alternativa es usar el [**método IUIAnimationManager::ScheduleTransition.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-scheduletransition)

### <a name="using-a-context-sensitive-duration"></a>Uso de una Context-Sensitive duración

Aunque algunas transiciones tienen una duración fija, la duración de otras depende del valor inicial o la velocidad de la variable animada cuando comienza la transición. Por ejemplo, el método [**IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed) crea una transición con una duración proporcional a la diferencia entre el valor inicial de la variable de animación y el valor final especificado. En esta ilustración, y las ilustraciones restantes, estas transiciones con duraciones arbitrarias se muestran con un signo de interrogación (?) y sus duraciones reales se determinan cuando se reproduce el guión gráfico.

![ilustración que muestra un guión gráfico simple con una duración desconocida](images/simplestoryboardunknownduration.png)

### <a name="building-a-more-complex-storyboard"></a>Creación de un guión gráfico más complejo

Después de crear un guión gráfico y agregar una única transición, T1, puede anexar una segunda transición para la variable X llamando de nuevo al método [**IUIAnimationStoryboard::AddTransition,**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) pero con T2 en lugar de T1.

Suponiendo que la transición T2 tenga una duración que tenga en cuenta el contexto, el guión gráfico ahora contiene dos transiciones de back-to-back de duración arbitraria que afectan a la variable X.

![ilustración que muestra un guión gráfico que contiene dos transiciones en la misma variable](images/appendingwithaddtransition.png)

Llamar [**a AddTransition de**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) nuevo con la variable Y y la transición T3 agrega una tercera transición al principio del guión gráfico. Dependiendo de los valores de X e Y cuando se reproduce el guión gráfico, T3 puede terminar después de T1 o incluso después de T2.

![ilustración que muestra un guión gráfico que contiene transiciones entre varias variables](images/multivariablestoryboard.png)

### <a name="using-keyframes"></a>Uso de fotogramas clave

Para agregar una transición en un desplazamiento desde el inicio del guión gráfico, primero debe agregar un fotograma clave. Los fotogramas clave representan instantes en el tiempo y, por sí mismos, no tienen ningún efecto en el comportamiento del guión gráfico. Cada guión gráfico tiene un fotograma clave implícito que representa el inicio del guión gráfico, UI [**\_ ANIMATION FRAME STORYBOARD \_ \_ \_ START;**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))puede agregar nuevos fotogramas clave en desplazamientos desde el principio llamando al método [**IUIAnimationStoryboard::AddKeyframeAtOffset**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset) con UI **ANIMATION KEYFRAME STORYBOARD \_ \_ \_ \_ START**.

El desplazamiento al que agrega un fotograma clave siempre es relativo a otro fotograma clave. En el diagrama siguiente se muestra el resultado de agregar fotograma clave1 y la transición T4, que se aplica a la variable Z, se alinea con fotograma clave1 y se crea con una duración fija. Por supuesto, dado que todavía no se conocen las duraciones de las otras transiciones, T4 podría no ser la última transición en finalizar.

![ilustración que muestra la adición de una transición alineada en un fotograma clave](images/addtransitionatkeyframe.png)

Los fotogramas clave también se pueden colocar en los extremos de las transiciones, mediante el método [**IUIAnimationStoryboard::AddKeyframeAfterTransition.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition) En el diagrama siguiente se muestra el resultado de agregar fotograma clave2 después de T1 y fotograma clave3 después de T2.

![ilustración que muestra la adición de fotogramas clave después de varias transiciones](images/addkeyframeaftertransition.png)

Dado que las duraciones de T1 y T2 no se conocen hasta que se reproduce el guión gráfico, los desplazamientos de fotograma clave2 y fotograma clave3 tampoco se determinan hasta entonces. Por lo tanto, los fotogramas clave2 e incluso los fotogramas clave3 pueden producirse antes que el fotograma clave1.

Tanto el inicio como el final de una transición se pueden alinear con fotogramas clave mediante el método [**IUIAnimationStoryboard::AddTransitionBetweenKeyframes.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes) En el diagrama siguiente se muestra el resultado de agregar una quinta transición, T5, en la variable Y, entre fotograma clave2 y fotograma clave3. Esto modifica la duración de T5, lo que hace que sea más larga o más corta en función de los desplazamientos relativos de fotograma clave2 y fotograma clave3.

![ilustración que muestra la adición de una transición entre fotogramas clave](images/addtransitionbetweenkeyframes.png)

### <a name="holding-variables"></a>Mantener variables

Si T4 finaliza después de T2 y T5, el guión gráfico deja de animar las variables X e Y, lo que hace que estén disponibles para que otros guiones gráficos se animarán. Sin embargo, la aplicación puede llamar al método [**IUIAnimationStoryboard::HoldVariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-holdvariable) para solicitar que el guión gráfico contiene algunas o todas las variables que anima en sus valores finales hasta que el guión gráfico se haya completado. En el diagrama siguiente se muestra el resultado de mantener X y Z cuando T4 finaliza por última vez. Observe que el guión gráfico contiene X en su valor final hasta que el guión gráfico se ha completado. La retención no tiene ningún efecto en Z porque el guión gráfico finaliza cuando finaliza T4.

![ilustración que muestra la retención de variables en los valores finales hasta que se ha completado el guión gráfico](images/holdvariable.png)

Aunque este guión gráfico no mantiene Y, su valor no cambia después de que T5 se complete a menos que otro guión gráfico lo anima. Dado que Y no se mantiene, cualquier otro guión gráfico, independientemente de la prioridad, puede animar Y después de que T5 haya finalizado. Por el contrario, dado que se mantiene X, un guión gráfico de prioridad inferior no puede animar X hasta que este guión gráfico haya finalizado.

Todas estas ilustraciones han supuesto un conjunto arbitrario de valores actuales para las variables cuando el guión gráfico comienza a reproducirse. Si se encuentran otros valores, es probable que las duraciones de las transiciones contextuales sean diferentes, como se muestra en la ilustración siguiente.

![ilustración que muestra el resultado de cambiar las condiciones iniciales usadas para la ilustración anterior](images/holdvariablez.png)

En este escenario, T5 comienza antes de que T3 haya finalizado y, por tanto, T3 se recorta. Dado que T4 finaliza antes que T2 y T5, el valor de Z se mantiene hasta el final del guión gráfico. En general, los valores y las velocidades de las variables cuando un guión gráfico comienza a reproducirse pueden afectar al orden de los fotogramas clave y a la longitud y forma generales del guión gráfico.

### <a name="scheduling-a-storyboard"></a>Programar un guión gráfico

Al programar un guión gráfico, su hora de inicio viene determinada por su esquema y los esquemas de los guiones gráficos que están actualmente en la programación. En concreto, el primer y el último momento en que el guión gráfico anima cada variable individual determinan si dos guiones gráficos y cuándo colisionan, pero los detalles internos de las transiciones dentro de no son importantes.

En la ilustración siguiente se muestra el esquema de un guión gráfico con cinco transiciones que animan tres variables.

![ilustración en la que se muestra un guión gráfico con cinco transiciones que animan tres variables](images/storyboardwithoutline.png)

Una de las piedras angulares de Windows Animation es su compatibilidad para permitir que una animación se complete antes de que comience otra, cuando sea necesario. Aunque esto elimina muchos problemas lógicos, también introduce una latencia arbitraria en la interfaz de usuario. Para solucionar este problema,  las aplicaciones pueden especificar el retraso más largo aceptable para que se inicie un guión gráfico, mediante el método [**IUIAnimationStoryboard::SetLongestAcceptableDelay**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay) y el administrador de animaciones usa esta información para programar el guión gráfico antes de que transcurra el período de latencia especificado. Cuando se programa un guión gráfico, el administrador de animaciones determina si primero se deben cancelar, recortar, concluir o comprimir otros guiones gráficos.

Una aplicación puede registrar un controlador al que se llamará cuando cambie el estado de un guión gráfico. Esto permite a la aplicación responder cuando el guión gráfico comienza a reproducirse, se ejecuta hasta su finalización, se quita completamente de la programación o se impide que se complete debido a la interrupción de un guión gráfico de mayor prioridad. Para identificar los guiones gráficos pasados a controladores de eventos de guión gráfico (o comparaciones de prioridad), una aplicación puede usar el método [**IUIAnimationStoryboard::SetTag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-settag) para aplicar etiquetas a guiones gráficos, similares a los que se pueden usar para identificar variables. Al igual que con el uso de guiones gráficos, los desarrolladores deben tener cuidado al usar etiquetas para identificar guiones gráficos y asegurarse de que no surjan ambigüedades cuando las acciones del usuario hagan que muchos guiones gráficos se ponen en cola.

En los ejemplos siguientes se muestran dos variaciones de un intento de programar el guión gráfico creado en las secciones anteriores de este tema.

En este escenario, ya se han programado seis guiones gráficos, de A a F, para animar variables W, X, Y y Z, pero solo A y B han empezado a reproducirse. El nuevo guión gráfico, etiquetado como G, tiene su retraso aceptable más largo establecido en la duración que se muestra en la ilustración siguiente.

![ilustración que muestra la adición de un nuevo guión gráfico a la programación existente](images/existingschedule1withlines.png)

La aplicación ha registrado comparaciones de prioridad que incluyen la siguiente lógica:

-   G solo puede cancelar C y E, y solo para evitar errores.
-   G solo puede recortar A, C, E y F, y solo para evitar errores.
-   Cualquier guión gráfico puede comprimir cualquier otro guión gráfico (la compresión siempre se realiza solo para evitar errores).

> [!Note]  
> El calificador "solo para evitar errores" significa que las comparaciones de prioridad registradas devuelven S OK solo cuando el parámetro \_ *priorityEffect* es UI **ANIMATION PRIORITY \_ EFFECT \_ \_ \_ FAILURE**. Consulte el [**método IUIAnimationPriorityComparison::HasPriority**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationprioritycomparison-haspriority) para obtener más información.

 

Para iniciar G antes de que haya transcurrido el retraso más largo aceptable, el administrador de animación debe hacer lo siguiente:

-   Recortar F
-   Cancelar E

Cuando se cancela E, D y F se descubren y vuelven a sus esquemas originales:

![ilustración en la que se muestran los contornos originales](images/existingschedule1bwithlines.png)

El administrador de animaciones no necesita cancelar ni recortar C para programar antes de que haya transcurrido el retraso más largo aceptable, por lo que la reunión de C y G determina cuándo se inicia G.

![ilustración en la que se muestra que f se recorta para permitir que c y g se cumplan](images/schedule1withgwithlines.png)

Una vez que G se ha programado correctamente, se pueden determinar las duraciones de sus transiciones y, por tanto, se conoce el resto de su esquema. Sin embargo, el esquema puede cambiar si se quita posteriormente otro guión gráfico de la programación.

Como segundo ejemplo, considere un escenario como el anterior, pero con un retraso aceptable más corto y largo especificado para G.

![ilustración que muestra el escenario anterior, pero con un retraso aceptable más corto más largo para g](images/existingschedule2withlines.png)

En este caso, se toman las siguientes acciones:

-   Recortar F
-   Cancelar E
-   Cancelar C

Además, el administrador de animaciones debe comprimir D según la cantidad que se muestra para permitir que G se inicie después de su retraso más largo aceptable y no más adelante.

![ilustración en la que se muestra dónde d debe comprimirse para permitir que g se inicie en su retraso aceptable más largo.](images/trimmedandcancelledwithlines.png)

Para conservar su tiempo relativo, también se comprimen A, B y F.

![ilustración que muestra a, b, d y f comprimidos](images/schedule2withgwithlines.png)

Sin embargo, los guiones gráficos en variables no relacionadas (no se muestran) no se comprimirían.

Una vez más, el esquema de G se conoce ahora y es diferente del resultado en el primer escenario porque las variables tienen valores diferentes cuando comienza G.

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

 

