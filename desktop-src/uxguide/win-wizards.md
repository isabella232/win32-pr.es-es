---
title: Asistentes
description: A pesar de ese nombre fantástico y llorón, los asistentes no son realmente una forma especial de interfaz de usuario y solo tienen una determinada gama de utilidades.
ms.assetid: 122d6e65-92f0-4e8a-92f7-ecd7e90665c8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 31a9a0b4ed0c114dbdeadce7fe894bdd7da9cc099960f6ce2291e073ffdf3ef5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119029131"
---
# <a name="wizards"></a>Asistentes

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

A pesar de ese nombre fantástico y llorón, los asistentes no son realmente una forma especial de interfaz de usuario y solo tienen una determinada gama de utilidades.

Los asistentes se usan para realizar tareas de varios pasos.

![Captura de pantalla que muestra el asistente "Agregar impresora" con "What type of printer do you want to install?" (¿Qué tipo de impresora desea instalar?) .](images/win-wizards-image1.png)

![Captura de pantalla que muestra el asistente "Agregar impresora" al buscar impresoras disponibles.](images/win-wizards-image2.png)

![captura de pantalla del Asistente para agregar impresora ](images/win-wizards-image3.png)

Varios pasos de un asistente se presentan como una secuencia de páginas.

Los asistentes suelen incluir los siguientes tipos de páginas:

-   Las páginas de elección se usan para recopilar información y permitir a los usuarios tomar decisiones.
-   La página Confirmar se usa para realizar una acción que no se puede deshacer haciendo clic en Atrás o Cancelar.
-   La página Progreso se usa para mostrar el progreso de una operación larga.

El diseño del asistente moderno ofrece un nivel premium de eficiencia, lo que [](glossary.md) hace que [](glossary.md) la página Progreso sea opcional para operaciones más cortas y, a menudo, se prescinda de la página de bienvenida tradicional y la página de enhorabuena al principio y al final.

Todas las páginas del asistente tienen estos componentes:

-   Barra de título para identificar el nombre del asistente, con un botón Atrás en la esquina superior izquierda y un botón Cerrar con botones opcionales Minimizar/Maximizar y Restaurar. Tenga en cuenta que la barra de título también incluye un icono para identificarlo en la barra de tareas.
-   Una instrucción principal para explicar el objetivo del usuario con la página.
-   Área de contenido con texto opcional y posiblemente otros controles.
-   Un área de comandos con al menos un botón de confirmación para confirmar en la tarea o continuar con el paso siguiente.

Aunque un asistente tiene varios pasos, todos estos pasos deben agregarse a una sola tarea, desde el punto de vista del usuario. Este es el principio fundamental de diseño del asistente de "un asistente, una tarea".

Por lo tanto, en este artículo, una tarea es la función básica de un asistente (por ejemplo, la tarea de un asistente para la instalación es instalar un programa). Las subtaá tareas son aspectos de la tarea más grande (por ejemplo, una subta tarea de un asistente para la instalación puede ser configurar el programa que se va a instalar). Por último, cada página del asistente se considera un paso en una tarea o subta tarea determinada (por ejemplo, puede haber dos o tres pasos implicados en la configuración del programa).

**Nota:** Las instrucciones relacionadas con [la configuración,](exper-setup.md) [los cuadros de](win-dialog-box.md)diálogo y las barras [de](progress-bars.md) progreso se presentan en artículos independientes.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Se puede usar un asistente para cualquier tarea que requiera varios pasos de entrada. Sin embargo, los asistentes efectivos tienen requisitos adicionales:

-   **¿Realiza el asistente una sola tarea atómica?** No use interacciones que no sean tareas únicas (un programa completo nunca debe ser un asistente a menos que realice una sola tarea). No use asistentes para combinar tareas independientes o pasos no relacionados en gran medida.
-   **¿Se puede reducir el número de preguntas necesarias? ¿Hay valores predeterminados aceptables que funcionen bien en la mayoría de los casos o que se puedan ajustar según sea necesario más adelante? Por lo tanto, ¿se puede reducir el número de páginas?** Si es así, intente simplificar la tarea para que se pueda presentar en una sola página (por ejemplo, un cuadro de diálogo) o elimine completamente la necesidad de entrada (lo que permite que la tarea se realice directamente).
-   **¿Se deben proporcionar las preguntas necesarias secuencialmente? ¿Hay varias preguntas probables, pero opcionales?** Si es así, considere un cuadro de diálogo o un cuadro de diálogo con pestañas.

    **Correcto:**

    ![captura de pantalla del cuadro de diálogo opciones de impresión ](images/win-wizards-image4.png)

    El cuadro de PowerPoint opciones de impresión de Microsoft contiene muchas opciones de entrada de usuario, por lo que podría presentarlas en un asistente. Sin embargo, no es necesario proporcionarlos secuencialmente, por lo que un cuadro de diálogo es una mejor opción.

Los asistentes son una forma relativamente pesada de interfaz de usuario; Si hay una solución adecuada y ligera disponible, úsela.

## <a name="design-concepts"></a>Conceptos de diseño

### <a name="overuse-of-wizards"></a>Uso excesivo de asistentes

Históricamente, los asistentes difieren de la interfaz de usuario normal en que se diseñaron para ayudar a los usuarios a realizar tareas especialmente complejas (con pasos que residen en ubicaciones dispares) y, a menudo, tenían inteligencia integrada para ayudar a los usuarios a tener éxito. En la actualidad, toda la interfaz de usuario debe diseñarse para que las tareas sean lo más sencillas posible, por lo que no es necesario una interfaz de usuario especial solo para este propósito.

