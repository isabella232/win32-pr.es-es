---
title: Información general sobre animaciones de Windows
description: Esta información general proporciona una introducción al administrador de animaciones de Windows y se centra en los conceptos y componentes clave.
ms.assetid: de1380c9-6801-4178-9281-a23af7d71d77
keywords:
- Animación de Windows animación de Windows, información general
- objetos del administrador de animaciones animación de Windows, descripción
- variables de animación animación de Windows, descripción
- objetos de temporizador de animación animación de Windows, descripción
- Animación de ventanas de sistema de control de tiempo
- Animación de duración contextual de Windows
- Animación de Windows con coincidencia de velocidad
- Animación de Windows de administración de contención
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a60b02b29d8d434cc93420f36c3cdca4428f94c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077851"
---
# <a name="windows-animation-overview"></a>Información general sobre animaciones de Windows

Esta información general proporciona una introducción al administrador de animaciones de Windows y se centra en los conceptos y componentes clave. Para obtener más información sobre los guiones gráficos y las transiciones, vea [información general sobre guiones gráficos](storyboard-construction.md).

Este tema contiene las siguientes secciones:

-   [Conceptos básicos](#basic-concepts)
-   [Componentes de la animación de Windows](#components-of-windows-animation)
-   [La API de animación de Windows](#the-windows-animation-api)
-   [Configuraciones](#configurations)
    -   [Animación controlada por aplicaciones](#application-driven-animation)
    -   [Animación controlada por temporizador](#timer-driven-animation)
-   [Características avanzadas](#advanced-features)
    -   [Administración de contención](#contention-management)
-   [Temas relacionados](#related-topics)

## <a name="basic-concepts"></a>Conceptos básicos

La *animación* es una secuencia de imágenes aún sucesivas que produce una ilusión de movimiento al reproducirse. El uso de la animación interactiva en su interfaz de usuario puede dar a una aplicación una personalidad única y mejorar la experiencia del usuario. La animación puede ayudar a comunicar los cambios de estado principales en la interfaz de usuario y ayudar a administrar la complejidad de la interfaz de usuario. La animación también puede agregarse a la percepción del usuario de la calidad de una aplicación.

Como ejemplo, la animación de Windows se usa en la barra de tareas para ayudarle a administrar y tener acceso a los archivos y programas, y al ampliador para ampliar diferentes partes de la pantalla con el fin de facilitar la visualización de los usuarios.

Las unidades fundamentales de una animación son la característica de un elemento visual que se va a animar y la descripción de cómo cambia esa característica con el tiempo. Una aplicación puede animar una gran variedad de características, como la posición, el color, el tamaño, la rotación, el contraste y la opacidad.

En la animación de Windows, una *variable de animación* representa la característica que se va a animar. Una *transición* describe el modo en que el valor de la variable de animación cambia a medida que se produce la animación. Por ejemplo, un elemento visual podría tener una variable de animación que especifica su opacidad y una acción del usuario podría generar una transición que toma esa opacidad de un valor de 50 a 100, que representa una animación de semitransparente a totalmente opaca.

Un *guión gráfico* es un conjunto de transiciones que se aplican a una o varias variables de animación a lo largo del tiempo. Una aplicación muestra animaciones construyendo y reproduciendo guiones gráficos y, a continuación, dibujando secuencias de fotogramas discretos a medida que los valores de las variables de animación cambian con el tiempo.

## <a name="components-of-windows-animation"></a>Componentes de la animación de Windows

La animación de Windows consta de los siguientes componentes:

<dl> <dt>

<span id="animation_manager"></span><span id="ANIMATION_MANAGER"></span>Administrador de animaciones
</dt> <dd>

Las aplicaciones usan un objeto de administrador de animaciones para crear variables de animación y guiones gráficos, programar y controlar animaciones, y actualizar la información de estado antes de que la aplicación dibuje cada fotograma. Normalmente, un único objeto de administrador de animaciones administra todas las animaciones en una aplicación y, por tanto, tiene control global sobre todos los guiones gráficos programados.

</dd> <dt>

<span id="animation_variables"></span><span id="ANIMATION_VARIABLES"></span>variables de animación
</dt> <dd>

Antes de iniciar las animaciones, una aplicación necesita crear objetos de variable de animación. Una variable de animación representa un aspecto de un elemento visual que se va a animar. La variable es un valor de punto flotante escalar, aunque el valor se puede redondear a un valor entero.

Normalmente, una variable de animación tiene la misma duración que el elemento visual que se va a animar. El valor inicial de una variable de animación se especifica cuando se crea la variable. Después, su valor no se puede cambiar directamente. debe actualizarse a través del administrador de animaciones.

Una variable de animación se puede identificar mediante una *etiqueta*, que es un emparejamiento de un identificador entero con un puntero a un objeto com. Una etiqueta no debe ser única, a menos que la aplicación la utilice para buscar una variable. De forma predeterminada, una variable de animación no tiene una etiqueta y se producirá un error en cualquier intento de leer su etiqueta hasta que se haya establecido una.

</dd> <dt>

<span id="timing_system"></span><span id="TIMING_SYSTEM"></span>sistema de control de tiempo
</dt> <dd>

La animación de Windows incluye un sistema de control de tiempo que ayuda a garantizar que las animaciones se representan a una velocidad de fotogramas homogénea y uniforme, a la vez que se reduce el uso de los recursos del sistema para la representación cuando el sistema está ocupado. Un *temporizador* ayuda a administrar la representación de animaciones indicando automáticamente el paso de una pequeña unidad de tiempo, denominada *paso*. El sistema de control de tiempo supervisa el rendimiento general de la representación del sistema y *limita* las animaciones al aumentar o reducir dinámicamente la frecuencia de los tics. Las aplicaciones pueden permitir que un temporizador impulse el administrador de animaciones y puede registrar un controlador para que se le notifique antes y después de que se actualice el administrador para cada paso. Las aplicaciones pueden especificar la velocidad de fotogramas de animación mínima aceptable para un temporizador y recibir una notificación si la velocidad de fotogramas real de una animación cae por debajo de esta tarifa.

Para conservar los recursos del sistema, se puede configurar un temporizador para deshabilitarse cuando no se realiza ninguna animación.

</dd> </dl>

## <a name="the-windows-animation-api"></a>La API de animación de Windows

La API de animación de Windows es una API basada en COM de un solo subproceso que proporciona las siguientes características para los desarrolladores:

-   Un objeto de administrador de animaciones, [**UIAnimationManager**](/previous-versions/windows/desktop/legacy/dd317019(v=vs.85)), para crear objetos de animación y controlar animaciones
-   Variables y guiones gráficos de animación
-   Una biblioteca básica, [**UIAnimationTransitionLibrary**](/previous-versions/windows/desktop/legacy/dd317028(v=vs.85)), de transiciones listas para usar
-   Un objeto de temporizador, [**UIAnimationTimer**](/previous-versions/windows/desktop/legacy/dd317021(v=vs.85)), para determinar la hora actual y, opcionalmente, para impulsar la animación
-   Enlaces de eventos para supervisar el estado y el progreso de la animación

Para consultar la referencia completa de la API, consulte [referencia de animación de Windows](windows-animation-reference.md). Para ver un ejemplo de código, vea [tareas de animación de Windows](using-windows-animation.md) y ejemplos de animación de [Windows](windows-animation-samples.md).

## <a name="configurations"></a>Configurations

Las aplicaciones deben obtener la hora actual antes de programar una nueva animación. A continuación se indican los mecanismos de control de tiempo admitidos por la animación de Windows:

-   [Animación controlada por aplicaciones](#application-driven-animation)
-   [Animación controlada por temporizador](#timer-driven-animation)

### <a name="application-driven-animation"></a>Application-Driven animación

Las aplicaciones que usan una API de gráficos con aceleración de hardware pueden sincronizarse con la frecuencia de actualización del monitor para representar animaciones suaves. Como alternativa, una aplicación puede usar un mecanismo de control de tiempo propio para determinar cuándo se debe dibujar cada fotograma de una animación. En cualquier caso, la aplicación le indicará al administrador de animaciones Cuándo debe actualizar su estado. Todavía se puede usar un temporizador de animación para determinar la hora actual con alta precisión en las unidades requeridas por el administrador de animaciones.

En el diagrama siguiente se muestran las interacciones entre una aplicación y los componentes de animación de Windows cuando la aplicación está llevando a cabo actualizaciones de animación directamente.

![diagrama que muestra las interacciones entre una aplicación y los componentes de animación de Windows cuando la aplicación está llevando a cabo actualizaciones de animación directamente.](images/animationupdates.png)

En la configuración más sencilla, una aplicación volverá a dibujar todo cada vez que se actualice la pantalla, aunque no se esté reproduciendo ninguna animación. Para evitar el trabajo desperdiciado, una aplicación puede registrar un controlador de eventos de administrador para que se le notifique cuando se hayan programado animaciones y pueda detectar cuándo está vacía la programación para que pueda dejar de volver a dibujar.

### <a name="timer-driven-animation"></a>Timer-Driven animación

En lugar de actualizar el administrador de animaciones directamente, las aplicaciones pueden dejar que el temporizador de animación indique al administrador de animaciones Cuándo debe actualizar su estado y, simplemente, recibir una notificación cuando se realice cada actualización. Se recomienda este enfoque para las API de gráficos anteriores. En general, si es posible sincronizar con la frecuencia de actualización del monitor, es mejor hacerlo y usar la animación controlada por la aplicación.

En el diagrama siguiente se muestran las interacciones entre una aplicación y los componentes de animación de Windows cuando el temporizador de animación está llevando a cabo actualizaciones de animaciones.

![diagrama que muestra las interacciones entre una aplicación y los componentes de animación de Windows cuando el temporizador de animación está impulsando actualizaciones de animaciones.](images/animationtimerupdates.png)

El temporizador se puede configurar para que se ejecute solo cuando se programan las animaciones; hacerlo es una cuestión sencilla de pasar un parámetro determinado cuando el temporizador y el administrador de animaciones están conectados.

## <a name="advanced-features"></a>Características avanzadas

Además de una base básica para admitir la animación, la animación de Windows incluye compatibilidad con varias técnicas de animación avanzadas, entre las que se incluyen:

<dl> <dt>

<span id="context-sensitive_duration"></span><span id="CONTEXT-SENSITIVE_DURATION"></span>*duración contextual*
</dt> <dd>

No es necesario corregir la duración de una transición; se puede determinar en función del valor y la velocidad de la variable animada cuando comienza la transición.

</dd> <dt>

<span id="velocity_matching"></span><span id="VELOCITY_MATCHING"></span>*coincidencia de velocidad*
</dt> <dd>

Por lo general, el movimiento es más agradable a la vista si la posición y la velocidad de un objeto móvil no se saltan de forma instantánea entre los valores. Cuando un nuevo guion gráfico interrumpe uno que se está reproduciendo actualmente, la coincidencia de velocidad permite que el nuevo guion gráfico se seleccione sin problemas en el punto en el que finalizó el anterior.

</dd> <dt>

<span id="contention_management"></span><span id="CONTENTION_MANAGEMENT"></span>*Administración de contención*
</dt> <dd>

Si dos guiones gráficos necesitan actualizar la misma variable de animación simultáneamente, se produce un conflicto de programación. En lugar de requerir una prioridad numérica específica para cada guión gráfico, la animación de Windows permite a la aplicación determinar las prioridades relativas de dos guiones gráficos.

</dd> </dl>

### <a name="contention-management"></a>Administración de contención

Los desarrolladores pueden implementar una devolución de llamada de *comparación de prioridad* para comparar la prioridad del guion gráfico que se va a programar y el guión gráfico que ya está en la programación. Una aplicación que implementa una comparación de prioridad puede usar cualquier lógica preferida para determinar cuándo un guion gráfico se empts en otro. Para resolver el conflicto de programación, animación de Windows pregunta a la aplicación qué acciones se pueden realizar, en el siguiente orden:

-   **Cancele el guión gráfico programado.** Si el guión gráfico programado aún no ha empezado a reproducirse, podría cancelarse y quitarse inmediatamente de la programación.
-   **Recorte el guión gráfico programado.** Cuando un nuevo guion gráfico recorta un guion gráfico programado, el guion gráfico programado deja de afectar a la variable en cuanto comienza el nuevo guión gráfico para animarlo. Las velocidades coinciden, lo que permite que el nuevo guion gráfico se seleccione sin problemas donde se quedó el anterior.
-   **Concluye el guión gráfico programado.** Un guión gráfico solo se puede concluir si contiene un bucle que se repite indefinidamente. Si el guion gráfico se encuentra en un bucle de este tipo al concluir, se completa la repetición actual y, a continuación, se reproduce el resto del guión gráfico. Si el bucle no ha empezado aún cuando se finaliza un guion gráfico, el bucle se omite por completo.
-   **Comprimir el guion gráfico programado.** Si recortar o cancelar el guión gráfico programado no es una opción, se permite que el guion gráfico se complete. La animación de Windows presenta la posibilidad de comprimir el tiempo disponible para el guión gráfico programado (y los guiones gráficos programados antes), por lo que las variables alcanzan su estado final con mayor rapidez. Cuando se aplica la compresión, el tiempo se acelera temporalmente para los guiones gráficos afectados, de modo que se reproducen más rápido.

Si no se permite ninguna de las acciones anteriores mediante los objetos de comparación de prioridad registrados, se produce un error al intentar programar el nuevo guion gráfico. De forma predeterminada, todos los guiones gráficos se pueden recortar, concluir o comprimir para evitar errores, pero no se puede cancelar ninguno.

En el diagrama siguiente se muestra el ciclo de vida de un guion gráfico, con los Estados definidos por la enumeración de [**\_ \_ \_ Estado de guion gráfico de animación de IU**](/windows/win32/api/uianimation/ne-uianimation-ui_animation_storyboard_status) . Las aplicaciones usan la API de animación de Windows para crear un guion gráfico y enviarlo para su programación. El administrador de animaciones programa el guión gráfico y administra la animación.

![diagrama que muestra cómo el administrador de animaciones programa el guión gráfico y administra la animación.](images/statediagram.png)

Para obtener más información sobre la programación y la administración de guiones gráficos, consulte [información general sobre guiones gráficos](storyboard-construction.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de animación de Windows](windows-animation-reference.md)
</dt> <dt>

[Ejemplos de animación de Windows](windows-animation-samples.md)
</dt> <dt>

[Tareas de animación de Windows](using-windows-animation.md)
</dt> </dl>

 

 