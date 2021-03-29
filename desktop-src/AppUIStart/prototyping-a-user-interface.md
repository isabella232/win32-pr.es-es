---
title: Prototipo de una interfaz de usuario
description: En este tema se explica cómo el prototipo de una interfaz de usuario puede ayudar a minimizar los errores de diseño y garantizar una experiencia de usuario correcta.
ms.assetid: 16e3fabb-9cd1-4517-8f19-b1d80c956ee0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148c01d31c3bee34b555ab2ce10565229a7d1fb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993826"
---
# <a name="prototyping-a-user-interface"></a>Prototipo de una interfaz de usuario

En este tema se explica cómo el prototipo de una interfaz de usuario puede ayudar a minimizar los errores de diseño y garantizar una experiencia de usuario correcta.

## <a name="introduction"></a>Introducción

A veces, a medida que un proyecto avanza, las suposiciones pequeñas y las decisiones bien intencionadas pero deficientes se acumulan, lo que convierte las horas de trabajo en una experiencia de usuario de Lousy. Los equipos inteligentes eliminan los errores antes de enviarlos mediante una técnica denominada prototipo de interfaz de usuario. En combinación con los estudios de facilidad de uso, los prototipos mantienen los equipos en la dirección correcta.

## <a name="why-prototype"></a>¿Por qué prototipo?

La forma de crear prototipos es un medio para explorar ideas antes de invertir en ellas. Todos los Craftspeople y ingenieros experimentados crean prototipos de su trabajo antes de crear nada: los arquitectos crean modelos sin papel o cartón, o con herramientas de realidad virtual. Los ingenieros de Aeronautic usan túneles de viento. Los creadores de puentes crean modelos de esfuerzo. Los diseñadores web y de software crean simulacros de cómo interactuarán los usuarios con sus diseños.

La mejor razón para el prototipo es ahorrar tiempo y recursos. El valor de un prototipo es que se trata de una fachada, como un conjunto de Hollywood, donde solo se construye la parte frontal del edificio. En relación con el producto real, los prototipos son fáciles y económicos de crear. Por lo tanto, para una inversión mínima, se pueden encontrar problemas de facilidad de uso y diseño y la interfaz de usuario se ajusta antes de que se realice una inversión sustancial en el diseño y las tecnologías finales.

En el examen de las necesidades de un proyecto determinado, es posible que se encuentren las razones para crear un prototipo que no sea el ahorro de dinero. ¿Es el objetivo de explorar un nuevo modelo de interfaz? ¿Realizar modificaciones en una parte del diseño existente? ¿Investigar una nueva tecnología? Antes de comenzar, es importante tener claro por qué está compilando lo que está compilando. Comenzar con objetivos claros ayuda a hacer que el esfuerzo sea directo y eficaz. Los motivos para crear prototipos se dividen en tres categorías básicas:

-   Prueba de concepto.

    Entre algunos equipos hay desacuerdos sobre la dirección futura de un proyecto. Se puede usar un prototipo para demostrar que una idea o un enfoque nuevo tiene mérito o valor. Un prototipo puede ayudar a ilustrar que una idea funciona, expresar sus cualidades de forma visual e interactiva, y/o motivar a los miembros del equipo a pensar en el problema desde otra perspectiva.

-   Exploración del diseño.

    Si diseña software interactivo, la única manera de explorar cómo se va a usar es crear una maqueta e interactuar con ella. A veces, el simulacro está asociado a un estudio de facilidad de uso, donde las partes del prototipo se pueden evaluar de forma estructurada. A veces, es simplemente una manera de expresar claramente a un desarrollador cómo debe funcionar o buscar algo. En muchos casos, es posible que un diseñador simplemente esté experimentando, en un esfuerzo por tener una idea de qué enfoque podría funcionar. Cualquier persona del equipo puede utilizar prototipos para explorar problemas de diseño, aunque los diseñadores suelen ser los más experimentados. Las exploraciones de diseño deben dirigirse para intentar resolver problemas específicos que se reconocen en el producto.