Sin embargo, persiste la convicción de que los asistentes son una interfaz de usuario especial, en gran medida porque se conocen como "asistentes" (mucho más creativos que, por ejemplo, "diálogos" y "ventanas de propiedades"). En su lugar, es mejor considerarlas como tareas de varios pasos y no llamar especial atención a ese hecho.

Antes de crear un asistente, tenga en cuenta si los usuarios realmente deben interrumpirse desde el flujo principal del programa. Puede haber una solución más ligera, insertada y contextual que, en última instancia, será más útil y eficaz para los usuarios. Por ejemplo, una característica mal diseñada en un programa no garantiza que un asistente la explique y simplifique. garantiza el rediseño de la propia característica. No se debe usar un asistente como ayuda de banda para corregir un problema más básico con el programa.

### <a name="wizards-do-have-appropriate-functions"></a>Los asistentes tienen las funciones adecuadas

Los asistentes son una de las claves para simplificar la experiencia del usuario. Permiten realizar una operación compleja, como la configuración de un programa, y dividirla en una serie de pasos sencillos. En cada punto del proceso, puede proporcionar una explicación de lo que se necesita y mostrar controles que permiten al usuario realizar selecciones y escribir texto.

Ciertos tipos de tareas de varios pasos se presta al formulario del asistente. Por ejemplo, en Windows, varios asistentes implican funciones de conectividad (a Internet o a la red corporativa, o a dispositivos periféricos, como impresoras y máquinas de fax).

![captura de pantalla del Asistente para conexión ](images/win-wizards-image5.png)

Conectarse a una red es una tarea típica de Windows adecuado para un asistente.

Aquí, la función del asistente es mediar entre algo conocido y estable (el sistema operativo estándar) y algo desconocido y variable (acuerdos de conectividad con una empresa telefónica o un proveedor de servicios de Internet). La complejidad de los ecosistemas informáticos es lo suficientemente importante ahora que resulta realmente útil usar asistentes para reducir esa complejidad.

Otros tipos de tareas que funcionan bien, así como los asistentes de Windows incluyen funciones de alto nivel (como el reconocimiento de escritura a mano y voz) y experiencias multimedia enriquecciones (como la configuración de opciones para crear y publicar películas). Los asistentes también se pueden implementar para tareas más básicas de varios pasos, como la solución de problemas. En resumen, si es probable que distintos usuarios quieran experimentar el programa de maneras muy diferentes, esto puede indicar la necesidad de un asistente y su capacidad para varios puntos de entrada de usuario.

Para el programa, merece la pena un poco de tiempo de diseño por adelantado para determinar qué función está atendiendo el asistente y si esa función realmente se eleva al nivel de implementación de un asistente.

### <a name="wizard-length"></a>Longitud del asistente

Las preguntas de diseño surgen de forma natural en torno al número y la organización de las páginas y las opciones. Por ejemplo:

-   ¿Hay un número óptimo de páginas para un asistente? ¿O al menos un intervalo deseable?
-   ¿El asistente debe ser conciso y simplificado para que los usuarios puedan completarlo lo antes posible?
-   ¿Debería haber más páginas que requieran menos opciones? ¿O menos páginas con más complejidad? ¿Qué diseño se considera más utilizable?
-   ¿Puede diseñar experiencias de asistente más rápidas mediante la aplicación de convenciones de interfaz de usuario como páginas con pestañas?

Microsoft solía aconsejar que los asistentes de tres páginas o menos se diseñaran como asistentes sencillos, y los de cuatro o más páginas usan un diseño de asistente avanzado (consulte las directrices de experiencia del usuario de [Windows](/previous-versions/ms997609(v=msdn.10)) de 1999). Pero los estándares de diseño del asistente actuales prescinditen de lo que había sido una de las principales diferencias entre las formas sencillas y avanzadas (el uso de las páginas De bienvenida y Enhorabuena), por lo que ahora estas categorías no son adecuadas y el número de páginas que determinan la elección de diseño parece arbitrario.

El asistente debe ser tan largo como sea necesario para la tarea. no hay ninguna directriz fija para su longitud. Un asistente de una página debe presentarse realmente como un cuadro de diálogo, por lo que es probable que dos páginas sean el formato más condensado posible para un asistente.

**Correcto:**

![captura de pantalla del cuadro de diálogo Crear disco ](images/win-wizards-image6.png)

Esta tarea tiene tan pocas opciones que presentarla como asistente sería un desperdicio. Un cuadro de diálogo es el formulario adecuado para esta interfaz de usuario.

En el otro extremo del espectro, si tiene un asistente que incluye varios puntos de decisión y ramas, y con frecuencia da lugar a que los usuarios pierdan el seguimiento de su ruta de navegación, ha superado un límite práctico y debe reducir la longitud del asistente. Como alternativa, puede dividir el asistente en varias tareas distintas.

A medida que determine la longitud más adecuada para el asistente, preste especial atención a los usuarios de destino. Los programas para los usuarios finales, como los consumidores del hogar y los trabajadores de la oficina, tienden a usar asistentes para ocultar la complejidad. los asistentes son lo más cortos posibles, con un diseño de página sencillo y limpio y valores predeterminados seleccionados previamente para tantas opciones como sea posible. Por el contrario, los asistentes o programas de servidor destinados a los profesionales de TI tienden a ser más largos y complejos. Este grupo de usuarios de destino tiene una tolerancia mucho mayor para tomar decisiones de configuración y, de hecho, puede resultar sospechoso si se oculta demasiada complejidad.

