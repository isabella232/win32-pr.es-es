---
title: Asistentes
description: A pesar de que es maravilloso, el nombre de divertidos, los asistentes no son una forma especial de interfaz de usuario y solo tienen un determinado intervalo de utilidad.
ms.assetid: 122d6e65-92f0-4e8a-92f7-ecd7e90665c8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 6455c38228606932e9144c744dd217d0a7fa67e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "103913974"
---
# <a name="wizards"></a>Asistentes

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

A pesar de que es maravilloso, el nombre de divertidos, los asistentes no son una forma especial de interfaz de usuario y solo tienen un determinado intervalo de utilidad.

Los asistentes se utilizan para realizar tareas de varios pasos.

![Captura de pantalla que muestra el asistente ' Agregar impresora ' con ' ¿Qué tipo de impresora desea instalar? ' .](images/win-wizards-image1.png)

![Captura de pantalla que muestra el Asistente para agregar impresora al buscar impresoras disponibles.](images/win-wizards-image2.png)

![captura de pantalla del Asistente para agregar impresoras ](images/win-wizards-image3.png)

Varios pasos de un asistente se presentan como una secuencia de páginas.

Los asistentes suelen incluir los siguientes tipos de páginas:

-   Las páginas de opciones se usan para recopilar información y permitir que los usuarios realicen elecciones.
-   La página confirmación se utiliza para realizar una acción que no se puede deshacer haciendo clic en atrás o cancelar.
-   La página de progreso se usa para mostrar el progreso de una operación larga.

El diseño del asistente moderno impone una gran eficacia, lo que hace que la página de progreso sea opcional para operaciones más cortas y, a menudo, se le ofrece la página de [bienvenida](glossary.md) tradicional y la [Página de enhorabuena](glossary.md) al principio y al final.

Todas las páginas del asistente tienen estos componentes:

-   Una barra de título para identificar el nombre del asistente, con un botón atrás en la esquina superior izquierda y un botón cerrar con botones opcionales minimizar/maximizar y restaurar. Tenga en cuenta que la barra de título también incluye un icono para identificarlo en la barra de tareas.
-   Una instrucción principal para explicar el objetivo del usuario con la página.
-   Un área de contenido con texto opcional y posiblemente otros controles.
-   Un área de comandos con al menos un botón de confirmación para confirmar la tarea o continuar con el paso siguiente.

Aunque un asistente tiene varios pasos, estos pasos deben agregarse a una sola tarea, desde el punto de vista del usuario. Este es el principio de diseño del asistente fundamental de "un asistente, una tarea".

Por lo tanto, en este artículo, una tarea es la función básica de un asistente (por ejemplo, la tarea de un asistente para la instalación es instalar un programa). Las subtareas son aspectos de la tarea más grande (por ejemplo, una subtarea de un asistente para la instalación puede ser configurar el programa que se va a instalar). Por último, cada página del asistente se considera un paso en una tarea o subtarea determinada (por ejemplo, puede haber dos o tres pasos implicados en la configuración del programa).

**Nota:** Las instrucciones relacionadas con la [instalación](exper-setup.md), los [cuadros de diálogo](win-dialog-box.md)y las [barras de progreso](progress-bars.md) se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Se puede usar un asistente para cualquier tarea que requiera varios pasos de entrada. Sin embargo, los asistentes eficaces tienen requisitos adicionales:

-   **¿Realiza el Asistente una sola tarea atómica?** No use interacciones que no sean tareas únicas (todo un programa nunca debe ser un asistente a menos que realice una sola tarea). No use asistentes para combinar tareas independientes o pasos no relacionados en gran medida.
-   **¿Se puede reducir el número de preguntas necesarias? ¿Hay valores predeterminados aceptables que funcionen bien en la mayoría de los casos o se puedan ajustar según sea necesario más adelante? Por lo tanto, ¿se puede reducir el número de páginas?** Si es así, intente simplificar la tarea para que se pueda presentar en una sola página (por ejemplo, un cuadro de diálogo) o elimine la necesidad de la entrada completamente (lo que permite realizar la tarea directamente).
-   **¿Se deben proporcionar las preguntas necesarias secuencialmente? ¿Hay varias preguntas probables pero opcionales?** Si es así, considere un cuadro de diálogo o un cuadro de diálogo con pestañas.

    **Correcto:**

    ![captura de pantalla del cuadro de diálogo Opciones de impresión ](images/win-wizards-image4.png)

    El cuadro de diálogo Opciones de impresión de Microsoft PowerPoint contiene muchas opciones de entrada de usuario, por lo que puede presentarlas en un asistente. Sin embargo, no es necesario proporcionarlos secuencialmente, por lo que un cuadro de diálogo es una opción mejor.

Los asistentes son una forma relativamente intensa de interfaz de usuario; Si hay disponible una solución adecuada y más ligera, úsela.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="overuse-of-wizards"></a>Uso excesivo de asistentes

Históricamente, los asistentes difieren de la interfaz de usuario ordinaria en que se diseñaron para ayudar a los usuarios a realizar tareas especialmente complejas (con pasos que residen en ubicaciones dispares) y a menudo tenían inteligencia integrada para ayudar a los usuarios a tener éxito. En la actualidad, todas las interfaces de usuario deben estar diseñadas para que las tareas sean lo más sencillas posible, por lo que no hay necesidad de una interfaz de usuario especial para este fin.