-   Exploración técnica.

    Los desarrolladores que investigan los enfoques de implementación de un problema con frecuencia prueban distintas técnicas de codificación para ver si funcionan bien. El uso de COM+, HTML dinámico (DHTML), Microsoft Win32 o enfoques de codificación específicos dentro de cada tecnología tienen diferentes inconvenientes. A veces, un prototipo representa una exploración en qué tecnología funcionará bien para admitir una determinada característica de la interfaz de usuario.

A veces se crean prototipos para una combinación de estos motivos. Si un equipo tiene un diseño bastante bueno, puede asignar tiempo para que un desarrollador y un diseñador o administrador de proyectos trabajen juntos en un prototipo. En tales casos, es muy importante definir claramente los objetivos y las contribuciones que cada miembro del equipo espera que realice. Todo el mundo debe estar claro sobre cuáles son los objetivos, qué es lo que está en juego y cuál será el resultado potencial.

## <a name="who-is-involved"></a>¿Quién está implicado?

Los prototipos se pueden realizar de manera informada por cualquiera, independientemente de su fondo o rol en el proyecto. Es fácil crear un prototipo sencillo pero eficaz tomando un mapa de bits de Adobe Photoshop, poniéndolo en la herramienta de creación y administración de sitios web de Microsoft FrontPage y agregando botones o vínculos activos. Estos prototipos ligeros solo van hasta ahora y pueden resultar difíciles de manejar para interacciones complejas.

En el caso de los equipos más grandes, un desarrollador o un jefe de proyecto suele colaborar con un diseñador y un ingeniero de facilidad de uso. Juntos generarán ideas, crearán un prototipo que represente las mejores ideas y, a continuación, entrarán en el laboratorio para ver su eficacia en la solución de problemas de los usuarios. Es posible que los desarrolladores participen en caso de que puedan inutilizar el tiempo o si se necesita su experiencia técnica. A menudo, el diseñador o el jefe de proyecto realizarán la mayoría de los scripts o la codificación para compilar el prototipo.

## <a name="when-should-a-prototype-be-built"></a>¿Cuándo se debe compilar un prototipo?

Según el ámbito del prototipo y el nivel de detalle requerido, los prototipos se pueden crear en cualquier momento durante el proyecto. Lo más frecuente es que se creen pronto en el proyecto, durante la fase de planeación y especificación, antes de que los desarrolladores escriban código de producción. Es decir, cuando la necesidad de la exploración es mayor y cuando la inversión de tiempo necesaria es más viable. Si los desarrolladores en lugar de los administradores o diseñadores de programas son prototipos, el tiempo de programación es aún más importante debido a la necesidad de asegurarse de que el trabajo invertido en el prototipo se tenga en cuenta en la programación de desarrollo. La planeación de cualquier versión de la interfaz de usuario debe incluir algún nivel de prototipo.

En tarde un proyecto, los prototipos más pequeños pueden ayudar a resolver problemas técnicos y de diseño difíciles. Una maqueta rápida HTML de cómo debe comportarse un cuadro de diálogo o una página web puede ayudar a responder a la pregunta de un desarrollador o dar a otros compañeros de soporte una idea de lo que debería ser la experiencia deseada. En algunos casos, un administrador de programas o diseñador seguro puede implementar el comportamiento en el software de desarrollo de Microsoft JScript y aproximar gran parte de la lógica de programación que los desarrolladores deben considerar.

El tiempo que se tarda en crear un prototipo puede variar enormemente, en función del ámbito y la precisión de lo que debe tener el resultado final. Un prototipo informal podría significar pocas horas de trabajo de una persona; un esfuerzo más organizado puede implicar semanas de esfuerzo por todo un equipo.

## <a name="where-should-the-focus-be"></a>¿Dónde debe ser el foco?

En un prototipo, compile solo la parte del diseño que sea necesaria. Es correcto tener botones que no funcionan o texto que nunca se actualiza. Siempre que se puedan experimentar las interacciones necesarias, es adecuado usar el humo y los reflejos para el resto. Estas son algunas de las razones por las que los esfuerzos deben centrarse cuidadosamente:

