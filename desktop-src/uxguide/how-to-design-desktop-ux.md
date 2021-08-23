---
title: Diseño de la experiencia de usuario para aplicaciones de escritorio
description: Una excelente aplicación de escritorio es eficaz y, al mismo tiempo, sencilla. Gracias a la selección y presentación de características cuidadosamente equilibradas, puede lograr eficacia y simplicidad.
ms.assetid: 0039a3ee-95bc-457f-a1a8-6a036ce22fd2
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a9c191a92ccf6147d37deca191a861220c4a925035bf39c92e7e7d062fa14184
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119221744"
---
# <a name="how-to-design-a-great-user-experience-for-desktop-applications"></a>Cómo diseñar una experiencia de usuario excelente para aplicaciones de escritorio

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Una excelente aplicación de escritorio es eficaz y, al mismo tiempo, sencilla. Gracias a la selección y presentación de características cuidadosamente equilibradas, puede lograr eficacia y simplicidad.

**Poderoso:**

![captura de pantalla del cuadro de diálogo de ortografía y gramática ](images/powerful-simple-image1.png)

**Eficaz y simple:**

![captura de pantalla de la lista de posibles revisiones ortográficas ](images/powerful-simple-image2.png)

La aplicación Windows basada en aplicaciones es eficaz y sencilla. Por supuesto, quiere que la aplicación sea eficaz y, por supuesto, quiere que sea sencilla, pero ¿puede lograr ambas cosas? Hay una tensión natural entre estos objetivos, pero esa tensión está lejos de ser irreconciable. Puede lograr eficacia y simplicidad a través de la selección y presentación de características cuidadosamente equilibradas.

## <a name="what-makes-an-application-powerful"></a>¿Qué hace que una aplicación sea eficaz?

¿Qué significa realmente "power" en términos de software? Una aplicación podría considerarse eficaz si está llena de características, con una gran gama de funcionalidades en un intento de ser todo para todos los usuarios. Es probable que este diseño no sea correcto porque es poco probable que un conjunto de características no objetivo satisfaga las necesidades de cualquiera. Este no es el tipo de potencia que buscamos.

Una aplicación es eficaz cuando tiene la combinación correcta de estas características:

-   **Permitiendo.** La aplicación satisface las necesidades de sus usuarios de destino, lo que les permite realizar tareas que de otro modo no podrían realizar y lograr sus objetivos de forma eficaz.
-   **Eficaz.** La aplicación permite a los usuarios realizar tareas con un nivel de productividad y escala que no era posible antes.
-   **Versátil.** La aplicación permite a los usuarios realizar una amplia gama de tareas de forma eficaz en una variedad de circunstancias.
-   **Directa.** La aplicación parece que ayuda directamente a los usuarios a lograr sus objetivos, en lugar de inponerse en el camino o requerir pasos innecesarios. Características como los accesos directos, el acceso al teclado y las macros mejoran la sensación de directness.
-   **Flexible.** La aplicación permite a los usuarios un control completo y preciso sobre su trabajo.
-   **Integrado.** La aplicación está bien integrada con Microsoft Windows, lo que le permite compartir datos con otras aplicaciones.
-   **Avanzado.** La aplicación tiene características excepcionales, innovadoras y de última generación que no se encuentran en soluciones de la competencia.

Algunas de estas características dependen de la percepción del usuario y son relativas a las capacidades actuales de los usuarios. Lo que se considera eficaz puede cambiar con el tiempo, por lo que la característica de búsqueda avanzada de hoy podría ser habitual mañana.

Todas estas características se pueden combinar en nuestra definición de potencia:

**Una aplicación es eficaz cuando permite que sus usuarios de destino se den cuenta de todo su potencial de forma eficaz.**

Por lo tanto, la medida final de la potencia es la productividad, no el número de características.

Los distintos usuarios necesitan ayuda para lograr todo su potencial de maneras diferentes. Lo que permite a algunos usuarios dañar la versatilidad, la directez y el control de otros usuarios. El software bien diseñado debe equilibrar estas características correctamente. Por ejemplo, un sistema de publicación de escritorio diseñado para no profesionales podría usar asistentes para recorrer las tareas complejas de los usuarios. Estos asistentes permiten a los usuarios de destino realizar tareas que, de lo contrario, no podrían realizar. Por el contrario, un sistema de publicación de escritorio para profesionales podría centrarse en la directez, la eficacia y el control completo. Para los usuarios de este tipo de aplicación, los asistentes pueden ser limitadores y frustrantes.

**Si solo hace una cosa...**

Comprender los objetivos de los usuarios de destino y crear un conjunto de características que les permita lograr esos objetivos de forma productiva.