Sin embargo, la creencia persiste que los asistentes son una interfaz de usuario especial, en gran medida porque se conocen como "asistentes" (mucho más creativos que, por ejemplo, "cuadros de diálogo" y "ventanas de propiedades"). En su lugar, es mejor considerarlas como tareas de varios pasos y no tomar especial atención en ese hecho.

Antes de crear un asistente, tenga en cuenta si los usuarios deben interrumpirse realmente desde el flujo principal del programa. Puede haber una solución más clara y contextual que, en última instancia, resulte más útil para los usuarios. Por ejemplo, una característica mal diseñada en un programa no garantiza que un asistente lo explique y lo simplifique; garantiza el rediseño de la propia característica. No se debe usar un asistente como ayuda de banda para solucionar un problema más básico con el programa.

### <a name="wizards-do-have-appropriate-functions"></a>Los asistentes tienen las funciones adecuadas

Los asistentes son una de las claves para simplificar la experiencia del usuario. Permiten realizar una operación compleja, como la configuración de un programa, y dividirla en una serie de pasos sencillos. En cada punto del proceso, puede proporcionar una explicación de lo que se necesita y mostrar los controles que permiten al usuario realizar selecciones y escribir texto.

Ciertos tipos de tareas de varios pasos se prestan al formulario del asistente. Por ejemplo, en Windows, varios asistentes implican funciones de conectividad (a Internet o a la red corporativa, o a dispositivos periféricos como impresoras y equipos de fax).

![captura de pantalla del Asistente para conexión ](images/win-wizards-image5.png)

La conexión a una red es una tarea típica de Windows adecuada para un asistente.

Aquí, la función del asistente consiste en mediar entre algo conocido y estable (el sistema operativo de caja) y algo desconocido y variable (acuerdos de conectividad con una compañía telefónica o un proveedor de servicios Internet). La complejidad de la informática de los ecosistemas es lo suficientemente importante ahora que es realmente útil usar asistentes para reducir la complejidad.

Otros tipos de tareas que funcionan bien como asistentes de Windows incluyen funcionalidad de tecnología avanzada (como el reconocimiento de voz y escritura a mano) y experiencias multimedia enriquecidas (como la configuración de opciones para realizar y publicar películas). Los asistentes también se pueden implementar para tareas más básicas de varios pasos, como la solución de problemas. En Resumen, si es probable que varios usuarios deseen experimentar el programa de maneras muy diferentes, esto puede indicar la necesidad de un asistente y su capacidad para varios puntos de entrada del usuario.

En el caso de su programa, merece la pena un poco más tiempo de diseño para determinar qué función está atendiendo el asistente, y si esa función realmente aumenta al nivel de implementación de un asistente.

### <a name="wizard-length"></a>Longitud del asistente

Las preguntas de diseño surgen naturalmente en torno al número y la organización de páginas y opciones. Por ejemplo:

-   ¿Hay un número óptimo de páginas para un asistente? ¿O al menos un intervalo deseado?
-   ¿El asistente debe ser conciso y simplificado para que los usuarios puedan hacerlo lo más rápido posible?
-   ¿Debe haber más páginas que requieran menos opciones? ¿O menos páginas con más complejidad? ¿Qué diseño se considera más utilizable?
-   ¿Puede diseñar experiencias más rápidas del asistente aplicando convenciones de la interfaz de usuario como páginas con pestañas?

Microsoft se usa para informar a que los asistentes de tres páginas o menos se diseñan como asistentes sencillos, y los de cuatro o más páginas utilizan un diseño avanzado del asistente (vea las instrucciones de la [experiencia del usuario de Windows](/previous-versions/ms997609(v=msdn.10)) desde 1999). Sin embargo, los estándares de diseño actuales del asistente disponían de lo que había sido una de las principales diferencias entre los formularios simple y avanzado (el uso de las páginas de bienvenida y enhorabuena), por lo que estas categorías ahora no son suficientes y el número de páginas que determinan la opción de diseño parece arbitrario.

El asistente debe ser tan largo o corto como requiere la tarea. no hay ninguna directriz fija para su longitud. Un asistente de una página debe aparecer realmente como un cuadro de diálogo, por lo que dos páginas es probablemente la forma más comprimida posible para un asistente.

**Correcto:**

![captura de pantalla del cuadro de diálogo crear disco ](images/win-wizards-image6.png)

Esta tarea tiene tantos opciones que la presentan como un asistente sería una pérdida de los mismos. Un cuadro de diálogo es el formulario adecuado para esta interfaz de usuario.

En el otro extremo del espectro, si tiene un asistente que incluye varios puntos de decisión y ramas y, con frecuencia, los usuarios pierden el seguimiento de la ruta de navegación, ha superado un límite práctico y debe reducir la longitud del asistente. Como alternativa, es posible que pueda interrumpir el asistente en varias tareas distintas.

Cuando determine la longitud más adecuada para el asistente, preste especial atención a los usuarios de destino. Los programas para los usuarios finales, como los consumidores particulares y los trabajadores de oficina, suelen usar asistentes para ocultar la complejidad; los asistentes son lo más cortos posible, con un diseño de página limpio y simple, y los valores predeterminados previamente seleccionados para tantas opciones como sea posible. Por el contrario, los asistentes de servidor o los programas destinados a los profesionales de ti suelen ser más largos y más complejos. Este grupo de usuarios de destino tiene una tolerancia mucho mayor para tomar decisiones de configuración y, de hecho, puede ser sospechoso si se oculta demasiada complejidad.

