---
title: Creación de prototipos de Interfaz de usuario
description: En este tema se explora cómo la creación de prototipos de una interfaz de usuario puede ayudar a minimizar los errores de diseño y garantizar una experiencia de usuario correcta.
ms.assetid: 16e3fabb-9cd1-4517-8f19-b1d80c956ee0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce42ad4240c3a06716f0db851e98b31e713b1ce0e23d1d485bc3e154375d9e50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507445"
---
# <a name="prototyping-a-user-interface"></a>Creación de prototipos de Interfaz de usuario

En este tema se explora cómo la creación de prototipos de una interfaz de usuario puede ayudar a minimizar los errores de diseño y garantizar una experiencia de usuario correcta.

## <a name="introduction"></a>Introducción

A veces, a medida que un proyecto avanza, se acumulan pequeñas suposiciones y decisiones bien intencionadas pero deficientes, lo que convierte las horas de trabajo en una experiencia de usuario pésima. Los equipos inteligentes eliminan sus errores antes de enviarse mediante una técnica denominada creación de prototipos de interfaz de usuario. Combinados con los estudios de facilidad de uso, los prototipos mantienen a los equipos en la dirección correcta.

## <a name="why-prototype"></a>¿Por qué prototipo?

La creación de prototipos es un medio de explorar ideas antes de invertir en ellas. Todos los ingenieros y los arquitectos experimentados crean prototipos de su trabajo antes de crear nada: los arquitectos crean modelos sin papel o con herramientas de realidad virtual. Los ingenieros de ingeniería usan túneles de viento. Los generadores de puentes crean modelos de esfuerzo. Los diseñadores web y de software crean simulaciones de cómo interactuarán los usuarios con sus diseños.

La mejor razón para crear prototipos es ahorrar tiempo y recursos. El valor de un prototipo es que se trata de una fachada, como un conjunto deImos, donde solo se construye la parte frontal del edificio. En relación con el producto real, los prototipos son fáciles y económicos de crear. Por lo tanto, para una inversión mínima, se pueden encontrar problemas de facilidad de uso y diseño y ajustar la interfaz de usuario antes de realizar una inversión sustancial en el diseño y las tecnologías finales.

Al examinar las necesidades de un proyecto determinado, se pueden encontrar razones para crear un prototipo que no sea ahorrar dinero. ¿El objetivo es explorar un nuevo modelo de interfaz? ¿Realizar modificaciones en una parte del diseño existente? ¿Investigar una nueva tecnología? Antes de empezar, es importante tener claro por qué está creando lo que está creando. Comenzar con objetivos claros ayuda a hacer que el esfuerzo sea directo y eficaz. Las razones para crear prototipos se divide en tres categorías básicas:

-   Prueba de concepto.

    Entre algunos equipos hay discrepancias sobre la dirección futura de un proyecto. Se puede usar un prototipo para demostrar que una idea o un nuevo enfoque tienen un valor o un valor. Un prototipo puede ayudar a ilustrar que una idea funciona, expresar sus calidades de forma visual e interactiva, o motivar a los miembros del equipo a pensar en el problema desde otra perspectiva.

-   Exploración del diseño.

    Si diseña software interactivo, la única manera de explorar cómo se usará algo es crear un objeto ficticio e interactuar con él. A veces, la simulación está vinculada a un estudio de facilidad de uso, donde las partes del prototipo se pueden evaluar de forma estructurada. A veces, es solo una manera de expresar claramente a un desarrollador cómo debe funcionar o parecer algo. En muchos casos, es posible que un diseñador simplemente esté experimentando, en un esfuerzo por obtener una idea de qué enfoque podría funcionar. Cualquier persona del equipo puede usar prototipos para explorar problemas de diseño, aunque los diseñadores suelen ser los más cualificados. Las exploraciones de diseño deben dirigirse a intentar resolver problemas específicos que se reconocen en el producto.