## <a name="what-makes-a-user-experience-simple"></a>¿Qué hace que una experiencia de usuario sea sencilla?

Definimos la simplicidad de la siguiente manera:

**La simplicidad es la reducción o eliminación de un atributo de un diseño que los usuarios de destino conocen y consideran no esencial.**

En la práctica, la simplicidad se logra mediante la selección del conjunto de características correcto y la presentación de las características de la manera correcta. Esto reduce el valor no esencial, real y percibido.

La simplicidad depende de la percepción de los usuarios. Tenga en cuenta cómo el efecto de una transmisión automática depende de la perspectiva de un usuario:

-   Para el controlador típico (el usuario de destino), una transmisión automática elimina la necesidad de un cambio de engranaje manual y un desplazamiento, lo que facilita mucho la conducción de un automóvil. Un cambio de marcha manual y una conducción no son esenciales para la tarea de conducción, por lo que se quitan para lograr simplicidad.
-   Para un piloto de carreras profesional, tener control directo sobre la transmisión es esencial para ser competitivo. Una transmisión automática afecta negativamente al rendimiento del automóvil, por lo que no se considera que da lugar a simplicidad.
-   Para una mecánica, una transmisión automática es un mecanismo más complejo y, por tanto, no es más fácil de reparar o mantener que una transmisión manual. A diferencia de la mecánica, el usuario de destino no es consciente de esta complejidad interna.

Aunque distintos usuarios consideran la transmisión automática de manera diferente, es correcta porque elimina la necesidad de conocimientos, aptitudes y esfuerzos no esenciales de sus usuarios de destino. Para el controlador típico, la transmisión automática es una gran característica porque simplemente funciona.

### <a name="simplicity-vs-ease-of-use"></a>Simplicidad frente a facilidad de uso

La simplicidad, cuando se aplica correctamente, da lugar a facilidad de uso. Pero la simplicidad y la facilidad de uso no son los mismos conceptos. La facilidad de uso se logra cuando los usuarios pueden realizar una tarea correctamente por sí mismos sin dificultades ni confusión en un período de tiempo adecuado. Hay muchas maneras de lograr facilidad de uso y la simplicidad (la reducción de lo no esencial) es solo una de ellas.

Todos los usuarios, independientemente de lo sofisticados que sean, quieren realizar su trabajo con una cantidad mínima de esfuerzo innecesario. Todos los usuarios, incluso los usuarios avanzados, están principalmente motivados para realizar su trabajo, no para obtener información sobre los equipos o la aplicación.

La simplicidad es la manera más eficaz de lograr la facilidad de uso y la facilidad de uso es igual a su uso. Las características complejas y difíciles de usar simplemente no se usan. Por el contrario, los diseños sencillos y elegantes que realizan bien su función son una buena opción para su uso. Invocan una respuesta positiva y emocional.

Por ejemplo, considere la compatibilidad con redes inalámbricas en Microsoft Windows XP. Microsoft podría haber agregado un asistente para llevar a los usuarios a través del proceso de configuración. Este enfoque habría dado lugar a facilidad de uso, pero no simplicidad, porque se habría agregado una característica no esencial (el asistente). En su lugar, Microsoft diseñó redes inalámbricas para configurarse automáticamente. En última instancia, a los usuarios no les importan los detalles de configuración, siempre que "funcionen" de forma confiable y segura. Esta combinación de potencia y simplicidad en la tecnología de red inalámbrica ha llevado a su popularidad y adopción rápida.

**Si solo hace una cosa...**

Inicie el proceso de diseño con los diseños más sencillos que hacen bien el trabajo.

Si no está satisfecho con el diseño actual, empiece por quitar todos los elementos no esenciales. Verá que lo que queda suele ser bastante bueno.

## <a name="obtaining-simplicity-while-maintaining-power"></a>Obtención de simplicidad al mismo tiempo que se mantiene la eficacia

### <a name="design-principles"></a>Principios de diseño

Para obtener simplicidad, diseñe siempre para lo probable, no para lo posible.

Lo posible

Las decisiones de diseño basadas en lo posible conducen a interfaces de usuario complejas como el Editor del Registro, donde el diseño supone que todas las acciones son igualmente posibles y, como resultado, requieren el mismo esfuerzo. Dado que todo es posible, los objetivos del usuario no se tienen en cuenta en las decisiones de diseño.

El probable

Diseñe decisiones basadas en el posible resultado de soluciones simplificadas, basadas en objetivos y tareas, donde los escenarios probables reciben el foco y requieren un esfuerzo mínimo para realizar.

Principio de diseño de simplicidad