Si un asistente por naturaleza simplifica una tarea compleja, debe hacerlo de forma relativamente mínima para una audiencia técnicamente sofisticada y relativamente agresiva para una base de usuarios sin experiencia.

**Correcto:**

![captura de pantalla del Asistente para mostrar idiomas ](images/win-wizards-image7.png)

Esta página del asistente está bien diseñada para los usuarios finales porque reduce un asunto potencialmente complejo a una opción binaria lógica simple: instalar o desinstalar.

**Correcto:**

![Captura de pantalla que muestra la página "Selección de características" SQL Server el asistente "Configuración del programa de instalación".](images/win-wizards-image8.png)

En el Asistente para la instalación de Microsoft SQL Server 2008, el diseño de páginas es más ocupado y las numerosas opciones requieren más reflexión, pero la audiencia de destino son los administradores de bases de datos que esperan un control estricto de la selección de características.

Por último, preste atención a la frecuencia con la que se podría realizar la tarea concreta. Una tarea poco frecuente puede implementar un asistente más largo, mientras que las tareas frecuentes deben favorecer definitivamente la brevedad.

### <a name="branching"></a>Bifurcación

Para los asistentes más largos, es posible que deba crear ramas del flujo de tareas en las que la secuencia de páginas puede diferir según la entrada del usuario proporcionada "ascendente". La bifurcación se desasigna inherentemente para los usuarios, por lo que debe diseñar la experiencia del usuario para transmitir estabilidad. Se recomienda no más de dos puntos de decisión que provocarán la bifurcación en todo el asistente y no más de una rama anidada dentro de una sola rama.