-   Exploración técnica.

    Los desarrolladores que investigan los enfoques de implementación de un problema suelen probar diferentes técnicas de codificación para ver si funcionan bien. El uso de COM+, HTML dinámico (DHTML), Microsoft Win32 o enfoques de codificación específicos dentro de cada tecnología tienen diferentes contras. A veces, un prototipo representa una exploración de qué tecnología funcionará bien para admitir una determinada característica de interfaz de usuario.

A veces se crean prototipos por una combinación de estos motivos. Si un equipo planea lo suficiente, puede dar tiempo a que un desarrollador y un diseñador o administrador de proyectos trabajen juntos en un prototipo. En tales casos, es muy importante definir claramente los objetivos y las contribuciones que se espera que realice cada miembro del equipo. Todo el mundo debe tener claro cuáles son los objetivos, qué está en peligro y cuál será el resultado potencial.

## <a name="who-is-involved"></a>Quién ¿Está implicado?

Cualquiera puede realizar la creación de prototipos de forma informal, independientemente de su experiencia o rol en el proyecto. Es fácil crear un prototipo sencillo pero eficaz tomando un mapa de bits de Adobe Photoshop, lo coloca en la herramienta de administración y creación de sitios web de Microsoft FrontPage y agrega botones o vínculos activos. Estos prototipos ligeros solo van tan lejos y pueden resultar difíciles de manejar para interacciones complejas.

Para prototipos más formales de equipos más grandes, un desarrollador o un administrador de proyectos a menudo colaborará con un diseñador y un ingeniero de facilidad de uso. Juntos generarán ideas, crearán un prototipo que represente las mejores ideas y, a continuación, irán al laboratorio para ver su eficacia en la resolución de problemas de los usuarios. Los desarrolladores pueden participar si pueden ahorrar tiempo o si se necesita su experiencia técnica. A menudo, el diseñador o el administrador de proyectos realizarán la mayor parte del scripting o la codificación para compilar el prototipo.

## <a name="when-should-a-prototype-be-built"></a>¿Cuándo se debe crear un prototipo?

Según el ámbito del prototipo y el nivel de detalle necesario, los prototipos se pueden crear en cualquier momento durante el proyecto. La mayoría de los casos se crean al principio del proyecto, durante la fase de planeamiento y especificación, antes de que los desarrolladores escriban cualquier código de producción. Es entonces cuando la necesidad de exploración es mayor y cuándo es más viable la inversión necesaria. Si los desarrolladores en lugar de los diseñadores o los administradores de programas son prototipos, el tiempo de programación es aún más importante debido a la necesidad de asegurarse de que el trabajo invertido en el prototipo se tenga en cuenta en la programación de desarrollo. La planeación de cualquier versión de la interfaz de usuario debe incluir algún nivel de creación de prototipos.

Al final de un proyecto, los prototipos más pequeños pueden ayudar a resolver problemas técnicos y de diseño difíciles. Una rápida simulación HTML de cómo debe comportarse un cuadro de diálogo o una página web puede ayudar a responder a la pregunta de un desarrollador o a dar una sensación a otros compañeros de equipo de cuál debe ser la experiencia deseada. En algunos casos, un diseñador o administrador de programas fuerte puede implementar el comportamiento en el software de desarrollo de Microsoft JScript y aproximarse a gran parte de la lógica de programación que los desarrolladores tendrán que pensar.

El tiempo necesario para crear un prototipo puede variar enormemente, en función del ámbito y la precisión de la apariencia del resultado final. Un prototipo informal podría significar unas horas de trabajo por parte de una persona. un esfuerzo más organizado puede implicar semanas de esfuerzo por parte de todo un equipo.

## <a name="where-should-the-focus-be"></a>¿Dónde debe estar el foco?

En un prototipo, cree solo la mayor parte del diseño que sea necesario. Es correcto tener botones que no funcionen o texto que nunca se actualice. Siempre que se puedan experimentar las interacciones necesarias, es mejor usar humo y reflejos para el resto. Estas son algunas de las razones por las que los esfuerzos deben centrarse detenidamente:

