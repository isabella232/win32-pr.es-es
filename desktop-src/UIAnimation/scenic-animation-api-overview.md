---
title: Windows Información general sobre animaciones
description: Esta información general proporciona una introducción a la Windows Animation Manager y se centra en los componentes y conceptos clave.
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Windows Animation Windows Animation ,overview
- objetos de administrador de animación Windows Animación ,descrito
- variables de animación Windows animación , descrita
- objetos de temporizador de animación Windows Animación ,descrito
- timing system Windows Animation
- duración contextual de Windows animación
- velocidad de coincidencia Windows animación
- contention management Windows Animation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc0892cffa3e79428e19cbe5b1a3c27d7abda62365c4ceb15731101aa857f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348013"
---
# <a name="windows-animation-overview"></a>Windows Información general sobre animaciones

Esta información general proporciona una introducción a la Windows Animation Manager y se centra en los componentes y conceptos clave. Para obtener más información sobre guiones gráficos y transiciones, vea [Información general sobre guiones gráficos.](storyboard-construction.md)

Este tema contiene las siguientes secciones:

-   [Conceptos básicos](#basic-concepts)
-   [Componentes de Windows animación](#components-of-windows-animation)
-   [La API Windows Animation](#the-windows-animation-api)
-   [Configuraciones](#configurations)
    -   [Animación controlada por la aplicación](#application-driven-animation)
    -   [Animación controlada por temporizador](#timer-driven-animation)
-   [Características avanzadas](#advanced-features)
    -   [Administración de contención](#contention-management)
-   [Temas relacionados](#related-topics)

## <a name="basic-concepts"></a>Conceptos básicos

*La* animación es una secuencia de imágenes fijas sucesivas que produce una sensación de movimiento cuando se reproduce. El uso de animación interactiva en su interfaz de usuario puede proporcionar a una aplicación una personalidad única, así como mejorar la experiencia del usuario. La animación puede ayudar a comunicar los cambios de estado principales en la interfaz de usuario y a administrar la complejidad de la interfaz de usuario. La animación también puede agregar a la percepción del usuario de la calidad de una aplicación.

Como ejemplos, Windows Animation se usa en la barra de tareas para ayudarle a administrar y acceder a archivos y programas, y Lupa para ampliar distintas partes de la pantalla para facilitar que los usuarios las vean.

Las unidades fundamentales de una animación son la característica de un elemento visual que se va a animar y la descripción de cómo cambia esa característica con el tiempo. Una aplicación puede animar una amplia variedad de características, como posición, color, tamaño, rotación, contraste y opacidad.

En Windows animación, una *variable de animación* representa la característica que se va a animar. Una *transición* describe cómo cambia el valor de esa variable de animación a medida que se produce la animación. Por ejemplo, un elemento visual podría tener una variable de animación que especifica su opacidad y una acción del usuario podría generar una transición que toma esa opacidad de un valor de 50 a 100, que representa una animación de semitransparente a totalmente opaca.

Un *guión* gráfico es un conjunto de transiciones aplicadas a una o varias variables de animación a lo largo del tiempo. Una aplicación muestra animaciones mediante la construcción y reproducción de guiones gráficos y, a continuación, el dibujo de secuencias de fotogramas discretos a medida que los valores de las variables de animación cambian con el tiempo.

## <a name="components-of-windows-animation"></a>Componentes de Windows animación

Windows La animación consta de los siguientes componentes:

<dl> <dt>

<span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>administrador de animaciones
</dt> <dd>

Las aplicaciones usan un objeto de administrador de animaciones para crear variables de animación y guiones gráficos, programar y controlar animaciones, y actualizar la información de estado antes de que la aplicación dibuje cada fotograma. Normalmente, un único objeto de administrador de animaciones administra todas las animaciones de una aplicación y, por tanto, tiene control global sobre todos los guiones gráficos programados.

</dd> <dt>

<span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>variables de animación
</dt> <dd>

Antes de iniciar las animaciones, una aplicación debe crear objetos de variable de animación. Una variable de animación representa un aspecto de un elemento visual que se va a animar. La variable es un valor de punto flotante escalar, aunque el valor se puede redondear a un valor entero.

Normalmente, una variable de animación tiene la misma duración que el elemento visual que se va a animar. El valor inicial de una variable de animación se especifica cuando se crea la variable. A partir de entonces, su valor no se puede cambiar directamente; debe actualizarse a través del administrador de animaciones.

Una variable de animación se puede identificar mediante *una* etiqueta , que es un emparejamiento de un identificador entero con un puntero a un objeto COM. Una etiqueta no debe ser única, a menos que la aplicación la use para buscar una variable. De forma predeterminada, una variable de animación no tiene una etiqueta y los intentos de leer su etiqueta producirán un error hasta que se haya establecido una.

</dd> <dt>

<span id="timing_system"></span><span id="TIMING_SYSTEM"></span>sistema de control de tiempo
</dt> <dd>

Windows La animación incluye un sistema de control de tiempo que ayuda a garantizar que las animaciones se representan a una velocidad de fotogramas suave y coherente, al tiempo que se reduce el uso de recursos del sistema para la representación cuando el sistema está ocupado. Un *temporizador* ayuda a administrar la representación de animación indicando automáticamente el paso de una pequeña unidad de tiempo, denominada *tic*. El sistema de control de  tiempo supervisa el rendimiento general de la representación del sistema y limita las animaciones al aumentar o reducir dinámicamente la frecuencia de los tics. Las aplicaciones pueden permitir que un temporizador controle el administrador de animaciones y puede registrar un controlador para recibir una notificación antes y después de actualizar el administrador para cada paso. Las aplicaciones pueden especificar la velocidad mínima de fotogramas de animación aceptable para un temporizador y recibir una notificación si la velocidad de fotogramas real de una animación está por debajo de esta velocidad.

Para conservar los recursos del sistema, se puede configurar un temporizador para deshabilitarse cuando no se está llevando a cabo ninguna animación.

</dd> </dl>

## <a name="the-windows-animation-api"></a>La API Windows Animation

La WINDOWS Animation API es una API basada en COM de un solo subproceso que proporciona las siguientes características para desarrolladores:

-   Un objeto de administrador de animaciones, [**UIAnimationManager,**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85))para crear objetos de animación y controlar animaciones
-   Variables de animación y guiones gráficos
-   Una biblioteca fundamental, [**UIAnimationTransitionLibrary,**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85))de transiciones listas para usar
-   Un objeto de temporizador, [**UIAnimationTimer,**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85))para determinar la hora actual y, opcionalmente, para impulsar la animación
-   Enlaces de eventos para supervisar el estado y el progreso de la animación

Para obtener la referencia completa de la API, [consulte Windows animation reference (Referencia de animación).](windows-animation-reference.md) Para obtener código de ejemplo, [vea Windows Animation Tasks](using-windows-animation.md) y Windows Animation [Samples](windows-animation-samples.md).

## <a name="configurations"></a>Configurations

Las aplicaciones deben obtener la hora actual antes de programar una animación nueva. Estos son los mecanismos de control de tiempo admitidos por Windows Animation:

-   [Animación controlada por la aplicación](#application-driven-animation)
-   [Animación controlada por temporizador](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven animación

Las aplicaciones que usan una API de gráficos acelerados por hardware pueden sincronizarse con la frecuencia de actualización del monitor para representar animaciones fluidas. Como alternativa, una aplicación puede usar un mecanismo de control de tiempo propio para determinar cuándo dibujar cada fotograma de una animación. En cualquier caso, la aplicación le dirá al administrador de animaciones cuándo actualizar su estado. Todavía se puede usar un temporizador de animación para determinar la hora actual con alta precisión, en las unidades requeridas por el administrador de animaciones.

En el diagrama siguiente se muestran las interacciones entre una aplicación y los componentes de animación Windows cuando la aplicación está impulsando directamente las actualizaciones de animación.

![diagrama que muestra las interacciones entre una aplicación y los componentes de animación de Windows cuando la aplicación está impulsando directamente las actualizaciones de animación.](images/animationupdates.png)

En la configuración más sencilla, una aplicación volverá a dibujar todo cada vez que se actualice la pantalla, incluso cuando no se reproduce ninguna animación. Para evitar el trabajo desperdiciado, una aplicación puede registrar un controlador de eventos de administrador para recibir una notificación cuando hay animaciones programadas y puede detectar cuándo la programación está vacía para que pueda dejar de dibujarse.

### <a name="timer-driven-animation"></a>Timer-Driven animación

En lugar de actualizar el administrador de animaciones directamente, las aplicaciones pueden permitir que el temporizador de animación informe al administrador de animaciones cuándo actualizar su estado y simplemente recibir una notificación cuando se haya realizado cada actualización. Este enfoque se recomienda para las API de gráficos anteriores. En general, si es posible sincronizar con la frecuencia de actualización del monitor, es mejor hacerlo y usar la animación controlada por la aplicación.

En el diagrama siguiente se muestran las interacciones entre una aplicación y los componentes de animación Windows cuando el temporizador de animación está impulsando las actualizaciones de animación.

![diagrama que muestra las interacciones entre una aplicación y los componentes de animación de Windows cuando el temporizador de animación está impulsando las actualizaciones de animación.](images/animationtimerupdates.png)

El temporizador se puede configurar para ejecutarse solo cuando se programan las animaciones; es una cuestión sencilla de pasar un parámetro determinado cuando el temporizador y el administrador de animaciones están conectados.

## <a name="advanced-features"></a>Características avanzadas

Más allá de una base básica para admitir la animación, Windows Animation incluye compatibilidad con varias técnicas avanzadas de animación, entre las que se incluyen:

<dl> <dt>

<span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*duración contextual*
</dt> <dd>

No es necesario solucionar la duración de una transición; se puede determinar en función del valor y la velocidad de la variable animada cuando comienza la transición.

</dd> <dt>

<span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*coincidencia de velocidad*
</dt> <dd>

El movimiento suele ser más agradable a los ojos si la posición y la velocidad de un objeto en movimiento no saltan instantáneamente entre los valores. Cuando un guión gráfico nuevo interrumpe uno que se está reproduciendo actualmente, la coincidencia de velocidad permite que el nuevo guión gráfico resalte sin problemas donde finalizó el anterior.

</dd> <dt>

<span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*administración de contención*
</dt> <dd>

Si dos guiones gráficos necesitan actualizar la misma variable de animación simultáneamente, se produce un conflicto de programación. En lugar de requerir una prioridad numérica específica para cada guión gráfico, Windows Animation permite a la aplicación determinar las prioridades relativas de dos guiones gráficos cualquiera.

</dd> </dl>

### <a name="contention-management"></a>Administración de contención

Los desarrolladores pueden implementar una *devolución de* llamada de comparación de prioridad para comparar la prioridad del guión gráfico de que se está programando y el guión gráfico que ya está en la programación. Una aplicación que implementa una comparación de prioridad puede usar cualquier lógica preferida para determinar cuándo un guión gráfico precarga a otro. Para resolver el conflicto de programación, Windows Animation pregunta a la aplicación cuál de estas acciones se puede realizar, en el orden siguiente:

-   **Cancele el guión gráfico programado.** Si el guión gráfico programado aún no se ha empezado a reproducir, es posible que se cancele y se quite inmediatamente de la programación.
-   **Recorte el guión gráfico programado.** Cuando un guión gráfico nuevo recorta un guión gráfico programado, el guión gráfico programado deja de afectar a la variable en cuanto el nuevo guión gráfico comienza a animarlo. Se comparan las velocidades, lo que permite que el nuevo guión gráfico se resalte sin problemas donde lo dejó el anterior.
-   **Concluya el guión gráfico programado.** Un guión gráfico solo se puede concluir si contiene un bucle que se repite indefinidamente. Si el guión gráfico está en un bucle de este tipo cuando se finaliza, se completa la repetición actual y, a continuación, se reproduce el resto del guión gráfico. Si el bucle aún no se ha iniciado cuando se ha finalizado un guión gráfico, el bucle se omite por completo.
-   **Comprima el guión gráfico programado.** Si recortar o cancelar el guión gráfico programado no es una opción, el guión gráfico puede completarse. Windows La animación presenta la posibilidad de comprimir el tiempo disponible para el guión gráfico programado (y los guiones gráficos programados antes de él), por lo que las variables alcanzan su estado final más rápidamente. Cuando se aplica la compresión, el tiempo se acelera temporalmente para los guiones gráficos afectados, por lo que se reproducen más rápido.

Si los objetos de comparación de prioridad registrados no permiten ninguna de las acciones anteriores, se produce un error al intentar programar el nuevo guión gráfico. De forma predeterminada, todos los guiones gráficos se pueden recortar, concluir o comprimir para evitar errores, pero no se puede cancelar ninguno.

En el diagrama siguiente se muestra el ciclo de vida de un guión gráfico, utilizando los estados definidos por la [**\_ enumeración UI ANIMATION \_ STORYBOARD \_ STATUS.**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) Las aplicaciones usan Windows Animation API para compilar un guión gráfico y enviarlo para su programación. El administrador de animación programa el guión gráfico y administra la animación.

![diagrama que muestra cómo el administrador de animación programa el guión gráfico y administra la animación.](images/statediagram.png)

Para obtener más información sobre la programación y administración de guiones gráficos, vea [Información general sobre guiones gráficos.](storyboard-construction.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Referencia de animación](windows-animation-reference.md)
</dt> <dt>

[Windows Ejemplos de animación](windows-animation-samples.md)
</dt> <dt>

[Windows Tareas de animación](using-windows-animation.md)
</dt> </dl>

 

 