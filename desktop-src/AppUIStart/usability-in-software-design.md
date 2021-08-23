---
title: Facilidad de uso en el diseño de software
description: En este tema se presenta el concepto de facilidad de uso y por qué debe ser una parte importante de cualquier proyecto de diseño de software.
ms.assetid: 912b3224-e36d-44d6-98fa-a7f28e68a2d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482fd749a797c58656d987e1bde9e995ac58b8fdf98a6c056cd327e846665749
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589135"
---
# <a name="usability-in-software-design"></a>Facilidad de uso en el diseño de software

En este tema se presenta el concepto de facilidad de uso y por qué debe ser una parte importante de cualquier proyecto de diseño de software.

-   [Introducción](#introduction)
-   [Definición de facilidad de uso](#defining-usability)
    -   [Facilidad de uso](#ease-of-use)
    -   [Facilidad de uso frente a utilidad](#usability-vs-utility)
    -   [Me gusta frente a su uso](#liking-it-vs-using-it)
    -   [Detección frente a Learning frente a eficiencia](#discovery-vs-learning-vs-efficiency)
    -   [Las indesaciones no funcionan](#slogans-do-not-work)
-   [¿Por qué es importante la facilidad de uso?](#why-is-usability-important)
    -   [¿Por qué debería interesar?](#why-should-you-care)
    -   [¿Qué cuesta?](#what-does-it-cost)
    -   [¿Cómo puedo aumentar la facilidad de uso?](#how-do-i-increase-usability)
    -   [¿Por qué debo implicar a los usuarios?](#why-should-i-involve-users)
    -   [¿No puedo seguir las instrucciones?](#cant-i-just-follow-guidelines)
    -   [¿Es necesario crear un laboratorio de facilidad de uso?](#do-i-need-to-build-a-usability-lab)
    -   [¿Cómo puedo Introducción?](#how-do-i-get-started)

## <a name="introduction"></a>Introducción

El término "facilidad de uso" en el contexto de creación de software representa un enfoque que coloca al usuario, en lugar del sistema, en el centro del proceso. Esta filosofía, conocida como diseño centrado en el usuario, incorpora preocupaciones y promoción de los usuarios desde el principio del proceso de diseño y dicta que las necesidades del usuario deben ser las más importantes de las decisiones de diseño.

El aspecto más visible de este enfoque son las pruebas de facilidad de uso, en las que los usuarios trabajan e interactúan con la interfaz de producto y comparten sus opiniones y preocupaciones con los diseñadores y desarrolladores.

## <a name="defining-usability"></a>Definición de facilidad de uso

En la sección se define lo que significa la facilidad de uso en el contexto del desarrollo de software y cómo se relaciona con otros aspectos del proceso de desarrollo.

### <a name="ease-of-use"></a>Facilidad de uso

La facilidad de uso es una medida de lo fácil que es usar un producto para realizar tareas prescritas. Esto es distinto de los conceptos relacionados de utilidad y facilidad de uso.

### <a name="usability-vs-utility"></a>Facilidad de uso frente a utilidad

Un atributo central que determina la calidad de un producto es útil. Esto mide si los usos reales de un producto pueden lograr los objetivos que los diseñadores pretenden lograr. El concepto de utilidad se bifurca aún más en utilidad y facilidad de uso. Aunque estos términos están relacionados, no son intercambiables.

La utilidad hace referencia a la capacidad del producto para realizar una tarea o tareas. Entre más tareas se diseñe el producto, más utilidad tiene.

Considere los procesadores de palabras MS-DOS de Microsoft típicos de finales de la década de 1980. Estos programas proporcionaban muchas características eficaces de edición y manipulación de texto, pero requerían que los usuarios aprendiesen y recordaran docenas de pulsaciones de teclas arcanas para realizarlas. Se puede decir que aplicaciones como estas tienen una utilidad alta (dan a los usuarios la funcionalidad necesaria) pero baja facilidad de uso (los usuarios deben dedicar mucho tiempo y esfuerzo a aprenderlos y usarlos). Por el contrario, una aplicación sencilla bien diseñada, como una calculadora, puede ser muy fácil de usar, pero no ofrecer mucha utilidad.

Ambas calidades son necesarias para la aceptación del mercado y ambas forman parte del concepto general de utilidad. Obviamente, si un programa es muy utilizable, pero no hace nada de valor, nadie lo usará. Y los usuarios a los que se les presenta un programa eficaz que es difícil de usar probablemente lo resistirán o buscarán alternativas.

Las pruebas de facilidad de uso le ayudan a determinar lo fácil que es para los usuarios realizar tareas concretas. Sin embargo, no ayuda directamente a determinar si el propio producto tiene valor o utilidad. (Los usuarios pueden participar en comentarios relacionados con la utilidad durante las pruebas de facilidad de uso, pero cualquier comentario debe comprobarse con otros métodos de investigación más sólidos).

### <a name="liking-it-vs-using-it"></a>Me gusta frente a su uso

La silabilidad siempre es un rasgo deseable en un producto. Si a las personas les gusta el producto, es más probable que lo usen y se lo recomiende a otras personas. Pero al igual que con la utilidad, debe tener cuidado de no confundir la sitabilidad con la facilidad de uso.

A las personas les suele gustar un producto por motivos no relacionados con la utilidad y la facilidad de uso. Pueden ser atractivos para su estilo o para el estado que creen que el producto les confiere. A las personas les suelen gustar productos muy utilizables, pero no debe suponer que se puede usar un producto que le gusta mucho.

La facilidad de uso es sobre si una persona puede usar el producto para realizar las tareas que necesita realizar. Las pruebas de facilidad de uso mide principalmente el rendimiento, no la preferencia. Sin embargo, se pueden usar cuestionarios estandarizados para medir las preferencias entre productos.

### <a name="discovery-vs-learning-vs-efficiency"></a>Detección frente a Learning frente a eficiencia

Hay muchos aspectos en la facilidad de uso, pero tradicionalmente el término hace referencia específicamente a los atributos de detección, aprendizaje y eficacia.

-   La detección implica buscar y buscar la característica de un producto en respuesta a una necesidad determinada. Las pruebas de facilidad de uso pueden determinar cuánto tiempo tarda un usuario en encontrar una característica y cuántos errores (opciones incorrectas sobre la ubicación) produce el usuario a lo largo del proceso.
-   Learning hace referencia al proceso por el que el usuario entiende cómo usar una característica detectada para completar una tarea. Las pruebas de facilidad de uso pueden determinar cuánto tiempo tarda este proceso y también cuántos errores produce el usuario al aprender la característica.
-   Eficiencia hace referencia al punto en el que el usuario ha "maestro" la característica y la usa sin necesidad de más aprendizaje. Las pruebas de facilidad de uso pueden determinar cuánto tiempo tarda el usuario experimentado en ejecutar los pasos necesarios para usar la característica.

Estos tres aspectos básicos de la facilidad de uso están muy influenciados por la naturaleza de la tarea en mano y la frecuencia con la que el usuario la realiza. Algunas características se usan tan rara vez o son tan complejas que el usuario las vuelve a aprender cada vez; Para estas características, Microsoft a menudo desarrolla asistentes para guiar al usuario a través del proceso.

### <a name="slogans-do-not-work"></a>Las indesaciones no funcionan

A veces, los desarrolladores de software creen que los simples desafíos como "hacer que el producto sea más utilizable" ayudarán a resolver problemas de facilidad de uso. Aunque es importante una postura positiva hacia la facilidad de uso, solo las pruebas de facilidad de uso adecuadas con usuarios normales, en el contexto del producto específico que se va a crear, pueden proporcionar a los desarrolladores la información que necesitan para crear un producto que se ajuste a las necesidades de los usuarios. "Hacer que el producto sea más utilizable" debe ser la idea de todos los desarrolladores de software, pero solo tiene sentido si el desarrollador sabe lo que significa la facilidad de uso. Las pruebas con usuarios normales son la manera más confiable de averiguarlo.

## <a name="why-is-usability-important"></a>¿Por qué es importante la facilidad de uso?

En la sección se responden algunas preguntas comunes sobre por qué es importante la facilidad de uso y cómo incorporar principios de diseño centrados en el usuario en el proceso de desarrollo.

### <a name="why-should-you-care"></a>¿Por qué debería interesar?

Si aún no se han incorporado consideraciones de facilidad de uso en el proceso de diseño del producto, es posible que se pregunte por qué es necesario o deseable. Después de todo, es posible lanzar un producto sin errores en funcionamiento sin realizar ningún trabajo de facilidad de uso. Pero la incorporación de principios de diseño centrados en el usuario puede dar lugar a un producto muy mejorado en varias áreas.

La mejor razón para realizar pruebas de facilidad de uso es reducir el número de llamadas de soporte técnico de los usuarios. La facilidad de uso deficiente es una de las principales razones por las que los usuarios llaman a las líneas de soporte técnico de software, y todos los ejecutivos de la empresa de software y el administrador de Information Services saben lo costoso que puede ser el soporte técnico del producto. Además, cobrar a los usuarios por soporte técnico aumenta la posible insatisfaz con el producto. Si a los usuarios les resulta fácil usar el producto, no tendrán que llamar al soporte técnico con tanta frecuencia.

Para el software generado para uso interno, la siguiente mejor razón para hacer que la facilidad de uso sea una parte importante del proceso de desarrollo es reducir los costos de entrenamiento. Un producto muy utilizable es mucho más fácil de aprender para los usuarios que uno para el que la facilidad de uso no era una prioridad alta. Los usuarios aprenden las características más rápidamente y conservan sus conocimientos más tiempo, lo que se correlaciona directamente con la reducción de los costos de entrenamiento y el tiempo.

Las pruebas de facilidad de uso ayudan a mejorar la aceptación del usuario. La aceptación se produce a partir de una serie de factores, como la facilidad de uso, la utilidad y la facilidad de uso. En el caso de los productos minoristas, la aceptación del usuario a menudo se correlaciona directamente con la repetición de la compra o con la fidelidad, lo que significa que es probable que el usuario recomiende el producto a otros usuarios. En el caso de las aplicaciones internas, la aceptación del usuario se correlaciona con la disposición de usar el software para realizar las tareas para las que se diseñó, lo que ayuda a aumentar la productividad. Aumentar la facilidad de uso es uno de los factores que pueden contribuir a una mayor aceptación del usuario.

La facilidad de uso puede ayudar a diferenciar los productos de los de sus competidores. Si dos productos son sustancialmente iguales en la utilidad, el producto con mejor facilidad de uso probablemente se considerará superior. Además, las directrices de programación Windows look-and-feel y las instrucciones de programación que lo acompañan han nivelado el campo de juego de la interfaz de usuario básica, de modo que muchos programas que sirven funciones similares se parezcan y actúen de forma similar. Estas similitudes significan que pequeñas diferencias en la facilidad de uso pueden tener un gran efecto en las preferencias del usuario.

Por último, todos los productos se prueban con el tiempo para comprobar su facilidad de uso. Los usuarios realizan pruebas de facilidad de uso en el producto cada vez que lo usan y representan su veredicto a través de su uso continuo o su falta. Probar el producto antes de lanzarlo al mercado puede ayudar a garantizar que las experiencias de los usuarios con el producto sean positivas.

### <a name="what-does-it-cost"></a>¿Qué cuesta?

Los desarrolladores de software y los administradores de proyectos suelen preocuparse de que iniciar un proceso de diseño centrado en el usuario y realizar pruebas de facilidad de uso adecuadas requieran cantidades inaceptables de tiempo y dinero. La realidad es que el costo en tiempo y dinero invertido en centrarse en el usuario suele ser relativamente pequeño y, ciertamente, en comparación con el costo de no hacerlo.

Tenga en cuenta, por ejemplo, el costo en tiempo y dinero de hacer revisiones de diseño tardías en el ciclo de desarrollo, en lugar de antes, cuando el producto todavía está en el tablero de dibujo. Esperar hasta el período beta para exponer a los usuarios al producto con fines de pruebas de facilidad de uso puede dar lugar a la deserción de partes del programa que tardaron mucho tiempo en desarrollarse. Y esperar hasta que el producto se lanza realmente y, a continuación, realizar cambios basados en comentarios negativos o admitir un diseño deficiente podría hacer que el costo sea inmeasurablemente mayor debido a los altos costos de soporte técnico del producto o a una mala recepción por parte de los usuarios.

Normalmente, se puede realizar un estudio de facilidad de uso razonable en unas dos semanas o menos, y puede reducir considerablemente el tiempo y el costo de realizar cambios al final del ciclo de desarrollo. El costo de realizar pruebas variará en función de la naturaleza del producto y de las partes de la interfaz que se prueban.

Piense que las pruebas de facilidad de uso son parecidas a las pruebas de código. Los administradores de proyectos correctos tienen en cuenta las pruebas de código al planear un proyecto de desarrollo. No lo ven como algo adicional que se debe incluir en la programación y el presupuesto del proyecto. En su lugar, los administradores de proyectos aceptan las pruebas de código como un costo de hacer negocios porque la alternativa es mucho más costosa. Lo mismo se aplica a las pruebas de facilidad de uso.

### <a name="how-do-i-increase-usability"></a>¿Cómo puedo aumentar la facilidad de uso?

Al leer y comprender la importancia de la facilidad de uso, los desarrolladores de software a veces se animan a agregar facilidad de uso, como si fuera un ingrediente que simplemente se puede agregar a un producto para que sea más fácil de usar. En su lugar, la facilidad de uso debe formar parte del propio proceso de diseño, en lugar de una "cosa" que se agrega al proceso aquí o allí. La razón por la que los expertos en facilidad de uso hacen referencia al "enfoque del usuario" y al "diseño centrado en el usuario" es que la facilidad de uso depende de mantener las necesidades de los usuarios centrales en el proceso de diseño. El diseño centrado en el usuario por necesidad implica algo más que seguir un conjunto de reglas que rigen la colocación de botones y menús en una interfaz. Las pruebas de facilidad de uso son una oportunidad para comprobar el trabajo de diseño. No es una manera de "agregar" facilidad de uso a un producto.

Gould, Boies y Lee (1991) identifican cuatro principios importantes del diseño centrado en el usuario:

-   Enfoque temprano en los usuarios.

    Los desarrolladores deben concentrarse en comprender las necesidades de los usuarios al principio del proceso de diseño.

-   Diseño integrado.

    Todos los aspectos del diseño deben evolucionar en paralelo, en lugar de en secuencia. Mantenga el diseño interno del producto coherente con las necesidades de la interfaz de usuario.

-   Pruebas tempranas y continuas.

    El único enfoque factible actualmente para el diseño de software es empírico: el diseño funciona si los usuarios reales deciden que funciona. La incorporación de pruebas de facilidad de uso a lo largo del proceso de desarrollo ofrece a los usuarios la oportunidad de enviar comentarios sobre el diseño antes de que se lanza el producto.

-   Diseño iterativo.

    Los problemas grandes suelen enmascarar problemas pequeños. Los diseñadores y desarrolladores deben revisar el diseño de forma iterativa a través de rondas de pruebas.

### <a name="why-should-i-involve-users"></a>¿Por qué debo implicar a los usuarios?

Los desarrolladores deben reconocer que no son usuarios típicos. Tienen un conocimiento y una comprensión más profundos del sistema que están desarrollando que el usuario medio que nunca lo hará. Por lo tanto, los aspectos de la interfaz poco claros o confusos para la mayoría de los usuarios pueden ser perfectamente claros para alguien que ha trabajado en el proyecto. Algunos desarrolladores de software pueden empatíarse con el usuario medio hasta cierto punto, pero no hay ningún sustituto para las interacciones reales de los usuarios reales con el producto.

En consecuencia, al centrarse en las necesidades típicas de los usuarios pronto y revisar el diseño en función de las pruebas de usuario a menudo, los desarrolladores de software centrados en el usuario producen mejores diseños y, como resultado, mejores productos.

Con un mejor diseño, los usuarios tienen una mejor aceptación. La ventaja con el software comercial es obvia: aumento de las ventas. La aceptación también es importante con el software desarrollado para uso interno: un mayor enfoque en el diseño centrado en el usuario conduce a una mayor productividad y una menor necesidad de soporte técnico. La implicación visible de los usuarios desde el principio del desarrollo también muestra interés en sus preocupaciones y necesidades, lo que aumenta su disposición a ayudar en el esfuerzo de desarrollo.

### <a name="cant-i-just-follow-guidelines"></a>¿No puedo seguir las instrucciones?

Microsoft ha desarrollado un conjunto de directrices de interfaz para la plataforma Windows informática para garantizar que los programas Windows tengan una apariencia coherente. Otras compañías han desarrollado directrices similares para otras plataformas informáticas, y expertos en facilidad de uso, como Unix Unix, han escrito ampliamente sobre el diseño de páginas web utilizables. Con la gran cantidad de información disponible sobre estos temas, los diseñadores a veces creen que el estricto cumplimiento de las directrices y estándares es todo lo necesario para producir productos utilizables.

El problema con este enfoque es que las directrices son intrínsecamente generales. Las directrices deben aplicarse a una amplia variedad de casos y, por tanto, no siempre se prescriba el mejor curso de acción para la aplicación en particular que se está desarrollando. La adhesión a un conjunto de directrices bien escrito puede ayudar en el diseño de una interfaz coherente, pero no pueden garantizar su usablility a menos que se haya probado con usuarios reales. Al usar directrices, no las use como una guía en la que las directrices apunten hacia el mejor de todos los resultados. Dos desarrolladores pueden implementar la misma guía de dos maneras diferentes, y es posible que ambas implementaciones no sean igualmente adecuadas para la situación. En ocasiones, el cumplimiento riguroso de las directrices puede provocar resultados deficientes o conflictos entre las directrices. Solo el diseño centrado en el usuario puede ayudar a vaciar estos problemas antes de que se conviertan en problemas.

Otra manera de pensar en esto es: permitir que el diseño centrado en el usuario sea el mediar de las decisiones de diseño, no las directrices de la interfaz de usuario.

### <a name="do-i-need-to-build-a-usability-lab"></a>¿Es necesario crear un laboratorio de facilidad de uso?

No suponga que las pruebas de facilidad de uso implican la confirmación de un laboratorio costoso, con cámaras montadas en el límite, reflejos uned paso a paso y otras capturas de grupos de enfoque. Sin duda, a las empresas que hacen muchas pruebas a menudo les resulta conveniente crear laboratorios dedicados y los consultores de facilidad de uso a menudo tienen una amplia gama de instalaciones y equipos para ofrecer a sus clientes. Pero las pruebas de facilidad de uso útiles y válidas se pueden realizar en una variedad de configuraciones y circunstancias.

Un enfoque es simplemente hacer que un evaluador tenga experiencia en la realización de estudios de participantes humanos y la recopilación de datos? ¿se encuentra detrás de un usuario mientras trabaja y observa al usuario realizando tareas. Esto se puede realizar fácilmente en una sala de conferencias o en una oficina. Para obtener más información sobre las pruebas por observación, vea la entrada Dumas y Redish en [Otros recursos.](other-resources.md)

A medida que las pruebas de facilidad de uso se desarrollan y se vuelven más implicadas, se pueden agregar equipos como una cámara de vídeo, un reflejo unitario o herramientas que permiten ver y grabar el monitor de un usuario en tiempo real.

Como alternativa, las pruebas se pueden externalizar a consultores de facilidad de uso. La sección siguiente contiene sugerencias sobre la búsqueda de los consultores adecuados.

### <a name="how-do-i-get-started"></a>¿Cómo puedo Introducción?

Una vez que se haya decidido incorporar principios de diseño centrados en el usuario en el proceso de desarrollo, tendrá que decidir si contratar profesionales de facilidad de uso o externalizar las pruebas de facilidad de uso a un proveedor.

La Asociación de profesionales de facilidad de uso (UPA) tiene una guía de proveedor que puede ayudar a encontrar consultores de facilidad de uso.

Algunos grupos de consultoría también pueden ayudar a configurar laboratorios de facilidad de uso o desarrollar un programa de facilidad de uso internos para incorporar principios de facilidad de uso en el proceso de diseño.

Si contrata a profesionales de facilidad de uso, Human Factors and La sociedad de las personas tiene un servicio de selección de ubicación que puede ayudar a encontrar posibles empleados. Muchos profesionales de facilidad de uso también pertenecen al grupo de interés especial de ACM en Computer-Human Interaction (SIGCHI) y UPA. Coloque anuncios de empleo en sus publicaciones o en sus conferencias.

Independientemente de la ruta que se haga, recuerde que se trata de servicios de prueba. El principio de que los diseñadores no son usuarios típicos también es cierto para los profesionales de facilidad de uso.

Para obtener más información sobre estas empresas y organizaciones, y para obtener más información sobre las pruebas de facilidad de uso y el diseño centrado en el usuario, vea [Otros recursos.](other-resources.md)

 

 