-   Costo de la creación del prototipo.

    Se debe minimizar el costo implicado en la creación del prototipo. El desafío con la creación de prototipos es reconocer la inversión mínima necesaria para responder eficazmente a preguntas sobre el diseño. Aquí es donde los estudios de facilidad de uso son críticos, ya que identifican claramente las partes de la interfaz de usuario que necesitan más trabajo. Incluso sin estudios de facilidad de uso, defina claramente qué problemas de usuario se resuelven o qué tareas se están mejorando, con el diseño en el prototipo.

-   Duración limitada.
-   Los prototipos deben tener duraciones claramente definidas. ¿El objetivo final es una presentación en una reunión de equipo? ¿Una reunión de revisión ejecutiva? ¿Una revisión de especificaciones? ¿Un estudio de facilidad de uso? ¿Identifica que el diseño resuelve un problema del usuario? Una vez que se cumplen las necesidades de estos objetivos específicos, se debe reservar el prototipo. La mentalidad básica es que el código o los mapas de bits generados en un prototipo se van a dejar atrás. Puede haber excepciones en las que el código o los objetos visuales se basen en el producto, pero la expectativa debe ser que esto no sea así.
-   Riesgo de desbordar al equipo.

    Mostrar prototipos a desarrolladores y compañeros de equipo puede ser complicado. Un prototipo demasiado complejo o elaborado, impresionantes objetos visuales y animaciones, puede sobrecargar a las personas. Tenga siempre una idea de hasta dónde llegar y cuánto del prototipo se debe tomar en serio.

## <a name="what-is-the-scope"></a>¿Cuál es el ámbito?

A medida que se determina el enfoque para el esfuerzo de creación de prototipos, tenga en cuenta lo siguiente:

-   Necesidades del cliente.

    A partir de una comprensión de los problemas o necesidades clave de los usuarios (quizás algo que haya proporcionado un ingeniero de facilidad de uso), se proporciona una idea sobre qué partes del diseño de la interfaz de usuario garantizan la mayor exploración.

-   Tareas de estudio de facilidad de uso.

    Si crea el prototipo para un estudio de facilidad de uso, analice con el ingeniero de facilidad de uso qué tareas específicas formarán parte del estudio y diseñe en torno a esos elementos.

-   Entrada del equipo.

    Hable con los desarrolladores clave del equipo a medida que se reúnen las ideas del prototipo. Obtenga una idea básica de lo que es razonable, lo que es posible y lo que está fuera de consideración para la próxima versión. En algunos casos, considere la posibilidad de ir más allá de lo que se dice que es posible para un aspecto del diseño si es un punto clave y el equipo debe ser desafío. Sin embargo, no lo haga con todos los aspectos del prototipo, ya que hay una línea fina entre forzar los límites y sobrecoge el equipo. Si el deseo es inspirar al equipo mostrándoles una visión para varias versiones, vaya por ella. Sin embargo, si el requisito es definir cambios específicos para la próxima versión, centre los esfuerzos en esos cambios. Asegúrese de llamar a los cambios específicos de forma modular y mostrar a los desarrolladores una ruta de acceso para crear los diseños.

-   Amplitud frente a profundidad.

    En el caso de prototipos más grandes, existe la consideración adicional de amplitud frente a profundidad. ¿Debe funcionar un poco cada característica del diseño o se debe elegir una característica para crear prototipos con casi todas sus piezas y opciones? Intente no hacer ambas cosas, ya que el resultado podría ser un prototipo grande y difícil de modificar y difícil de deshacer.

## <a name="flexible-prototypes"></a>Prototipos flexibles

Una manera de centrar los recursos de creación de prototipos es concentrarse en el diseño inteligente. Se pueden crear prototipos más eficaces permitiendo que un fragmento de código de prototipo pueda ejercer muchas ideas diferentes. En lugar de tener cinco prototipos diferentes, considere la posibilidad de crear un prototipo que tenga las opciones para cambiar los distintos atributos del prototipo.