Si un asistente por naturaleza simplifica una tarea compleja, debe hacerlo de forma relativamente mínima para una audiencia técnicamente sofisticada y de manera relativamente agresiva para una base de usuarios sin experiencia.

**Correcto:**

![captura de pantalla del Asistente para mostrar idiomas ](images/win-wizards-image7.png)

Esta página del asistente está bien diseñada para los usuarios finales porque reduce un sujeto potencialmente complejo a una elección binaria simple y lógica: instalar o desinstalar.

**Correcto:**

![Captura de pantalla que muestra la página "selección de características" del Asistente para la instalación de "SQL Server".](images/win-wizards-image8.png)

En el Asistente para la instalación de Microsoft SQL Server 2008, el diseño de página está más ocupado y las numerosas opciones requieren más pensamiento, pero el público de destino es administradores de bases de datos que esperan un estrecho control de la selección de características.

Por último, preste atención a la frecuencia con la que se puede realizar la tarea en cuestión. Una tarea poco frecuente puede implementar un asistente más largo, mientras que las tareas frecuentes deben favorecer la brevedad.

### <a name="branching"></a>Bifurcación

En el caso de los asistentes más largos, puede que tenga que crear bifurcaciones del flujo de tareas en las que la secuencia de páginas puede diferir según la entrada del usuario proporcionada como "ascendente". La bifurcación se está desubicando de forma inherente para los usuarios, por lo que debe diseñar la experiencia del usuario para transmitir la estabilidad. No se recomiendan más de dos puntos de decisión que provocarán la bifurcación en el asistente completo y no más de una rama anidada dentro de una sola rama.