Para obtener instrucciones sobre cómo crear una experiencia de usuario estable dentro de un asistente de bifurcación, vea [Bifurcación](#branching) en la sección Directrices de este artículo.

### <a name="providing-a-navigation-guide"></a>Proporcionar una guía de navegación

Las guías de navegación pueden ser útiles cuando hay muchos pasos en la tarea y los usuarios pueden perder su lugar en la secuencia o simplemente quieren saber cuánto tiempo se tarda en completarse.

Las guías de navegación suelen aparecer como una lista de páginas o secciones del asistente, con un aspecto un poco parecido a una tabla de contenido, en una columna o panel en el lado izquierdo de cada página. Aunque la lista persiste en todo el asistente (la misma lista de páginas aparece en cada página), hay algunos medios visuales para indicar dónde se encuentra el usuario actualmente en la secuencia (por ejemplo, mediante negrita para distinguir la página o sección activa).

Las guías de navegación pueden ser secuenciales o no secuenciales. El tipo secuencial presenta las páginas anteriores junto con las páginas futuras conocidas. Puede presentar el futuro en términos de pasos en lugar de páginas si se conocen los pasos y las páginas dependen. A continuación, puede rellenar las páginas dinámicamente a medida que se conozcan. Dado que la secuencia de navegación es fija, la guía de navegación no es interactiva.

Las guías de navegación no secuenciales son interactivas, por lo que los usuarios pueden volver a visitar las páginas vistas previamente directamente. También pueden omitir la secuencia de navegación para las páginas diseñadas para ser opcionales. Las páginas opcionales deben tener valores predeterminados que sean aceptables en la mayoría de las circunstancias. Con este tipo de guía:

-   Las páginas vistas anteriormente siempre se pueden ver directamente.
-   Es posible que las páginas futuras no se puedan ver si tienen requisitos previos.
-   Las páginas que se pueden visitar deben distinguirse visiblemente de aquellas que no se pueden (por ejemplo, mediante vínculos que están activos o deshabilitados), junto con páginas necesarias u opcionales.

Los usuarios pueden confundirse con el significado de la botón Atrás en este escenario. ¿El hecho de hacer clic en Atrás le lleva a la página o sección anterior de la guía de navegación o a la última página o sección que se ha visto? Dado Windows asistentes de botón Atrás coloca el botón Atrás en la esquina superior izquierda de las páginas del asistente, en lugar de en la esquina inferior derecha con los otros botones de confirmación, los usuarios piensen en la funcionalidad Atrás como lo hacen en la Web. Por lo tanto, la mejor solución es proporcionar a su botón Atrás el significado de la navegación web (al hacer clic en Atrás debe conducir a la última página o sección vista) y usar la guía de navegación del asistente para la navegación secuencial.

### <a name="page-integrity"></a>Integridad de la página

El diseño del asistente implica no solo las decisiones relativas a todo el flujo de tareas, como cómo controlar la navegación y la experiencia de bifurcación, sino también aquellas que pertenecen a las páginas individuales que forma el asistente. **El principio más importante para diseñar buenas páginas del asistente es el de integridad: el contenido de una página debe pertenecer juntos.**

Las páginas del asistente son mucho más fáciles de usar si cada una se queda juntas conceptualmente, tratando solo con un aspecto de la tarea general. La [instrucción principal](glossary.md) es el medio principal para lograrlo. Identifique claramente el objetivo o propósito de la página para los usuarios. [Las instrucciones complementarias](glossary.md)y los controles de la página pertenecen directamente a la instrucción principal. Aunque las páginas del asistente deben presentar a los usuarios opciones para las que se requiere alguna reflexión, ese esfuerzo no parece que funcione porque se centra estrechamente en la integridad de la propia página.

Desafortunadamente, los diseñadores de asistentes suelen confundir el rápido clic de los usuarios en el botón Siguiente como prueba de la facilidad de uso, la simplicidad y la integridad de sus páginas. La experiencia final del asistente no es Siguiente, Siguiente, Siguiente, Siguiente, Finalizar. Aunque esta experiencia sugiere que los valores predeterminados se eligieron correctamente, también sugiere que el asistente no era realmente necesario porque todas las opciones son opcionales.

En términos de objetos visuales y texto, debe reducir estos elementos a lo básico. Rechace la necesidad de agrupar varias subtades en una sola página (el "asistente para burros") o de recurrir a las pestañas para presentar requisitos de entrada complejos. Una sola página debe cubrir una sola subta tarea de la tarea general del asistente.

**Incorrecto:**

![captura de pantalla del Asistente para instalación de SQL Server ](images/win-wizards-image9.png)

Con tres pestañas de entrada de usuario bastante densas requeridas, esta página del asistente está intentando realizar demasiado.

En la mayoría de los casos, mantenga el tamaño de cada página en todo el asistente para fomentar una apariencia coherente. Aunque Windows asistentes permiten páginas de tamaño ajustable para que el tamaño de una página coincida con la cantidad de contenido, solo unos pocos hacen uso de esta opción.

Por último, mantenga los elementos estructurales de cada página del asistente a través de la secuencia. Por ejemplo, no mueva el botón Atrás de la esquina superior izquierda hacia abajo al área de botones de confirmación de una página o dos. Este nivel de coherencia de diseño ayuda a los usuarios a sentirse estables dentro del asistente. Piense en esto como una línea base para la integridad visual de una página.

### <a name="finding-the-right-level-of-communication"></a>Búsqueda del nivel correcto de comunicación

Los usuarios tienen una tolerancia baja para leer grandes bloques de texto en pantalla, y menos aún dentro de una superficie de interfaz de usuario cuyo propósito rápido es moverse rápidamente a través de una tarea.

Los asistentes tienen tendencia a comunicarse en exceso. Ocupa mucho espacio en la pantalla, lo que parece animar a una unidad a rellenar el espacio. Es como una variación de la ley de Asíns: el texto de la interfaz de usuario se expandirá para rellenar el espacio disponible.

Un responsable de este exceso es la redundancia. Debido a las plantillas usadas en el diseño inicial del asistente, el mismo idioma puede aparecer en varias ubicaciones de una página, como en la barra de título, los encabezados, el texto del cuerpo, las etiquetas de control, y así sucesivamente.

Merece la pena contratar a un editor profesional para que recorte el texto del asistente de forma incansable. Elimine preguntas y opciones innecesarias en páginas individuales y elimine las páginas enteras del asistente en su conjunto (por ejemplo, las tradicionales páginas de bienvenida y enhorabuena). Llegue directamente al punto de la página con una instrucción principal escrita concisamente, usando el lenguaje que usa el público de destino para describir la tarea, no la jerga de la tecnología o característica que usted o su equipo usan internamente. Este enfoque centrado en el usuario es fundamental para mejorar la comunicación de los asistentes del programa.

Preste especial atención al tono del asistente: a veces, las impresión más duraderas del programa no son el resultado de lo que se dice, sino de cómo se dice. En los asistentes, los usuarios se siente cómodos con un tono descriptivo y conversacional, con un uso libre del pronombre de segunda persona ("usted") cuando el programa solicita una entrada. Para obtener más instrucciones, [vea Estilo y tono.](text-style-tone.md)

La reducción del recuento de palabras en la página del asistente suele ser predecible, pero tenga cuidado de no ir demasiado lejos. Si la tarea es importante y garantiza un asistente, los usuarios aprecian tener suficiente información para tomar decisiones inteligentes. En el ejemplo siguiente se muestra cómo se puede condensar el texto del asistente sin sacrificar el significado.

**Antes:**

![captura de pantalla del asistente cleartype, borrador ](images/win-wizards-image10.png)

**Después:**

![captura de pantalla del asistente cleartype, revisada ](images/win-wizards-image11.png)

La versión editada de esta página del asistente proporciona una instrucción principal orientada a tareas, quita el párrafo explicativo innecesario debajo de la instrucción principal y revisa la etiqueta de casilla para aclarar el propósito de la casilla.

**Si solo hace tres cosas...**

1. Asigne la tarea que está intentando realizar con la interfaz de usuario adecuada para realizar el trabajo. No se limite a usar de forma predeterminada un asistente cuando cree que necesita recopilar una gran cantidad de entradas de los usuarios.

2. Piense detenidamente en la longitud y la estructura del asistente. prefiere asistentes cortos que no son de bifurcación para mantener la experiencia lo más sencilla posible, de modo que los usuarios puedan volver a su tarea principal o interés en el programa.

3. Asegúrese de la integridad de cada página del asistente: el contenido de una página debe pertenecer claramente.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Considere primero alternativas ligeras, como cuadros de diálogo, paneles de tareas o páginas únicas.** No tiene que usar asistentes: puede proporcionar información útil y ayuda en cualquier interfaz de usuario.
-   **Use asistentes para tareas de varios pasos.** Use cuadros de diálogo de varias páginas para tareas de un solo paso con comentarios. Para obtener más instrucciones, vea [Cuadros de diálogo](win-dialog-box.md).

    **Correcto:**

    ![captura de pantalla del cuadro de diálogo diagnósticos ](images/win-wizards-image12.png)

    ![captura de pantalla de comentarios del cuadro de diálogo de diagnóstico ](images/win-wizards-image13.png)

    En este ejemplo, Windows diagnóstico de red consta de páginas de progreso y resultados. Dado que la tarea es solo un paso, no requiere los botones de navegación que los usuarios necesitan en un asistente. Se presenta de forma eficaz como un cuadro de diálogo de varias páginas.

### <a name="window-size"></a>Tamaño de la ventana

-   **Elija un tamaño de ventana que pueda mostrar todas las páginas del asistente sin desplazamiento de página vertical u horizontal.** Aunque los controles de la página pueden requerir desplazamiento, las propias páginas del asistente no deben hacerlo.
-   **Tamaño de las ventanas lo suficientemente grande como para realizar sus tareas cómodamente.** El diseño de la página no debe ser reducido ni requerir que los usuarios se desplacen o cambien de tamaño excesivamente.
-   **Pero no haga que las ventanas sea demasiado grande.** Las ventanas más grandes hacen que la tarea se sienta más compleja y requiera movimiento adicional para la interacción.
-   **Use ventanas de tamaño ajustable para un asistente que pueda beneficiarse de más espacio en la pantalla, pero que no lo requiera.** Asigne un tamaño mínimo adecuado. Las ventanas de tamaño ajustable son útiles cuando las páginas requieren interactuar con contenido de tamaño ajustable, como vistas de lista grandes.

    **Correcto:**

    ![captura de pantalla del programa de instalación de Visual Studio, lista parcial ](images/win-wizards-image14.png)

    **Mejor:**

    ![captura de pantalla de configuración de Visual Studio, lista completa ](images/win-wizards-image15.png)

    En este ejemplo, el tamaño de la ventana ayuda a los usuarios a ver la lista completa.

-   **Considere la posibilidad de usar asistentes de tamaño dinámico cuyo tamaño de página cambia según sea necesario para su contenido.** Si lo hace, un asistente puede adaptarse a los diseños de página con una amplia gama de contenido.
-   **Prefiere el tamaño estático sobre dinámico si los usuarios pueden percibir los cambios como una falta de estabilidad en su experiencia del asistente.** La estabilidad visual suele ser un alojamiento de contenido. La mayoría de los asistentes deben adoptar tamaños de ventana estándar estáticos, con el tamaño dinámico reservado para casos especiales.

### <a name="wizard-length"></a>Longitud del asistente

-   **Haga que el asistente sea lo más conciso y simplificado posible.** Deshaga las opciones y preguntas innecesarias y use valores predeterminados inteligentes para reducir el número de páginas necesarias para la entrada del usuario.
    -   **Excepción:** Los profesionales de TI y otros usuarios técnicos tienen una mayor tolerancia para asistentes más largos y requisitos de entrada detallados.
-   **Haga que el asistente sea un mínimo de dos páginas.** En su lugar, se debe rediseñar un asistente de una página como un cuadro de diálogo.
-   **No reduzca el número de páginas del asistente simplemente aumentando la complejidad de cada página.** Por ejemplo, una página del asistente que incluye tres pestañas que requieren la entrada del usuario se debe rediseñar como tres páginas independientes.
-   **No aumente el número de páginas del asistente haciendo que cada página sea tan sencilla que los usuarios haga clic sin sentido en Siguiente a través de toda la secuencia.** Se trata de un error de diseño de asistente común. Si una página del asistente no requiere al menos cierto grado de reflexión, probablemente no tenga que estar en el asistente.

### <a name="branching"></a>Bifurcación

-   **Prefiere el diseño del asistente que no es de bifurcación en lugar de la bifurcación.** Los asistentes que no son de bifurcación tienden a ser más sencillos, más cortos y fáciles de navegar. Los asistentes para bifurcación dificultan a los usuarios determinar cuántos pasos de la tarea y dónde se encuentran en la secuencia.
-   **Si debe bifurcar, ayude a los usuarios a orientarse mediante una de las técnicas siguientes:**
    -   **Enumerar páginas.** Una técnica común consiste en indicar la ubicación del usuario en la secuencia de cada página, como con la frase Paso X de Y. Asegúrese de que el punto de conexión (Y) es estable. Si cambia de valor, esto vulnera la confianza de los usuarios.
    -   **Incluya la noción de subescales** (como el paso 2a de 6).
    -   **Realice pasos independientes de las páginas, donde cada paso puede implicar varias páginas.** Por ejemplo, un servicio de viajes podría emplear una organización asistente basada en convenciones de comercio electrónico bien establecidas para el sector.

        **Correcto:**

        ![captura de pantalla de la organización del asistente basado en pasos ](images/win-wizards-image16.png)

        Las etiquetas lógicas pueden proporcionar una orientación adecuada para los usuarios de un asistente de bifurcación.

    -   **Trate los pasos opcionales como persistentes en la secuencia de enumeración.** Por ejemplo, si una rama simplemente omite algunos pasos opcionales, simplemente omita los pasos de los comentarios también, en lugar de volver a numerar. Por lo tanto, si un usuario toma una decisión en la página 2 que da como resultado que las páginas 3 y 4 son opcionales, muestre los pasos 1, 2, 5 y 6 de 6. No vuelva a numerar los pasos 5 y 6.
    -   **Si el asistente emplea una sola rama y la rama se produce al principio de la tarea, inicie la secuencia en ese momento y, a continuación, simplemente use el enfoque que no es de bifurcación.** Es decir, a partir del punto de la rama, progresa en secuencia hasta el final de la rama.

-   **Si debe bifurcar, limite el número de ramas a una o dos dentro de un solo asistente.** No incluya nunca más de una rama dentro de una rama (una rama "anidada").

### <a name="commit-buttons"></a>Botones de confirmación

-   **Cuando los usuarios confirmen** una tarea, use un botón de confirmación que sea una respuesta específica a la instrucción principal (por ejemplo, Imprimir, Conectar o Iniciar). No use etiquetas genéricas como Siguiente (que no implica compromiso) o Finalizar (que no es específico) para confirmar una tarea. Las etiquetas de estos botones de confirmación deben tener sentido por sí solas. Inicie siempre las etiquetas de botón de confirmación con un verbo. **Excepciones:**
    -   Use Finalizar cuando las respuestas específicas siguen siendo genéricas, como Guardar, Seleccionar, Elegir u Obtener.
    -   Use Finalizar para cambiar una configuración específica o una colección de configuraciones.
-   **Un solo asistente puede tener varios puntos de confirmación, pero se prefiere un único punto.**
-   **Si es necesario, puede cambiar el nombre u ocultar los botones de confirmación en una página.** Esta flexibilidad es una ventaja del nuevo diseño del asistente en Windows que no estaba disponible en los asistentes anteriores. Tenga en cuenta que ocultar un botón de confirmación es diferente de deshabilitarlo.
-   **Evite deshabilitar un botón de confirmación positiva.** De lo contrario, los usuarios tienen que deducir por qué los botones de confirmación están deshabilitados. Es mejor dejar habilitados los botones de confirmación y proporcionar un mensaje de error útil cada vez que surja un problema. Deshabilitar el botón solo es aceptable si el motivo para hacerlo es obvio e inequívoco.
-   **No confunda los botones de navegación (Siguiente y Atrás) con los botones de confirmación.** Siguiente significa avanzar en el asistente sin compromiso; Atrás siempre debe estar disponible en la página siguiente y, al hacer clic en Atrás, se debe deshacer el efecto del último botón Siguiente. Si esto no es posible, los usuarios están realizando un compromiso, que se indica a través de una etiqueta específica en el botón de confirmación. Para obtener más instrucciones sobre los botones Siguiente y Atrás, vea [Navegación.](#providing-a-navigation-guide)

### <a name="cancel-buttons"></a>Botones cancelar

-   **No pida a los usuarios que confirmen si realmente pretenden cancelar.** Si lo hace, puede ser molesto. **Excepciones:**
    -   La acción tiene consecuencias significativas y, si es incorrecta, no se puede corregir fácilmente.
    -   La acción puede provocar una pérdida significativa del tiempo o el esfuerzo del usuario.
    -   La acción es claramente incoherente con otras acciones.
-   **Permitir que los usuarios reinicien los asistentes en caso de que se cancelen por error.**
-   **No deshabilite el botón Cancelar. Excepciones:**
    -   Si la cancelación es dañina, podría ser el caso al realizar una tarea en asistentes independientes.
    -   Si la cancelación es imposible, podría ser el caso cuando el asistente no tiene control sobre todos los pasos.

### <a name="close-buttons"></a>Botones cerrar

-   **Use Cerrar para las páginas Follow-Up y Finalización.** No use Cancelar, ya que cerrar la ventana no abandonará los cambios ni las acciones que se realicen en este momento. No use Listo, porque no es un verbo imperativo.
-   **Una vez realizada la tarea, Cancelar debe convertirse en Cerrar (para asistentes independientes).** El efecto de Cerrar es simplemente cerrar la ventana.

### <a name="other-controls"></a>Otros controles

-   **Use vínculos de comandos solo para las opciones, no los compromisos.** Los botones de confirmación específicos indican un compromiso mucho mejor que los vínculos de comandos de un asistente.
-   **Al usar vínculos de comandos, oculte el botón Siguiente, pero deje el botón Cancelar.**

### <a name="using-pages-vs-dialog-boxes-or-inline-ui"></a>Usar páginas (frente a cuadros de diálogo o interfaz de usuario insertadas)

-   **En general, se prefieren las páginas a los cuadros de diálogo.** Los usuarios esperan que los asistentes se basen en páginas.
-   **Use cuadros de diálogo para ayudar a completar páginas, como** con selectores de objetos y exploradores.
-   **Use cuadros de diálogo para proporcionar mensajes de error que se aplican a toda la página y como resultado de hacer clic en un botón de confirmación.**
-   **Use la presentación insertada para comportamientos dinámicos simples, como** la divulgación progresiva y la interfaz de usuario contextual.
-   **Use la presentación en línea para los mensajes de error que se aplican a controles específicos.**

### <a name="wizard-pages"></a>Páginas del asistente

-   **Céntrate en la toma de decisiones eficaz.** Reduzca el número de páginas para centrarse en lo esencial. Consolide las páginas relacionadas y saque las páginas opcionales del flujo principal. Hacer que los usuarios haga clic en Siguiente por completo a través del asistente puede parecer una buena experiencia al principio, pero si los usuarios nunca necesitan cambiar los valores predeterminados, es probable que las páginas no sean necesarias.
-   **Diseñe cada página para que tenga un único propósito y coherencia visual.** Para obtener más información, vea [Integridad de página.](#page-integrity)
-   **No use páginas de bienvenida: haga que la primera página sea funcional siempre que sea posible.** Use una página de Tareas iniciales opcional solo cuando:

    -   El asistente tiene requisitos previos necesarios para completar el asistente correctamente.
    -   Es posible que los usuarios no comprendan el propósito del asistente en función de su primera página de elección y no hay espacio para más explicaciones.
    -   La instrucción principal para Tareas iniciales páginas es "Antes de comenzar:".

    **Incorrecto:**

    ![captura de pantalla de la página de bienvenida de la configuración del punto de mapa ](images/win-wizards-image17.png)

-   Los asistentes modernos optan por las primeras páginas funcionales. Aquí no hay nada que hacer, pero haga clic en Siguiente. ¿Por qué obligar a los usuarios a pagar este impuesto de token por su valioso tiempo?
-   **En las páginas en las que se pide a los usuarios que to elijan, optimice para los casos más probables.** Estos tipos de páginas deben presentar opciones reales, no solo instrucciones.
    -   Si no usa una página de Tareas iniciales, explique el propósito del asistente en la parte superior de la primera página de opciones.
-   **Use las páginas de confirmación para dejar claro cuándo los usuarios confirman la tarea.** Normalmente, la página Confirmar es la última página de opciones y el botón Siguiente se vuelve a etiquetar para indicar la tarea que se está confirmando.
    -   No use páginas de resumen que simplemente resuman las selecciones anteriores del usuario, a menos que la tarea sea arriesgada (que implique seguridad o pérdida de tiempo o dinero) o que haya una buena probabilidad de que los usuarios necesiten revisar sus selecciones.
-   **Use las páginas progreso para mostrar el estado de una operación larga.** Una vez completada correctamente, la página de progreso debe avanzar automáticamente al paso siguiente. Solo debe permanecer en la página de progreso si hay un problema que el usuario necesita ver. Hacer clic en Volver a una página de progreso no debe tener ningún efecto secundario.
    -   **Use una sola barra de progreso determinada.** Siga las [directrices de la barra de progreso determinadas,](progress-bars.md)entre las que se incluyen:
        -   Indique claramente la finalización. No permita que una barra de progreso vaya al 100 % a menos que se haya completado la operación.
        -   No reinicie el progreso. Una barra de progreso pierde su valor si se reinicia (quizás porque se completa un paso de la operación) porque los usuarios no tienen forma de saber cuándo se completará la operación. En su lugar, haga que todos los pasos de la operación compartan una parte del progreso y que la barra de progreso se complete una vez.
    -   **Proporcione una descripción concisa del paso actual encima de la barra de progreso.** Para las operaciones rápidas, este texto no es necesario; la barra de progreso por sí sola es suficiente. Para las operaciones que requieren un minuto o más, el texto puede ser útil.
        -   Use fragmentos de oración, normalmente empezando por un verbo y terminando con puntos suspensivos. Ejemplos: Copiar archivos..., Instalar los componentes necesarios...
        -   Coloque el texto encima de la barra, no debajo.
        -   **Incorrecto:**
        -   ![captura de pantalla de la barra de progreso con el texto siguiente ](images/win-wizards-image18.png)
        -   En este ejemplo, el texto explicativo debe aparecer encima de la barra de progreso.
        -   Evite abarrote la página de progreso con detalles innecesarios. Esta página no es para soporte técnico; es para los usuarios.
        -   **Incorrecto:**
        -   ![captura de pantalla de la barra de progreso con demasiados detalles ](images/win-wizards-image19.png)
        -   En este ejemplo, los detalles técnicos, como los GUID, no tienen sentido para los usuarios.
-   **No use páginas de enhorabuena que no hagan nada más que finalizar el asistente.** Si los resultados del asistente son claramente evidentes para los usuarios, cierre el asistente en el botón de confirmación final.
    -   Use Follow-Up cuando haya tareas relacionadas que es probable que los usuarios realicen como seguimiento. Evite tareas de seguimiento conocidas, como "Enviar un mensaje de correo electrónico".
    -   Use las páginas de finalización solo cuando los resultados no sean visibles y no haya ninguna manera mejor de proporcionar comentarios para la finalización de la tarea.
    -   Los asistentes que tienen páginas de progreso deben usar una página Finalización Follow-Up página para indicar la finalización de la tarea. Para las tareas de ejecución larga, cierre el asistente en la página Confirmar y use notificaciones para enviar comentarios.
-   **Use páginas de resumen solo si la entrada es compleja y los usuarios deben revisar, si la tarea implica un riesgo significativo (por ejemplo, una transición financiera) o si el asistente realizará acciones en función de la entrada del usuario que no sea obvia (para generar confianza a través de la transparencia).** A menudo, las páginas de resumen no cumplen esta barra de relevancia y se pueden omitir.
-   **Use páginas de error si el asistente no se puede completar debido a un problema desde el que no es posible la recuperación.** En esta página, explique cuál es el problema en lenguaje claro, sin jerga técnica que los usuarios no comprenderán. Proporcione también los pasos prácticos que los usuarios pueden seguir para resolver el problema. Para obtener más instrucciones, vea [Mensajes de error](mess-error.md).
    -   **Excepción:** Si el asistente se completa con un problema menor desde el que es posible la recuperación, presente el problema como una tarea adicional en lugar de un error. Use un lenguaje positivo, orientado al éxito y alentador, no términos como error, error o problema. No use un icono de error.

### <a name="navigation"></a>Navegación

-   **Use Siguiente solo al avanzar a la página siguiente sin compromiso.** Avanzar a la página siguiente se considera un compromiso cuando su efecto no se puede deshacer haciendo clic en Atrás o Cancelar.
-   **Use Atrás solo para corregir errores.** Además de corregir errores, los usuarios no deben tener que hacer clic en Atrás para avanzar en una tarea.
-   **Conservar las selecciones de usuario a través de la navegación.** Por ejemplo, si el usuario realiza cambios, hace clic en Atrás y, a continuación, en Siguiente, esos cambios se deben conservar. Los usuarios no esperan tener que volver a escribir los cambios a menos que elijan explícitamente borrarlos.
-   **No deshabilite el botón Atrás a menos que repetir los pasos sea perjudicial.**
-   **Permitir que los usuarios examinen o revisen las opciones en los siguientes escenarios de navegación:**
    -   El usuario proporciona entrada, hace clic en el botón confirmar, hace clic en Atrás para revisar los cambios anteriores, no cambia nada y, a continuación, vuelve a hacer clic en el botón confirmar. Normalmente, esto debería ser posible y la segunda confirmación debería avanzar a la página siguiente (porque la tarea ya se ha realizado).
    -   El usuario proporciona entrada, hace clic en el botón confirmar, hace clic en Atrás para revisar los cambios anteriores, cambia algo y, a continuación, vuelve a hacer clic en el botón confirmar. Normalmente, esto debería ser posible y la segunda confirmación debe rehacer la tarea con la entrada cambiada (reemplazando o deshaciendo el efecto de la primera).

### <a name="help"></a>Ayuda

-   **Páginas del asistente de diseño para proporcionar información suficiente para que no sea necesaria la referencia a la documentación del programa Ayuda.** Un asistente ya está alejando a los usuarios de su interacción deseada y directa con el programa. requerir a los usuarios que busquen ayuda externa los quita aún más de este estado. La ayuda debe ser la excepción, no la regla.
-   **Si debe proporcionar un punto de acceso a la Ayuda, use un vínculo en la parte inferior izquierda del área de contenido de la página (encima del área de comandos).** Este vínculo debe ser breve y normalmente debe incluirse en forma de pregunta que es más probable que los usuarios quieran responder.
-   **Correcto:**
-   ![captura de pantalla de la página del asistente con el vínculo de ayuda ](images/win-wizards-image5.png)
-   Este vínculo a la Ayuda es adecuado porque la información básica básica como esta abarrote demasiado la página del asistente.

## <a name="text"></a>Texto

### <a name="general"></a>General

-   Use usted y su para hacer referencia al usuario y al equipo del usuario, al documento, a la configuración, entre otros. No use la primera persona (I, my) para hacer referencia al equipo o al asistente. Sin embargo, es aceptable usar la primera persona en las opciones que el usuario selecciona. **Ejemplo: casilla Solo uso.**
-   Cada página del asistente debe tener [una instrucción principal](glossary.md).

### <a name="titles"></a>Títulos

-   Coloque el nombre del asistente en la barra de título. Use [el uso de mayúsculas de estilo de título.](glossary.md)
-   Los títulos no deben incluir signos de puntuación, excepto los que tienen signos de interrogación.
-   No incluya la palabra Asistente en los títulos del asistente. Por ejemplo, use Conectar a una red en lugar de red Asistente para instalación.

### <a name="buttons"></a>Botones

-   No incluya texto en el botón Atrás. Use el glifo de flecha en su lugar, sin etiquetar.
-   Incluya texto en el botón Siguiente. No use glifos (como > o >>) además de la palabra Siguiente.
-   Use etiquetas de botón de confirmación específicas que tienen sentido por sí solas y son una respuesta a la instrucción principal. Lo ideal es que los usuarios no tengan que leer nada más para comprender la etiqueta. Es mucho más probable que los usuarios lean las etiquetas del botón de comando que el texto estático.
-   Si es posible, no use la palabra Finalizar para la etiqueta del botón de confirmación, ya que normalmente hay un botón de confirmación mejor y más específico:
    -   Si al hacer clic en el botón se confirma en la tarea (por lo que aún no se ha realizado la tarea), use una etiqueta específica que comience con un verbo que sea una respuesta a la instrucción principal (ejemplos: Imprimir, Conectar, Iniciar).
    -   Si la tarea ya se ha realizado en el asistente, use Cerrar en su lugar.

        **Excepciones:**

        -   Puede usar Finalizar cuando la etiqueta específica sigue siendo genérica, como Guardar, Seleccionar, Elegir u Obtener.
        -   Puede usar Finalizar cuando la tarea implica cambiar una configuración o una colección de valores.

-   Inicie las etiquetas de botón de confirmación con un verbo. Las excepciones son Ok, Yes y No.
-   Use [mayúsculas y mayúsculas de estilo oración.](glossary.md)
-   No uses puntuación final.

## <a name="documentation"></a>Documentación

-   Aunque la mayoría Windows asistentes ya no tienen la palabra Asistente en el título, es aceptable hacer referencia a los asistentes como asistentes en la documentación. Esta referencia debe estar en minúsculas.
-   **Correcto:**
-   Si va a configurar una red por primera vez, puede obtener ayuda mediante el asistente **Conectar a una** red.
-   Algunos asistentes heredados de versiones anteriores de Windows pueden incluir el Asistente en el título. Al hacer referencia a uno de esos asistentes, es aceptable usar el Asistente X para evitar decir el Asistente \[ \] para \[ \] X.
-   Consulte una pantalla individual dentro de un asistente como una página.

 

 