-   Costo de crear el prototipo.

    Se debe minimizar el costo implicado en la generación del prototipo. El reto con la realización de prototipos es reconocer la inversión mínima necesaria para responder de forma eficaz a las preguntas sobre el diseño. Aquí es donde los estudios de facilidad de uso son críticos, ya que identifican claramente las partes de la interfaz de usuario que necesitan más trabajo. Incluso sin estudios de facilidad de uso, defina claramente qué problemas de usuario se están resolviendo o qué tareas se están mejorando con el diseño del prototipo.

-   Duración limitada.
-   Los prototipos deben tener una duración claramente definida. ¿Es el objetivo final una presentación en una reunión de equipo? ¿Una reunión de revisión Ejecutiva? ¿Una revisión de la especificación? ¿Un estudio de uso? ¿Identificar que el diseño resuelve un problema del usuario? Una vez que se cumplan las necesidades de estos objetivos específicos, se debe reservar el prototipo. La mentalidad básica es que el código o los mapas de bits generados en un prototipo se dejarán atrás. Puede haber excepciones en las que el código o los objetos visuales estén activos en el producto, pero la expectativa debe ser que este no sea el caso.
-   Riesgo de abrumar al equipo.

    La visualización de prototipos para desarrolladores y compañeros puede resultar complicada. Un prototipo demasiado complejo o elaborado, fantásticos objetos visuales y animaciones, puede abrumar a las personas. Tenga en cuenta siempre el grado de avance y la cantidad del prototipo que debe tomarse en serio.

## <a name="what-is-the-scope"></a>¿Cuál es el ámbito?

A medida que se determine el enfoque de la elaboración de prototipos, tenga en cuenta lo siguiente:

-   Necesidades del cliente.

    A partir de una descripción de los problemas clave o de las necesidades de los usuarios (quizás algo que haya proporcionado un ingeniero de uso) proporciona una idea sobre qué partes del diseño de la interfaz de usuario garantizan la mayor parte de la exploración.

-   Tareas de estudio de facilidad de uso.

    Si crea el prototipo para un estudio de facilidad de uso, hable con el ingeniero de facilidad de uso de las tareas específicas que formarán parte del estudio y diseñe los elementos.

-   Entrada del equipo.

    Hable con los principales desarrolladores del equipo a medida que las ideas del prototipo están juntas. Obtenga una idea básica de lo razonable, lo que es posible y lo que más se debe tener en cuenta en la próxima versión. En algunos casos, considere la posibilidad de ir más allá de lo que dicen es posible para un aspecto del diseño si es un punto clave y el equipo debe ser un desafío. Sin embargo, no lo haga con todos los aspectos del prototipo, ya que hay una línea fina entre la inserción de los límites y la sobrecarga de su equipo. Si el deseo es inspirar al equipo mostrándole una visión de varias versiones, entonces, vaya a ella. Sin embargo, si el requisito es definir cambios específicos para la próxima versión, céntrese en los cambios. Asegúrese de llamar a los cambios específicos de una forma modular y de mostrar a los desarrolladores una ruta de acceso para crear los diseños.

-   Amplitud frente a profundidad.

    En el caso de los prototipos más grandes, existe una consideración adicional de amplitud frente a profundidad. ¿Debe funcionar cada característica del diseño solo un poco o se debe elegir una característica para el prototipo con casi todas sus partes y opciones? Intente no hacer ambas cosas, ya que el resultado puede ser un prototipo grande y poco manejable que es difícil de modificar y difícil de quitar.

## <a name="flexible-prototypes"></a>Prototipos flexibles

Una manera de centrarse en los recursos de prototipos es concentrarse en el diseño inteligente. Se pueden crear prototipos más eficaces permitiendo que un fragmento de código de prototipo ejerza muchas ideas diferentes. En lugar de tener cinco prototipos diferentes, considere la posibilidad de crear un prototipo que tenga las opciones para cambiar los distintos atributos del prototipo.

