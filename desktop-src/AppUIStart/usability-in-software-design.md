---
title: Facilidad de uso en el diseño de software
description: En este tema se presenta el concepto de facilidad de uso y por qué debe ser una parte importante de cualquier proyecto de diseño de software.
ms.assetid: 912b3224-e36d-44d6-98fa-a7f28e68a2d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b302e63a475d060748e896440b28915816d910e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075268"
---
# <a name="usability-in-software-design"></a>Facilidad de uso en el diseño de software

En este tema se presenta el concepto de facilidad de uso y por qué debe ser una parte importante de cualquier proyecto de diseño de software.

-   [Introducción](#introduction)
-   [Definir la facilidad de uso](#defining-usability)
    -   [Facilidad de uso](#ease-of-use)
    -   [Facilidad de uso frente a utilidad](#usability-vs-utility)
    -   [Gustos y uso](#liking-it-vs-using-it)
    -   [Detección frente a aprendizaje frente a eficacia](#discovery-vs-learning-vs-efficiency)
    -   [Los lemas no funcionan](#slogans-do-not-work)
-   [¿Por qué es importante la facilidad de uso?](#why-is-usability-important)
    -   [¿Por qué debería interesarle?](#why-should-you-care)
    -   [¿Qué cuesta?](#what-does-it-cost)
    -   [¿Cómo aumento la facilidad de uso?](#how-do-i-increase-usability)
    -   [¿Por qué debo incluir a los usuarios?](#why-should-i-involve-users)
    -   [¿No se pueden seguir las instrucciones?](#cant-i-just-follow-guidelines)
    -   [¿Es necesario crear un laboratorio de uso?](#do-i-need-to-build-a-usability-lab)
    -   [¿Cómo puedo empezar?](#how-do-i-get-started)

## <a name="introduction"></a>Introducción

El término "facilidad de uso" en el contexto de la creación de software representa un enfoque que coloca al usuario, en lugar del sistema, en el centro del proceso. Esta filosofía, conocida como diseño centrado en el usuario, incorpora las preocupaciones del usuario y el apoyo desde el principio del proceso de diseño y determina que las necesidades del usuario deben ser las más importantes de las decisiones de diseño.

El aspecto más visible de este enfoque son las pruebas de facilidad de uso, en las que los usuarios trabajan e interactúan con la interfaz del producto y comparten sus vistas y preocupaciones con los diseñadores y los desarrolladores.

## <a name="defining-usability"></a>Definir la facilidad de uso

En la sección se define qué significa la facilidad de uso en el contexto del desarrollo de software y cómo se relaciona con otros aspectos del proceso de desarrollo.

### <a name="ease-of-use"></a>Facilidad de uso

La facilidad de uso es una medida de lo fácil que es usar un producto para realizar las tareas prescritas. Esto es distinto de los conceptos relacionados de utilidad y de la misma manera.

### <a name="usability-vs-utility"></a>Facilidad de uso frente a utilidad

Un atributo central que determina la calidad de un producto es útil. Esto mide si los usos reales de un producto pueden conseguir los objetivos que los diseñadores desean lograr. El concepto de la utilidad se ramifica en la utilidad y la facilidad de uso. Aunque estos términos están relacionados, no son intercambiables.

La utilidad hace referencia a la capacidad del producto de realizar una tarea o tareas. Cuanto más tareas haya diseñado el producto, más utilidad tendrá.

Tenga en cuenta los procesadores de textos típicos de Microsoft MS-DOS del último de los ochenta. Estos programas proporcionaban muchas características de edición y manipulación de texto eficaces, pero requerían que los usuarios aprendan y recuerden docenas de pulsaciones de teclas más separativas para realizarlas. Se puede decir que las aplicaciones, como estas, tienen una utilidad alta (proporcionan a los usuarios la funcionalidad necesaria), pero tienen una facilidad de uso bajo (los usuarios deben gastar mucho tiempo y esfuerzo en aprender y usarlos). Por el contrario, una aplicación sencilla y bien diseñada, como una calculadora, puede ser muy fácil de usar, pero no ofrece mucha utilidad.

Ambas cualidades son necesarias para la aceptación del mercado y ambas forman parte del concepto general de utilidad. Obviamente, si un programa es muy utilizable pero no hace nada de valor, nadie lo usará. Además, los usuarios que se presenten con un programa eficaz y que sean difíciles de usar probablemente la resistan o busquen alternativas.

Las pruebas de facilidad de uso le ayudan a determinar lo fácil que es que los usuarios realicen tareas específicas. Sin embargo, no ayuda directamente a determinar si el propio producto tiene el valor o la utilidad. (Los usuarios pueden enviar comentarios relacionados con la utilidad durante las pruebas de uso, pero los comentarios deben comprobarse con otros métodos de investigación más sólidos).

### <a name="liking-it-vs-using-it"></a>Gustos y uso

La like es siempre un rasgo deseable en un producto. Si hay personas como el producto, es más probable que la utilicen y lo recomienden a otras personas. Sin embargo, al igual que con la utilidad, debe tener cuidado de no confundir el modo de facilidad de uso.

Personas con frecuencia como un producto por motivos no relacionados con la utilidad y la facilidad de uso. Pueden estar atraídos por su estilo o por el estado que creen que el producto confiere a ellos. Personas normalmente como productos muy utilizados, pero no debe suponer que esto significa que se puede usar un producto bien conocido.

La facilidad de uso es la posibilidad de que una persona pueda usar el producto para realizar las tareas que necesita realizar. Las pruebas de facilidad de uso miden principalmente el rendimiento, no las preferencias. Sin embargo, los cuestionarios estandarizados se pueden usar para medir las preferencias de los productos.

### <a name="discovery-vs-learning-vs-efficiency"></a>Detección frente a aprendizaje frente a eficacia

Hay muchos aspectos para la facilidad de uso, pero tradicionalmente el término hace referencia específicamente a los atributos de detección, aprendizaje y eficiencia.

-   La detección implica buscar y encontrar la característica de un producto en respuesta a una necesidad concreta. Las pruebas de facilidad de uso pueden determinar cuánto tiempo tarda un usuario en encontrar una característica y cuántos errores (elecciones equivocadas sobre la ubicación) realiza el usuario a lo largo del proceso.
-   El aprendizaje se refiere al proceso por el que el usuario entiende cómo usar una característica detectada para completar una tarea. Las pruebas de facilidad de uso pueden determinar el tiempo que tarda este proceso y también el número de errores que realiza el usuario mientras se aprende la característica.
-   La eficacia hace referencia al punto en el que el usuario ha "dominado" la característica y la usa sin requerir más aprendizaje. Las pruebas de facilidad de uso pueden determinar cuánto tiempo tarda el usuario experimentado en ejecutar los pasos necesarios para usar la característica.

Estos tres aspectos básicos de la facilidad de uso se ven afectados por la naturaleza de la tarea a mano y por la frecuencia con la que el usuario la realiza. Algunas características se usan tan pocas veces o tan complejas que el usuario las reaprende esencialmente cada vez. para estas características, Microsoft suele desarrollar asistentes para guiar al usuario a través del proceso.

### <a name="slogans-do-not-work"></a>Los lemas no funcionan

A veces, los desarrolladores de software piensan que los lemas simples, como "hacer que el producto sea más utilizable", le ayudarán a resolver los problemas de uso. Aunque una actitud positiva hacia la facilidad de uso es importante, solo las pruebas de facilidad de uso adecuadas con usuarios normales, en el contexto del producto específico que se está creando, pueden proporcionar a los desarrolladores la información que necesitan para crear un producto que satisfaga las necesidades de los usuarios. "Hacer que el producto sea más utilizable" debe ser el eslogan de cada desarrollador de software, pero solo tiene sentido si el desarrollador sabe lo que significa la facilidad de uso. Las pruebas con usuarios normales son la manera más confiable de averiguar.

## <a name="why-is-usability-important"></a>¿Por qué es importante la facilidad de uso?

En la sección se responden algunas preguntas comunes sobre por qué es importante la facilidad de uso y cómo incorporar los principios de diseño centrados en el usuario al proceso de desarrollo.

### <a name="why-should-you-care"></a>¿Por qué debería interesarle?

Si las consideraciones de facilidad de uso todavía no se han incorporado en el proceso de diseño del producto, puede que se pregunte por qué es necesario o deseable. Después de todo, es ciertamente posible publicar un producto en funcionamiento y sin errores sin realizar ningún trabajo de uso. Pero la incorporación de principios de diseño centrados en el usuario puede conducir a un producto muy mejorado en varias áreas.

La mejor razón para realizar pruebas de facilidad de uso es reducir el número de llamadas de soporte técnico de los usuarios. Un uso deficiente es una razón importante por la que los usuarios llaman a las líneas de soporte técnico de software, y todos los ejecutivos de la compañía de software y el administrador de servicios de información saben cuánto cuesta el soporte técnico del producto. Además, la carga de los usuarios para obtener soporte técnico aumenta la insatisfacción del producto. Si los usuarios le resultan fáciles de usar el producto, no tendrán que llamar a para obtener soporte técnico con tanta frecuencia.

En el caso del software producido para uso interno, la siguiente mejor razón para que la facilidad de uso sea una parte importante del proceso de desarrollo es reducir los costos de entrenamiento. Un producto muy utilizable es mucho más fácil para que los usuarios aprendan de lo que el uso no era una prioridad alta. Los usuarios aprenden las características con más rapidez y conservan sus conocimientos más tiempo, lo que se correlaciona directamente con los costos y el tiempo de entrenamiento reducidos.

Las pruebas de facilidad de uso ayudan a mejorar la aceptación del usuario. Resultados de la aceptación de una serie de factores, incluida la facilidad de uso, la utilidad y el modo de like. En el caso de los productos de venta directa, la aceptación del usuario suele correlacionarse directamente con la repetición de la compra o la fidelidad, lo que significa que es probable que el usuario recomiende el producto a otros usuarios. En el caso de las aplicaciones internas, la aceptación del usuario se correlaciona con la voluntad de usar el software para realizar las tareas para las que se diseñó, lo que ayuda a aumentar la productividad. Aumentar la facilidad de uso es uno de los factores que pueden contribuir a una mayor aceptación del usuario.

La facilidad de uso puede ayudar a diferenciar los productos de los de sus competidores. Si dos productos son prácticamente iguales en la utilidad, el producto con una mejor capacidad de uso se considerará como superior. Además, las directrices de programación y la apariencia de Windows y las instrucciones de programación que lo acompañan han nivelado el campo de reproducción para la interfaz de usuario básica, de modo que muchos programas que atienden funciones similares parezcan y actúen ligeramente. Estas similitudes significan que las pequeñas diferencias de facilidad de uso pueden tener un gran efecto en las preferencias del usuario.

Finalmente, todos los productos se comprueban para obtener facilidad de uso. Los usuarios llevan a cabo pruebas de facilidad de uso en el producto cada vez que lo usan y presentan su veredicto a través de su uso continuado o de su ausencia. Probar el producto antes de publicarlo en el mercado puede ayudar a garantizar que las experiencias de los usuarios con el producto sean positivas.

### <a name="what-does-it-cost"></a>¿Qué cuesta?

Los desarrolladores de software y los administradores de proyectos suelen preocuparse de que el inicio de un proceso de diseño centrado en el usuario y la realización de pruebas de facilidad de uso adecuadas requerirán una cantidad de tiempo y dinero inaceptables. La realidad es que el costo de tiempo y dinero empleado en centrarse en el usuario suele ser relativamente pequeño y, por lo tanto, en comparación con el costo de no hacerlo.

Considere, por ejemplo, el costo en el tiempo y el dinero de realizar revisiones de diseño en el ciclo de desarrollo en lugar de antes, cuando el producto todavía está en el tablero de dibujo. La espera hasta que el período de la versión beta de exponga a los usuarios en el producto para la realización de pruebas de facilidad de uso puede dar lugar a la desmontaje de partes del programa que tardaron mucho tiempo en desarrollarse. Y esperar hasta que el producto se lance realmente y, después, realizar cambios en función de los comentarios negativos o de admitir un diseño deficiente podría hacer que el costo sea más alto debido a costos de soporte técnico elevados del producto o a una mala recepción por parte de los usuarios.

Un estudio de facilidad de uso razonable se puede realizar normalmente en aproximadamente dos semanas o menos, y puede reducir considerablemente el tiempo y el costo de realizar cambios en el ciclo de desarrollo. El costo de realizar pruebas variará en función de la naturaleza del producto y de las partes de la interfaz que se prueben.

Piense en las pruebas de facilidad de uso como parecidas a las pruebas de código. Cuenta correcta de administradores de proyectos para las pruebas de código al planear un proyecto de desarrollo. No lo ven como algo adicional que se debe agregar a la programación y al presupuesto del proyecto. En su lugar, los jefes de proyecto aceptan pruebas de código como un costo de hacer negocios porque la alternativa es mucho más costosa. Lo mismo se aplica a las pruebas de facilidad de uso.

### <a name="how-do-i-increase-usability"></a>¿Cómo aumento la facilidad de uso?

En el momento de leer y comprender la importancia de la facilidad de uso, a veces los desarrolladores de software se ven tentados a agregar facilidad de uso, como si fuera un ingrediente que simplemente se puede Agregar a un producto para que sea más fácil de usar. En su lugar, la facilidad de uso debe ser parte del propio proceso de diseño, en lugar de una "Thing" que se agrega aquí o allí. La razón por la que los expertos en facilidad de uso hacen referencia a "enfoque del usuario" y "diseño centrado en el usuario" es que la facilidad de uso depende del mantenimiento de las necesidades de los usuarios en el proceso de diseño. El diseño centrado en el usuario por necesidad implica algo más que simplemente seguir un conjunto de reglas que rigen el botón y la posición del menú en una interfaz. Las pruebas de facilidad de uso son una oportunidad para comprobar el trabajo de diseño. No es una forma de "agregar" facilidad de uso a un producto.

Gould, Boies y Lewis (1991) identifican cuatro principios importantes del diseño centrado en el usuario:

-   Foco temprano en los usuarios.

    Los desarrolladores deben concentrarse en comprender las necesidades de los usuarios al principio del proceso de diseño.

-   Diseño integrado.

    Todos los aspectos del diseño deben evolucionar en paralelo, en lugar de en secuencia. Mantenga el diseño interno del producto coherente con las necesidades de la interfaz de usuario.

-   Pruebas tempranas y continuas.

    El único enfoque actualmente viable para el diseño de software es un modelo empírico: el diseño funciona si los usuarios reales deciden que funciona. La incorporación de pruebas de facilidad de uso a lo largo del proceso de desarrollo permite a los usuarios enviar comentarios sobre el diseño antes de lanzar el producto.

-   Diseño iterativo.

    Los grandes problemas suelen enmascarar pequeños problemas. Los diseñadores y desarrolladores deben revisar el diseño de forma iterativa a través de rondas de pruebas.

### <a name="why-should-i-involve-users"></a>¿Por qué debo incluir a los usuarios?

Los desarrolladores deben reconocer que no son usuarios típicos. Tienen conocimientos más profundos y conocimientos sobre el sistema que están desarrollando que el usuario medio en cualquier momento. Los aspectos de la interfaz que no son claros o confusos para la mayoría de los usuarios podrían estar perfectamente claros para alguien que haya trabajado en el proyecto. Algunos desarrolladores de software pueden empatía con el usuario promedio hasta cierto punto, pero no hay ninguna sustitución por las interacciones reales de los usuarios reales con el producto.

En consecuencia, al centrarse en las necesidades de los usuarios típicos y revisar el diseño en función de las pruebas de usuario a menudo, los desarrolladores de software centrados en el usuario producen mejores diseños y, como resultado, mejores productos.

El mejor diseño ofrece una mejor aceptación por parte de los usuarios. La ventaja del software de venta al por menor es obvia: mayor ventas. La aceptación también es importante con el software desarrollado para uso interno: el aumento del enfoque en el diseño centrado en el usuario conlleva una mayor productividad y una necesidad reducida de soporte técnico. En la medida de lo que respecta a los usuarios desde el principio del desarrollo, también se muestra un interés en sus preocupaciones y necesidades, lo que aumenta su voluntad para ayudar en el esfuerzo de desarrollo.

### <a name="cant-i-just-follow-guidelines"></a>¿No se pueden seguir las instrucciones?

Microsoft ha desarrollado un conjunto de directrices de interfaz para la plataforma informática de Windows con el fin de garantizar que los programas de Windows tienen una apariencia coherente. Otras compañías han desarrollado directrices similares para otras plataformas informáticas y los expertos en usabilidad como Jakob Nielsen se han escrito en el diseño de páginas web que se pueden usar. Con la gran cantidad de información disponible en estos temas, a veces los diseñadores consideran un cumplimiento riguroso de las directrices y estándares es todo lo necesario para generar productos que se puedan usar.

El problema de este enfoque es que las instrucciones son intrínsecamente generales. Las instrucciones se deben aplicar a una amplia variedad de casos y, por lo tanto, no siempre prescriben el mejor procedimiento de acción para la aplicación concreta que se está desarrollando. El cumplimiento de un conjunto de directrices bien escrito puede ayudar en el diseño de una interfaz coherente, pero no puede garantizar su usablility a menos que se pruebe con usuarios reales. Al usar las instrucciones, no las use como una cocina en la que las instrucciones señalan la manera en el mejor de todos los resultados. Dos desarrolladores pueden implementar la misma directriz de dos maneras diferentes, y es posible que ambas implementaciones no sean igualmente adecuadas para la situación. En ocasiones, un cumplimiento riguroso de las instrucciones puede conducir a resultados insuficientes o a conflictos entre las instrucciones. Solo el diseño centrado en el usuario puede ayudar a vaciar estos problemas antes de que se conviertan en problemas.

Otra manera de pensar en esto es: dejar que el diseño centrado en el usuario sea el árbitro de las decisiones de diseño, no las directrices de la interfaz de usuario.

### <a name="do-i-need-to-build-a-usability-lab"></a>¿Es necesario crear un laboratorio de uso?

No asuma que las pruebas de facilidad de uso implican la confirmación de un laboratorio caro, con cámaras montadas en el techo, reflejos unidireccionales y otras capturas de grupo de enfoque. Para estar seguro, las empresas que realizan muchas pruebas a menudo le resultan útiles para crear laboratorios dedicados, y los asesores de facilidad de uso suelen tener una amplia gama de instalaciones y equipos para ofrecer sus clientes. Pero útil, se pueden realizar pruebas de uso válidas en diversas opciones y circunstancias.

Un enfoque consiste en tener simplemente un evaluador? alguien que se ha verso a la realización de estudios de participantes humanos y recopilación de datos. Siéntese detrás de un usuario cuando trabaja y observa que el usuario realiza tareas. Esto puede realizarse fácilmente en una sala de conferencias o en una oficina. Para obtener más información sobre las pruebas por observación, vea la entrada de Dumas y de recápsula en [otros recursos](other-resources.md).

A medida que las pruebas de facilidad de uso se desarrollan y se vuelven más complicadas, se pueden agregar equipos como una cámara de vídeo, un reflejo unidireccional o herramientas que permiten ver y grabar el monitor de un usuario en tiempo real.

Como alternativa, las pruebas se pueden subfuente a consultores de facilidad de uso. La siguiente sección contiene sugerencias sobre cómo buscar los asesores adecuados.

### <a name="how-do-i-get-started"></a>¿Cómo puedo empezar?

Una vez que se ha decidido incorporar los principios de diseño centrados en el usuario al proceso de desarrollo, deberá decidir si desea contratar a los profesionales de facilidad de uso o subcontratar las pruebas de facilidad de uso para un proveedor.

La Asociación de profesionales de facilidad de uso (UPA) tiene una guía de proveedores que puede ayudar a encontrar consultores de facilidad de uso.

Algunos grupos de consultoría también pueden ayudar a configurar laboratorios de uso o desarrollar un programa de uso interno para incorporar los principios de facilidad de uso en el proceso de diseño.

Si contrata a los profesionales de facilidad de uso, la sociedad de factores humanos y ergonomía tiene un servicio de colocación que puede ayudar a encontrar los posibles empleados. Muchos profesionales de facilidad de uso también pertenecen al grupo de interés especial de ACM en Computer-Human interacción (SIGCHI) y UPA. Coloque los anuncios de empleo en sus publicaciones o en sus conferencias.

Sea cual sea la ruta que se realice, recuerde que se trata de servicios de prueba. El principio de que los diseñadores no son usuarios típicos también es cierto para los profesionales de facilidad de uso.

Para obtener más información sobre estas empresas y organizaciones, y para obtener más información sobre las pruebas de facilidad de uso y el diseño centrado en el usuario, consulte [otros recursos](other-resources.md).

 

 