**Para obtener simplicidad, céntrate en lo que es probable; reducir, ocultar o quitar lo que es poco probable; y eliminar lo que es imposible.**

Lo que harán los usuarios es mucho más importante para el diseño que lo que podrían hacer.

### <a name="design-techniques"></a>Técnicas de diseño

Para obtener simplicidad mientras se mantiene la potencia, elija el conjunto adecuado de características **,** busque las características en los lugares adecuados y **reduzca** el esfuerzo para usarlas. En esta sección se den algunas técnicas comunes para lograr estos objetivos.

Elección del conjunto de características adecuado

"Se logra la insondez, no cuando no hay nada más que agregar,

pero cuando no queda nada que quitar". —Loba de Saint-Exupery

Las siguientes técnicas de diseño dan a los usuarios las características que necesitan a la vez que logran la simplicidad mediante la reducción o eliminación reales:

-   **Determine las características que necesitan los usuarios.** Comprenda las necesidades de los usuarios mediante el análisis de objetivos, escenarios y tareas. Determine un conjunto de características que se ajusten a estos objetivos.
-   **Quitar elementos innecesarios.** Quite los elementos que no es probable que se utilicen o que tengan alternativas preferibles.
-   **Quite la redundancia innecesaria.** Puede haber varias maneras eficaces de realizar una tarea. Para lograr la simplicidad, tome la decisión más difícil y elija la mejor para los usuarios de destino en lugar de proporcionarlas todas y hacer que la elección sea una opción.
-   **Haga que "funcione" automáticamente.** El elemento es necesario, pero cualquier interacción del usuario para que funcione no se debe a que hay un comportamiento o una configuración predeterminados aceptables. Para lograr la simplicidad, haga que funcione automáticamente y oculte al usuario por completo o reduzca significativamente su exposición.

Secuenciación de la presentación

"La capacidad de simplificar significa eliminar lo innecesario

para que lo necesario pueda hablar". —HansMann

Use las siguientes técnicas de diseño para conservar la potencia, a la vez que logra la simplicidad a través de la percepción de reducción o eliminación:

-   **Combine lo que se debe combinar.** Coloque las características esenciales que admiten una tarea conjuntamente para que se pueda realizar una tarea en un solo lugar. Los pasos de la tarea deben tener un flujo unificado y optimizado. Dividir tareas complejas en un conjunto de pasos sencillos y claros, para que "uno" pueda constar de varias superficies de interfaz de usuario, como un asistente.
-   **Separe lo que se debe separar.** No todo se puede presentar en un solo lugar, por lo que siempre hay límites claros y bien elegidos. Haga que las características que admiten escenarios principales son centrales y obvias, y ocultan la funcionalidad opcional o la convierten en periférico. Separe las tareas individuales y proporcione vínculos a tareas relacionadas. Por ejemplo, las tareas relacionadas con la manipulación de fotos deben estar claramente separadas de las tareas relacionadas con la administración de colecciones de fotos, pero deben ser fácilmente accesibles entre sí.
-   **Elimine lo que se puede eliminar.** Realice una impresión del diseño y resalte los elementos usados para realizar las tareas más importantes. Incluso resalte las palabras individuales en el texto de la interfaz de usuario que comunican información útil. Ahora revise lo que no está resaltado y considere la posibilidad de quitarlo del diseño. Si quita el elemento, ¿ocurriría algo malo? Si no es así, quítelo.
-   La coherencia, la configuración y la generalización suelen ser calidades deseables, pero pueden dar lugar a una complejidad innecesaria. Revise el diseño de los esfuerzos equivocados en coherencia (por ejemplo, tener texto redundante), generalización (por ejemplo, tener cualquier número de zonas horarias cuando dos son suficientes) y capacidad de configuración (por ejemplo, opciones que los usuarios no es probable que cambien) y eliminar lo que se puede eliminar.
-   **Coloque los elementos en el lugar correcto.** Dentro de una ventana, la ubicación de un elemento debe seguir su utilidad. Los controles, instrucciones y explicaciones esenciales deben estar en contexto en orden lógico. Si se necesitan más opciones, expongalas en contexto haciendo clic en un botón de contenido adicional o un mecanismo similar. Si se necesita más información, muestre una información sobre cómo mantener el mouse sobre el mouse. Coloque tareas, opciones e información de Ayuda menos importantes fuera del flujo principal en una ventana o página independientes. La técnica de mostrar detalles adicionales según sea necesario se denomina divulgación progresiva.
-   **Usar combinaciones significativas de alto nivel.** A menudo es más sencillo y escalable seleccionar y manipular grupos de elementos relacionados que elementos individuales. Entre los ejemplos de combinaciones de alto nivel se incluyen carpetas, temas, estilos y grupos de usuarios. Estas combinaciones a menudo se asignan a un objetivo o intención del usuario que no es evidente a partir de los elementos individuales. Por ejemplo, la intención detrás del contraste alto de color negro es mucho más evidente que la de un fondo de ventana negra.
-   **Seleccione los controles correctos.** Los elementos de diseño se representan mediante los controles que se usan para representarlos, por lo que la selección del control correcto es fundamental para una presentación eficaz. Por ejemplo, el cuadro de selección de fuentes usado por Microsoft Word muestra una vista previa de la fuente, así como las fuentes usadas más recientemente. De forma similar, la forma en que Word muestra posibles errores ortográficos y gramaticales en su lugar es mucho más sencilla que la alternativa del cuadro de diálogo, como se muestra al principio de este artículo.