Para obtener instrucciones sobre cómo crear una experiencia de usuario estable dentro de un asistente para bifurcaciones, vea el tema sobre la creación de [ramas](#branching) en la sección directrices de este artículo.

### <a name="providing-a-navigation-guide"></a>Proporcionar una guía de navegación

Las guías de navegación pueden ser útiles cuando hay muchos pasos en la tarea y los usuarios pueden perder su lugar en la secuencia, o simplemente quieren saber cuánto tiempo se tarda en completarse.

Las guías de navegación suelen aparecer como una lista de páginas o secciones del asistente, mirando un poco como una tabla de contenido, en una columna o panel del lado izquierdo de cada página. Aunque la lista se conserva a lo largo del asistente (la misma lista de páginas aparece en cada página), hay algunos medios visuales que indican dónde se encuentra el usuario actualmente en la secuencia (por ejemplo, con negrita para distinguir la página o sección activa).

Las guías de navegación pueden ser secuenciales o no secuenciales. El tipo secuencial presenta las páginas anteriores junto con las páginas futuras conocidas. Puede presentar el futuro en términos de pasos en lugar de páginas si los pasos son conocidos y las páginas son dependientes. Después, puede rellenar las páginas de forma dinámica a medida que se conocen. Dado que la secuencia de navegación es fija, la guía de navegación no es interactiva.

Las guías de navegación no secuenciales son interactivas, por lo que los usuarios pueden volver a visitar las páginas previamente vistas directamente. También pueden omitir la secuencia de navegación para las páginas diseñadas para ser opcionales. Las páginas opcionales deben tener valores predeterminados que sean aceptables en la mayoría de los casos. Con este tipo de guía:

-   Las páginas vistas anteriormente siempre se pueden ver directamente.
-   Es posible que no se vean futuras páginas si tienen requisitos previos.
-   Las páginas que se pueden visitar deben distinguirse de manera visible de las que no pueden (por ejemplo, mediante el uso de vínculos activos o deshabilitados), junto con las páginas requeridas u opcionales.

Los usuarios se pueden confundir sobre el significado del botón atrás en este escenario. ¿Al hacer clic en atrás se le conducirá a la página o sección anterior de la guía de navegación, o a la última página o sección que se vio? Dado que los asistentes de Windows ahora colocan el botón atrás en la esquina superior izquierda de las páginas del asistente, en lugar de en la esquina inferior derecha con los demás botones de confirmación, los usuarios piensan en la funcionalidad de vuelta en la Web. Por lo tanto, la mejor solución es hacer que el botón atrás sea el significado de la navegación web (al hacer clic en atrás debe conducir a la última página o sección visualizada) y usar la guía de navegación del Asistente para una navegación secuencial.

### <a name="page-integrity"></a>Integridad de página

El diseño del asistente no solo implica tomar decisiones relacionadas con el flujo de tareas completo, como la forma de controlar la navegación y la experiencia de bifurcación, sino también las que pertenecen a las páginas individuales que componen el asistente. **El principio más importante para diseñar buenas páginas del asistente es la integridad: el contenido de una página debe estar Unido.**

Las páginas del asistente son mucho más fáciles de usar si cada una de ellas se bloquea conceptualmente, con solo un aspecto de la tarea global. La [instrucción principal](glossary.md) es el medio principal para lograr esto. Identifique claramente el objetivo o el propósito de la página para los usuarios. Todas las [instrucciones adicionales](glossary.md), así como los controles de la página, se relacionan directamente con la instrucción principal. A pesar de que las páginas del asistente deben presentar a los usuarios opciones en las que se requiere algún pensamiento, ese esfuerzo no se siente como el trabajo porque está muy enfocado por la integridad de la propia página.

Desafortunadamente, los diseñadores de asistentes suelen equivocar al hacer clic rápidamente en el botón siguiente como prueba de la facilidad de uso, la simplicidad y la integridad de sus páginas. La experiencia del asistente Ultimate no es Next, Next, Next, Next. Aunque esta experiencia sugiere que los valores predeterminados se eligieron correctamente, también sugiere que el asistente no era realmente necesario, ya que todas las opciones son opcionales.

En lo que respecta a los objetos visuales y el texto, reduzca estos elementos a los aspectos esenciales. Resista la tentación de agrupar varias subtareas en una sola página (el "Asistente para Burrito") o de recurrir a las pestañas para presentar requisitos de entrada complejos. Una sola página debe cubrir una única subtarea de la tarea general del asistente.

**Incorrecto:**

![captura de pantalla del Asistente para la instalación de SQL Server ](images/win-wizards-image9.png)

Con tres pestañas de la entrada de usuario bastante densa requerida, esta página del asistente está intentando realizar demasiadas acciones.

En la mayoría de los casos, mantenga el tamaño de cada página a lo largo del Asistente para fomentar una apariencia coherente. Aunque los asistentes de Windows permiten páginas de tamaño ajustable para que el tamaño de una página coincida con la cantidad de contenido, solo algunos usan esta opción.

Por último, mantenga los elementos estructurales de cada página del asistente a través de la secuencia. Por ejemplo, no vuelva a colocar el botón atrás de la esquina superior izquierda en el área botones de confirmación de una o dos páginas. Este nivel de coherencia del diseño ayuda a los usuarios a sentirse estables dentro del asistente. Piense en esto como una línea de base para la integridad visual de una página.

### <a name="finding-the-right-level-of-communication"></a>Buscar el nivel correcto de comunicación

Los usuarios tienen una tolerancia baja para leer grandes bloques de texto en la pantalla e incluso menos en una superficie de la interfaz de usuario cuyo propósito expreso es desplazarse rápidamente a través de una tarea.

Los asistentes tienen tendencia al exceso de comunicación. Ocupan mucho espacio en la pantalla, lo que parece alentar a una unidad para que rellene el espacio. Es como una variación de la ley de Parkinson: el texto de la interfaz de usuario se expandirá para rellenar el espacio disponible.

Una causa de este exceso es la redundancia. Debido a las plantillas que se usan en el diseño del asistente temprano, el mismo idioma podría aparecer en varias ubicaciones en una página, como en la barra de título, los encabezados, el texto del cuerpo, las etiquetas de control, etc.

Merece la pena contratar un editor profesional para eliminar el texto del asistente ruthlessly. Elimine las preguntas y las opciones innecesarias en las páginas individuales y elimine todas las páginas del asistente como un todo (por ejemplo, las páginas de bienvenida y enhorabuena tradicionales). Obtenga acceso al punto de la página con una instrucción principal de escritura concisa, con el lenguaje que usa el público de destino para describir la tarea, no la jerga de la tecnología o característica que usted o su equipo usa internamente. Este enfoque centrado en el usuario es fundamental para mejorar la comunicación de los asistentes del programa.

Preste especial atención al tono del asistente: a veces las impresiones más duraderas de su programa son el resultado no de lo que le digo, sino de cómo lo digas. En los asistentes, los usuarios se sienten cómodos con un tono de conversación agradable, con un uso liberal del pronombres de la segunda persona ("usted") cuando el programa solicita datos. Para obtener más instrucciones, consulte [estilo y tono](text-style-tone.md).

Reducir el recuento de palabras en la página del asistente suele ser elogiable, pero tenga cuidado de no llegar demasiado lejos. Si la tarea es importante y garantiza un asistente, los usuarios aprecian que dispone de suficiente información para tomar decisiones acertadas. En el ejemplo siguiente se muestra cómo se puede condensar el texto del asistente sin sacrificar el significado.

**Antes:**

![captura de pantalla del asistente ClearType, draft ](images/win-wizards-image10.png)

**Después:**

![captura de pantalla del asistente ClearType, revisado ](images/win-wizards-image11.png)

La versión editada de esta página del asistente proporciona una instrucción principal orientada a tareas, quita el párrafo explicativo que se encuentra debajo de la instrucción principal y revisa la etiqueta de la casilla para aclarar la finalidad de la casilla.

**Si solo hace tres cosas...**

1. Asigne la tarea que está intentando realizar con la interfaz de usuario adecuada para realizar el trabajo; no tiene por qué tener como valor predeterminado un asistente cuando cree que necesita recopilar una gran cantidad de entradas de los usuarios.

2. Piense detenidamente en la longitud y la estructura del asistente; prefiera que los asistentes cortos y sin bifurcación mantengan la experiencia lo más simple posible, para que los usuarios puedan volver a su tarea principal o a su interés en el programa.

3. Garantizar la integridad de cada página del asistente: el contenido de una página debe estar claramente Unido.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Considere las alternativas ligeras en primer lugar, como cuadros de diálogo, paneles de tareas o páginas individuales.** No tiene que usar asistentes; puede proporcionar información útil y ayuda en cualquier interfaz de usuario.
-   **Use los asistentes para las tareas de varios pasos.** Usar cuadros de diálogo de varias páginas para tareas de un solo paso con comentarios. Para obtener más instrucciones, consulte [cuadros de diálogo](win-dialog-box.md).

    **Correcto:**

    ![captura de pantalla del cuadro de diálogo diagnósticos ](images/win-wizards-image12.png)

    ![captura de pantalla de los comentarios del cuadro de diálogo diagnóstico ](images/win-wizards-image13.png)

    En este ejemplo, diagnósticos de red de Windows consta de páginas de progreso y resultados. Dado que la tarea es solo un paso único, no requiere los botones de navegación que los usuarios necesitan en un asistente. Se presenta de manera eficaz como un cuadro de diálogo de varias páginas.

### <a name="window-size"></a>Tamaño de la ventana

-   **Elija un tamaño de ventana que pueda mostrar todas las páginas del asistente sin desplazamiento vertical u horizontal de la página.** Aunque es posible que los controles de la página requieran desplazamiento, las propias páginas del asistente no deben hacerlo.
-   **Ajuste el tamaño de las ventanas lo suficientemente grande como para realizar sus tareas de una comodidad.** El diseño de página no debe ser estorban ni requerir que los usuarios se desplacen o cambien de tamaño excesivamente.
-   **Pero no hacer que Windows sea demasiado grande.** Las ventanas más grandes hacen que la tarea sea más compleja y requieren un movimiento adicional para la interacción.
-   **Use ventanas de tamaño variable para un asistente que pueda beneficiarse de más espacio de pantalla pero no lo requiera.** Asigne un tamaño mínimo adecuado. Las ventanas de tamaño variable son útiles cuando las páginas requieren interactuar con contenido de tamaño variable, como vistas de lista grandes.

    **Correcto:**

    ![captura de pantalla de la instalación de Visual Studio, lista parcial ](images/win-wizards-image14.png)

    **Manera**

    ![captura de pantalla de la instalación de Visual Studio, lista completa ](images/win-wizards-image15.png)

    En este ejemplo, el cambio de tamaño de la ventana ayuda a los usuarios a ver la lista completa.

-   **Considere la posibilidad de usar asistentes de tamaño dinámico cuyo tamaño de página cambia según sea necesario para su contenido.** Esto permite a un asistente acomodar diseños de página con una amplia variedad de contenido.
-   **Prefiere el ajuste de tamaño estático sobre dinámico si los usuarios pueden percibir los cambios como falta de estabilidad en su experiencia del asistente.** A menudo, la estabilidad visual supera el alojamiento de contenido. La mayoría de los asistentes deben adoptar tamaños de ventana estándar y estáticos, con un tamaño dinámico reservado para casos especiales.

### <a name="wizard-length"></a>Longitud del asistente

-   **Haga que el asistente sea tan conciso y más sencillo como sea posible.** Deshágase de las opciones y preguntas innecesarias y use los valores predeterminados inteligentes para reducir el número de páginas necesarias para los datos proporcionados por el usuario.
    -   **Excepción:** Los profesionales de ti y otros usuarios técnicos tienen una mayor tolerancia para asistentes más largos y requisitos de entrada detallados.
-   **Haga que el asistente tenga un mínimo de dos páginas.** En su lugar, un asistente de una página debe rediseñarse como un cuadro de diálogo.
-   **No reduzca el número de páginas del asistente simplemente aumentando la complejidad de cada página.** Por ejemplo, una página del asistente que incluye tres pestañas que requieren la intervención del usuario debe rediseñarse como tres páginas independientes.
-   **No aumente el número de páginas del asistente haciendo que cada página sea tan sencilla que los usuarios mindlessly clic en siguiente a través de la secuencia completa.** Se trata de un error común de diseño del asistente. Si una página del asistente no requiere al menos algún grado de pensamiento, es probable que no tenga que estar en absoluto en el asistente.

### <a name="branching"></a>Bifurcación

-   **Prefiere el diseño del Asistente para la no ramificación en una bifurcación.** Los asistentes que no son de bifurcación suelen ser más sencillos, más cortos y fáciles de navegar. Los asistentes de bifurcación dificultan que los usuarios determinen el número de pasos de la tarea y dónde se encuentran en la secuencia.
-   **Si tiene que crear una rama, ayude a los usuarios a orientarse a ellos mismos mediante una de las técnicas siguientes:**
    -   **Enumerar páginas.** Una técnica común consiste en indicar la ubicación del usuario en la secuencia de cada página, como con la frase paso X de Y. Asegúrese de que el punto de conexión (Y) es estable. Si cambia el valor, esto dificulta la confianza de los usuarios.
    -   **Incluya la noción de** subprocesos (como el paso 2a de 6).
    -   **Cree pasos independientes de las páginas, donde cada paso puede incluir varias páginas.** Por ejemplo, un servicio de viajes podría emplear la organización del asistente basada en convenciones de comercio electrónico bien establecidas para el sector.

        **Correcto:**

        ![captura de pantalla de la organización del asistente basada en pasos ](images/win-wizards-image16.png)

        Las etiquetas lógicas pueden proporcionar una orientación adecuada para los usuarios de un asistente de bifurcación.

    -   **Trate los pasos opcionales como persistentes en la secuencia de enumeración.** Por ejemplo, si una bifurcación simplemente omite algunos pasos opcionales, simplemente omita los pasos de los comentarios, en lugar de volver a numerar. Por lo tanto, si un usuario elige la página 2, lo que hace que las páginas 3 y 4 sean opcionales, muestre los pasos 1, 2, 5 y 6 de 6. No renumerar los pasos 5 y 6.
    -   **Si el asistente emplea una sola rama y la bifurcación se produce al principio de la tarea, inicie la secuencia en ese momento y, a continuación, simplemente use el enfoque sin bifurcación.** Es decir, a partir del punto de la bifurcación, progresa en secuencia hasta el final de la bifurcación.

-   **Si debe crear una bifurcación, limite el número de bifurcaciones a uno o dos en un solo asistente.** Nunca incluya más de una rama dentro de una bifurcación (una rama "anidada").

### <a name="commit-buttons"></a>Botones de confirmación

-   **Cuando los usuarios están confirmando una tarea, use un botón de confirmación que sea una respuesta específica a la instrucción principal** (por ejemplo, imprimir, conectar o iniciar). No use etiquetas genéricas como Next (que no implica ningún compromiso) o Finish (que no es específico) para confirmar una tarea. Las etiquetas de estos botones de confirmación deberían tener sentido por sí solos. Iniciar siempre etiquetas de botón de confirmación con un verbo. **Excepciones:**
    -   Use finalizar cuando las respuestas específicas sigan siendo genéricas, como guardar, seleccionar, elegir o obtener.
    -   Use finalizar para cambiar una configuración específica o una colección de valores de configuración.
-   **Un solo asistente puede tener varios puntos de confirmación, pero se prefiere un único punto.**
-   **Si es necesario, puede cambiar el nombre u ocultar los botones de confirmación en una página.** Esta flexibilidad es una ventaja del nuevo diseño del asistente en Windows que no estaba disponible en los asistentes anteriores. Tenga en cuenta que ocultar un botón confirmar no es lo mismo que deshabilitarlo.
-   **Evite deshabilitar un botón de confirmación positivo.** De lo contrario, los usuarios deben deducir por qué están deshabilitados los botones de confirmación. Es mejor dejar habilitados los botones de confirmación y proporcionar un mensaje de error útil siempre que surja un problema. Deshabilitar el botón solo es aceptable si el motivo para hacerlo es obvio y no es ambiguo.
-   **No confunda los botones de navegación (siguiente y atrás) con los botones de confirmación.** A continuación se indica el progreso del asistente sin compromiso; Back siempre debe estar disponible en la página siguiente y, al hacer clic en atrás, se debe deshacer el efecto del último botón siguiente. Si esto no es posible, los usuarios están realizando un compromiso y se indica a través de una etiqueta específica en el botón confirmar. Para obtener más instrucciones acerca de los botones siguiente y atrás, consulte [navegación](#providing-a-navigation-guide).

### <a name="cancel-buttons"></a>Cancelar botones

-   **No pídale a los usuarios que confirmen si realmente pretenden cancelar.** Esto puede resultar molesto. **Excepciones:**
    -   La acción tiene consecuencias importantes y, si es incorrecta, no es fácil fixable.
    -   La acción puede provocar una pérdida significativa del tiempo o del trabajo del usuario.
    -   La acción es claramente incoherente con otras acciones.
-   **Permitir a los usuarios reiniciar los asistentes en caso de que se hayan cancelado por error.**
-   **No deshabilite el botón Cancelar. Excepciones**
    -   Si la cancelación es dañina, que podría ser el caso al realizar una tarea en asistentes independientes.
    -   Si no es posible cancelar, lo que podría ser el caso en el que el asistente no tiene control sobre todos los pasos.

### <a name="close-buttons"></a>Botones cerrar

-   **Use cerrar para Follow-Up y páginas de finalización.** No use cancelar, porque al cerrar la ventana no se descartarán los cambios o acciones realizados en este momento. No utilice Done, ya que no es un verbo imperativo.
-   **Una vez realizada la tarea, la cancelación debe cerrarse (para los asistentes independientes).** El efecto de cerrar es simplemente cerrar la ventana.

### <a name="other-controls"></a>Otros controles

-   **Use los vínculos de comandos solo para las opciones, no para los compromisos.** Los botones de confirmación específicos indican mucho mejor el compromiso que los vínculos de comandos de un asistente.
-   **Al usar vínculos de comandos, oculte el botón siguiente, pero deje el botón Cancelar.**

### <a name="using-pages-vs-dialog-boxes-or-inline-ui"></a>Usar páginas (frente a cuadros de diálogo o interfaz de usuario alineada)

-   **En general, prefiere páginas a cuadros de diálogo.** Los usuarios esperan que los asistentes estén basados en páginas.
-   **Utilice los cuadros de diálogo para ayudar a completar páginas,** como con los selectores y exploradores de objetos.
-   **Utilice los cuadros de diálogo para proporcionar mensajes de error que se aplican a toda la página y el resultado de hacer clic en un botón de confirmación.**
-   **Use la presentación en línea para comportamientos dinámicos simples,** como la divulgación progresiva y la interfaz de usuario contextual.
-   **Use la presentación en línea para los mensajes de error que se aplican a controles específicos.**

### <a name="wizard-pages"></a>Páginas del asistente

-   **Céntrese en la toma de decisiones eficaz.** Reduzca el número de páginas para centrarse en Essentials. Consolide páginas relacionadas y tome páginas opcionales fuera del flujo principal. Hacer que los usuarios haga clic en siguiente completamente a través del asistente puede parecer una buena experiencia al principio, pero si los usuarios nunca necesitan cambiar los valores predeterminados, es probable que las páginas no sean necesarias.
-   **Diseñe cada página para que tenga un único propósito y coherencia visual.** Para obtener más información, vea [integridad de página](#page-integrity).
-   **No usar páginas de bienvenida: hace que la primera página sea funcional siempre que sea posible.** Use una página de Introducción opcional solo cuando:

    -   El asistente tiene requisitos previos que son necesarios para completar el asistente correctamente.
    -   Es posible que los usuarios no conozcan el propósito del asistente en función de la primera página de su elección y no haya espacio para una explicación más detallada.
    -   La instrucción principal para Introducción páginas es "antes de comenzar:".

    **Incorrecto:**

    ![captura de pantalla de la página de bienvenida de configuración de MapPoint ](images/win-wizards-image17.png)

-   Los asistentes modernos optan por las primeras páginas funcionales. Aquí no hay nada que hacer, pero haga clic en siguiente. ¿Por qué obligar a los usuarios a pagar este impuesto de token en un tiempo valioso?
-   **En las páginas en las que se pide a los usuarios que realicen elecciones, optimice los casos más probables.** Estos tipos de páginas deben presentar opciones reales, no solo instrucciones.
    -   Si no usa una página de Introducción, explique la finalidad del asistente en la parte superior de la primera página de opciones.
-   **Use las páginas de confirmación para que quede claro cuando los usuarios se confirman en la tarea.** Normalmente, la página de confirmación es la última página de opciones y el botón siguiente se reetiqueta para indicar la tarea que se confirma.
    -   No utilice páginas de resumen que resuman simplemente las selecciones anteriores del usuario, a menos que la tarea sea arriesgada (lo que implica la seguridad, o la pérdida de tiempo o dinero) o haya una buena posibilidad de que los usuarios tengan que revisar sus selecciones.
-   **Use páginas de progreso para mostrar el estado de una operación larga.** Una vez finalizado correctamente, la página de progreso debe avanzar automáticamente al paso siguiente. Debe permanecer en la página de progreso solo si hay un problema que el usuario necesita ver. Hacer clic en volver a una página de progreso no debe tener ningún efecto secundario.
    -   **Use una sola barra de progreso determinante.** Siga las [instrucciones de la barra de progreso de finalización](progress-bars.md), que incluye:
        -   Indique claramente la finalización. No permita que una barra de progreso vaya al 100 por ciento, a menos que la operación se haya completado.
        -   No reinicie el progreso. Una barra de progreso pierde su valor si se reinicia (quizás porque se completa un paso de la operación) porque los usuarios no tienen forma de saber cuándo se completará la operación. En su lugar, haga que todos los pasos de la operación compartan una parte del progreso y que la barra de progreso vaya a finalización una vez.
    -   **Proporcione una descripción concisa del paso actual situado encima de la barra de progreso.** En el caso de las operaciones rápidas, este tipo de texto no es necesario; la barra de progreso solo es suficiente. En el caso de las operaciones que requieren un minuto o más, el texto puede ser útil.
        -   Utilice fragmentos de oraciones, que normalmente empiezan por un verbo, y que terminan con puntos suspensivos. Ejemplos: Copiando archivos..., instalando los componentes necesarios....
        -   Coloque el texto encima de la barra, no a continuación.
        -   **Incorrecto:**
        -   ![captura de pantalla de la barra de progreso con el texto siguiente ](images/win-wizards-image18.png)
        -   En este ejemplo, el texto explicativo debe aparecer encima de la barra de progreso.
        -   Abstenerse de abarrotar la página de progreso con detalles innecesarios. Esta página no es para soporte técnico; es para los usuarios.
        -   **Incorrecto:**
        -   ![captura de pantalla de la barra de progreso con demasiados detalles ](images/win-wizards-image19.png)
        -   En este ejemplo, los detalles técnicos, como los GUID, no tienen sentido para los usuarios.
-   **No utilice páginas de enhorabuena que no hagan nada, pero que finalice el asistente.** Si los resultados del asistente son evidentes para los usuarios, solo tiene que cerrar el asistente en el botón de confirmación final.
    -   Utilice Follow-Up páginas cuando haya tareas relacionadas que es probable que los usuarios realicen como seguimiento. Evite tareas de seguimiento conocidas, como "enviar un mensaje de correo electrónico".
    -   Use las páginas de finalización solo cuando los resultados no estén visibles y no haya una forma mejor de proporcionar comentarios para la finalización de tareas.
    -   Los asistentes que tienen páginas de progreso deben usar una página de finalización o Follow-Up página para indicar la finalización de la tarea. En el caso de las tareas de ejecución prolongada, cierre el asistente en la página confirmar y use las notificaciones para enviar comentarios.
-   **Use las páginas de Resumen solo si la entrada es compleja y los usuarios deben revisarla, si la tarea implica un riesgo significativo (por ejemplo, una transición financiera) o si el asistente realizará una acción en función de los datos proporcionados por el usuario que no sean obvios (para generar confianza a través de la transparencia).** A menudo, las páginas de resumen no cumplen esta barra de relevancia y se pueden omitir.
-   **Use las páginas de error si no se puede completar el asistente debido a un problema del que no es posible la recuperación.** En esta página, explique cuál es el problema en lenguaje claro, sin que los usuarios de jerga técnica lo sepan. Proporcione también los pasos prácticos que los usuarios pueden llevar a cabo para resolver el problema. Para obtener más instrucciones, consulte [mensajes de error](mess-error.md).
    -   **Excepción:** Si el asistente se completa con un problema leve del que es posible la recuperación, presente el problema como una tarea adicional en lugar de un error. Use el lenguaje de promoción correcto, orientado a errores, que le anima, no los términos como error, error o problema. No use un icono de error.

### <a name="navigation"></a>Navegación

-   **Usar siguiente solo al avanzar a la página siguiente sin compromiso.** El avance a la página siguiente se considera un compromiso cuando su efecto no se puede deshacer haciendo clic en atrás o cancelar.
-   **Use atrás solo para corregir errores.** Además de corregir los errores, los usuarios no deben hacer clic en atrás para realizar el progreso en una tarea.
-   **Conservar las selecciones del usuario a través de la navegación.** Por ejemplo, si el usuario realiza cambios, vuelve a hacer clic en atrás y, a continuación, los cambios se deben conservar. Los usuarios no esperan tener que volver a escribir los cambios a menos que elijan explícitamente borrarlos.
-   **No deshabilite el botón atrás a menos que la repetición de los pasos sea perjudicial.**
-   **Permitir a los usuarios examinar o revisar las opciones en los siguientes escenarios de navegación:**
    -   El usuario proporciona la entrada, hace clic en el botón confirmar, vuelve a hacer clic para revisar los cambios anteriores, no cambia nada y vuelve a hacer clic en el botón confirmar. Normalmente, esto debe ser posible y la segunda confirmación debe pasar a la página siguiente (porque la tarea ya se ha realizado).
    -   El usuario proporciona la entrada, hace clic en el botón confirmar, vuelve a hacer clic para revisar los cambios anteriores, cambia algo y, a continuación, vuelve a hacer clic en el botón confirmar. Normalmente, debe ser posible y la segunda confirmación debe rehacer la tarea con la entrada modificada (reemplazando o deshaciendo el efecto de la primera).

### <a name="help"></a>Ayuda

-   **Diseñe las páginas del Asistente para proporcionar suficiente información, de modo que no sea necesario hacer referencia a la documentación de la ayuda del programa.** Un asistente ya está sacando a los usuarios de su interacción directa deseada con el programa; solicitar a los usuarios que busquen ayuda externa Los elimina incluso de este estado. La ayuda debe ser la excepción, no la regla.
-   **Si debe proporcionar un punto de acceso para ayuda, use un vínculo en la parte inferior izquierda del área de contenido de la página (encima del área de comandos).** Este vínculo debe ser breve y suele ser una frase en forma de pregunta que es más probable que los usuarios deseen responder.
-   **Correcto:**
-   ![captura de pantalla de la página del asistente con el vínculo de ayuda ](images/win-wizards-image5.png)
-   Este vínculo a la ayuda es adecuado porque la información básica básica como esta tendría un desorden demasiado en la página del asistente.

## <a name="text"></a>Texto

### <a name="general"></a>General

-   Use usted y su para hacer referencia al usuario y al equipo, el documento, la configuración, etc. del usuario. No use la primera persona (I, mi) para hacer referencia al equipo o al asistente. Sin embargo, es aceptable usar la primera persona en las opciones que el usuario selecciona. **Ejemplo: casilla mi solo uso** .
-   Cada página del asistente debe tener una [instrucción principal](glossary.md).

### <a name="titles"></a>Títulos

-   Coloque el nombre del asistente en la barra de título. Usar [mayúsculas y minúsculas de estilo de título](glossary.md).
-   Los títulos no deben incluir signos de puntuación, excepto los que tienen signos de interrogación.
-   No incluya el Asistente para Word en los títulos del asistente. Por ejemplo, use conectarse a una red en lugar de al Asistente para configuración de red.

### <a name="buttons"></a>Botones

-   No incluya texto en el botón atrás. En su lugar, use el glifo de flecha sin etiquetar.
-   Incluya texto en el botón siguiente. No use glifos (como > o >>) además de la palabra siguiente.
-   Use etiquetas de botón de confirmación específicas que tengan sentido por sí mismas y que sean una respuesta a la instrucción principal. Lo ideal es que los usuarios no tengan que leer nada más para entender la etiqueta. Es mucho más probable que los usuarios lean etiquetas de botón de comando que el texto estático.
-   Si es posible, no use la palabra finalizar para la etiqueta del botón de confirmación, ya que normalmente hay un botón de confirmación mejor y más específico:
    -   Si al hacer clic en el botón se confirma la tarea (por lo que no se ha realizado ya la tarea), use una etiqueta específica que comience por un verbo que sea una respuesta a la instrucción principal (ejemplos: Print, Connect, Start).
    -   Si la tarea ya se ha realizado en el asistente, utilice Close en su lugar.

        **Excepciones:**

        -   Puede usar finalizar cuando la etiqueta específica siga siendo genérica, como guardar, seleccionar, elegir o obtener.
        -   Puede usar finalizar cuando la tarea implique cambiar una configuración o una colección de valores de configuración.

-   Iniciar las etiquetas del botón confirmar con un verbo. Las excepciones son OK, yes y no.
-   Usar [mayúsculas y minúsculas en el estilo de oraciones](glossary.md).
-   No uses puntuación final.

## <a name="documentation"></a>Documentación

-   Aunque la mayoría de los asistentes de Windows ya no tienen el Asistente para Word en el título, es aceptable hacer referencia a los asistentes como asistentes en la documentación de. Esta referencia debe estar en minúsculas.
-   **Correcto:**
-   Si está configurando una red por primera vez, puede obtener ayuda mediante el Asistente para **conectarse a una red** .
-   Algunos asistentes heredados de versiones anteriores de Windows podrían incluir el asistente en el título. Al hacer referencia a uno de esos asistentes, es aceptable usar el Asistente de \[ x \] para evitar el uso del asistente del \[ \] Asistente x.
-   Consulte una pantalla individual dentro de un asistente como página.

 

 