¿La barra de herramientas debe estar situada a la izquierda o en la parte superior? ¿Deben mostrarse 10 elementos en la Página principal o en 20? Un buen prototipo tiene algún tipo de panel de opciones integrado que le permite cambiar los parámetros de aspecto o funcionamiento del prototipo. Mantener estos paneles de opciones ocultos en el prototipo: Intente evitar que un participante de facilidad de uso los encuentre involuntariamente durante una prueba.

El reto es mantener el prototipo sencillo, pero seguir siendo bastante útil para que se pueda mostrar a un compañero, se pueden demostrar opciones diferentes y se pueden obtener comentarios.

## <a name="beta-vs-prototype"></a>Versión beta frente a prototipo

Las versiones beta no se califican como prototipos, ya que son esfuerzos de ingeniería completos. Si se encuentra un error crítico en una característica de una versión beta, no es probable que se descarte, aunque pueda ser el mejor interés del producto. Los desarrolladores, evaluadores y diseñadores ya han invertido mucho tiempo y la presión de vivir con malas decisiones es muy alta. Las versiones beta ciertamente ayudan en la búsqueda de errores y defectos, pero rara vez son útiles para realizar estudios controlados del valor de las direcciones de diseño específicas.

## <a name="tools-and-technologies"></a>Herramientas y tecnologías

Hay varias herramientas y tecnologías diferentes que se pueden usar para crear prototipos, cada una de las cuales tiene sus ventajas y desventajas. Tenga en cuenta el tipo de trabajo de diseño que se está creando como prototipo y los objetivos del proceso de prototipo antes de decidir qué herramienta o tecnología es la adecuada.

-   Microsoft Visual Basic o C#.

    Esta es la tecnología más rápida para crear prototipos de interfaz de usuario de estilo Windows. El objeto de explorador Web facilita la integración de HTMLUI con componentes estándar de Windows. Aunque es cierto que un desarrollador experimentado con Microsoft Visual Studio podría generar la interfaz de usuario más rápido en C/C++, esto crea la tentación de reutilizar el código del prototipo de interfaz de usuario en el código de producción. Requiere una disciplina para reconocer que los objetivos de un prototipo de interfaz de usuario rápido y modificado son muy divergentes de la ingeniería de alta calidad. Asegúrese de que está claro qué tipo de código se está escribiendo y que el equipo o el administrador comprende lo que se descartará.

-   Microsoft Expression Blend + SketchFlow.

    SketchFlow es una herramienta visual para diseñar, crear prototipos y crear interfaces de usuario sofisticadas para Windows Presentation Foundation (WPF) y aplicaciones web y de escritorio de Microsoft Silverlight. Las aplicaciones se crean dibujando formas, dibujando controles, como botones y cuadros de lista, haciendo que las partes de una aplicación respondan a los clics del mouse y otros datos proporcionados por el usuario, y aplicando el estilo de todo para que sea único.

-   Adobe Director o Adobe Flash.

    Director es una popular herramienta de prototipo de interfaz de usuario entre diseñadores. Es más útil para los diseños de GUI no estándar o multimedia, o para los prototipos que requieren una animación significativa. Su alta flexibilidad hace que sea complicado para la interfaz de usuario de estilo de la interfaz de usuario en comparación con Visual Basic. Sin embargo, un usuario de Director experto puede generar Windows o la interfaz de usuario Web sin dificultad.

-   HTML.

    FrontPage y otros editores HTML permiten la creación rápida de prototipos simples. Para expresar una idea, a menudo es posible crear mapas de bits que ilustren una secuencia de interacción con el usuario y colocarlos en FrontPage. Estas imágenes se pueden usar para simular la interacción con el diseño. JScript y DHTML llevan cosas a otro nivel, lo que permite una lógica e interacción muy sofisticadas. Si usa HTML para generar prototipos de un sitio web, la advertencia que se acaba de describir para C/C++ también se aplica aquí; no se incluye en el reventado de código de prototipo rápido confuso con ingeniería de calidad de producción.

 

 