¿La barra de herramientas debe estar ubicada a la izquierda o en la parte superior? ¿Debemos mostrar 10 elementos en la página principal o 20? Un buen prototipo tiene algún tipo de panel de opciones integrado que le permite cambiar los parámetros de cómo se ve o funciona el prototipo. Mantenga estos paneles de opciones ocultos en el prototipo: intente evitar que un participante de facilidad de uso los encuentre accidentalmente durante una prueba.

El desafío consiste en mantener el prototipo sencillo, pero lo suficientemente útil como para que se pueda mostrar a un compañero de equipo, se pueden demostrar distintas opciones y se pueden obtener comentarios.

## <a name="beta-vs-prototype"></a>Beta frente a prototipo

Las versiones beta no se califican como prototipos, porque son trabajos de ingeniería completos. Si se encuentra un error crítico en una característica de una versión beta, es poco probable que se descarte, aunque sea lo mejor para el producto. Los desarrolladores, evaluadores y diseñadores ya han invertido una gran cantidad de tiempo y la presión de la vida con decisiones mal tomadas es muy alta. Las versiones beta ciertamente ayudan a encontrar errores y defectos, pero rara vez son útiles para realizar estudios controlados del valor de instrucciones de diseño específicas.

## <a name="tools-and-technologies"></a>Herramientas y tecnologías

Hay varias herramientas y tecnologías diferentes que se pueden usar para crear prototipos, cada una de las cuales tiene sus ventajas y desventajas. Tenga en cuenta el tipo de trabajo de diseño que se está diseñando y los objetivos del trabajo de creación de prototipos antes de decidir qué herramienta o tecnología es la adecuada.

-   Microsoft Visual Basic o C#.

    Esta es la tecnología más rápida para crear prototipos Windows de interfaz de usuario de estilo clásico. El objeto de explorador web facilita la integración de HTMLUI con componentes Windows estilo estándar. Aunque es cierto que un desarrollador experimentado con Microsoft Visual Studio podría generar la interfaz de usuario más rápido en C/C++, esto crea la tentación de reutilizar el código del prototipo de interfaz de usuario en el código de producción. Se requiere disciplina para reconocer que los objetivos de un prototipo de interfaz de usuario rápido y desduciado son muy divergentes de la ingeniería de alta calidad. Asegúrese de que está claro qué tipo de código se escribe y que el equipo o el administrador entiende lo que se descartará.

-   Microsoft Expression Blend + SketchFlow.

    SketchFlow es una herramienta visual para diseñar, crear prototipos y crear interfaces de usuario sofisticadas para aplicaciones web y de escritorio de Windows Presentation Foundation (WPF) y Microsoft Silverlight. Las aplicaciones se construyen dibujando formas, dibujando controles como botones y cuadros de lista, haciendo que los elementos de una aplicación respondan a clics del mouse y a otras entradas del usuario, y aplicar estilos a todo para que parezcan únicos.

-   Adobe Director o Adobe Flash.

    Director es una conocida herramienta de creación de prototipos de IU entre diseñadores. Es más útil para diseños de GUI multimedia o no estándar, o para prototipos que requieren animación significativa. Su alta flexibilidad lo hace complicado para la interfaz de usuario de estilo de interfaz de usuario en comparación con Visual Basic. Sin embargo, un usuario de Director eficaz puede generar Windows o interfaz de usuario web sin dificultades.

-   HTML.

    FrontPage y otros editores HTML permiten crear rápidamente prototipos sencillos. Para expresar una idea, a menudo es posible crear mapas de bits que ilustran una secuencia de interacción del usuario y colocarlos en FrontPage. Estas imágenes se pueden usar para simular cómo interactuar con el diseño. JScript y DHTML llevan las cosas a otro nivel, lo que permite una lógica y una interacción muy sofisticadas. Si usa HTML para crear prototipos de un sitio web, la advertencia que se acaba de describir para C/C++ también se aplica aquí: no se encuentra en la trampa de confundir el código de prototipo rápido con ingeniería de calidad de producción.

 

 