Reducción del esfuerzo

"Las cosas simples deben ser sencillas.

Deben ser posibles cosas complejas". —Alan Kay

Las siguientes técnicas de diseño reducen el esfuerzo de los usuarios:

-   **Hacer que las tareas sean reconocibles y visibles.** Todas las tareas, pero especialmente las tareas frecuentes, deben poder detectarse fácilmente dentro de la interfaz de usuario. Los pasos necesarios para realizar tareas deben ser visibles y no deben basarse en la memoria.
-   **Presentar tareas en el dominio del usuario.** El software complejo requiere que los usuarios asignen sus problemas a la tecnología. El software simple hace esa asignación para ellos mediante la presentación de lo que es natural. Por ejemplo, una característica de reducción de ojos rojos se asigna directamente al espacio con problemas y no requiere que los usuarios piensen en términos de detalles como matiz y degradados.
-   **Coloque el conocimiento del dominio en el programa.** No es necesario que los usuarios accedan a información externa para usar la aplicación correctamente. El conocimiento del dominio puede abarcar desde algoritmos y datos complejos hasta simplemente dejar claro qué tipo de entrada es válido.
-   **Use el texto que los usuarios entiendan.** El texto bien diseñado es fundamental para una comunicación eficaz con los usuarios. Use conceptos y términos familiares para los usuarios. Explique completamente lo que se pide en lenguaje sin formato para que los usuarios puedan tomar decisiones inteligentes e informadas.
-   **Use valores predeterminados seguros, seguros y probables.** Si una configuración tiene un valor que se aplica a la mayoría de los usuarios en la mayoría de las circunstancias y esa configuración es segura y segura, úsela como valor predeterminado. Haga que los usuarios especifiquen valores solo cuando sea necesario.
-   **Use restricciones.** Si hay muchas maneras de realizar una tarea, pero solo algunas son correctas, restrinja la tarea a esas maneras correctas. No se debe permitir que los usuarios realicen errores fácilmente prevenibles.

### <a name="simplicity-does-not-mean-simplistic"></a>La simplicidad no significa simplista

"Todo debe ser lo más sencillo posible,

pero no es más sencillo". —Ya sea Asíns

Creemos que la simplicidad es fundamental para una experiencia de usuario eficaz y deseable, pero siempre es posible llevar algo bueno demasiado lejos. La esencia de la simplicidad es la reducción o eliminación de lo no esencial. La eliminación de lo esencial simplemente produce un diseño deficiente. Si la "simplificación" provoca que los usuarios se sientan frustrados, confusos, desconfiados o no puedan completar las tareas correctamente, ha quitado demasiado.

### <a name="simplicity-does-mean-more-effort-for-you"></a>La simplicidad implica más esfuerzo

"Solo he hecho esta letra más tiempo porque

no es el momento de que sea más corto". —Blaise Pascal

La obtención de simplicidad a la vez que se conserva la potencia a menudo requiere una complejidad interna considerable. Normalmente es más fácil diseñar software que expone toda la tecnología que diseñar uno que lo oculte; este último requiere una excelente comprensión de los usuarios de destino y sus objetivos. La eliminación de una característica requiere disciplina, al igual que decidir no agregar esa característica interesante que realmente no es práctica. La simplicidad requiere la toma de decisiones de diseño duro en lugar de hacer que todo sea configurable. El software complejo suele ser el resultado de una idea errónea sobre los usuarios: que valoran las características no utilizadas o las características demasiado complejas que no pueden entender.

## <a name="powerful-and-simple"></a>Eficaz y sencillo

La capacidad es permitir a los usuarios y hacer que sean productivos. La simplicidad se centra en quitar las características no esenciales y presentar las correctamente. Al comprender a los usuarios de destino y lograr el equilibrio adecuado de características y presentación, puede diseñar aplicaciones basadas en Windows que hacen ambas cosas.

 

 