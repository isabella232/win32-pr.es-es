---
title: Interfaz de usuario induce
description: En este tema se describe el modelo de interfaz de usuario conocido como interfaz de usuario induce (IUI).
ms.assetid: d99dc30a-68e5-4b7a-8cbd-0ac77a90a354
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 632e16191b7103cbf6be9fe209ada78781d4a53c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268255"
---
# <a name="inductive-user-interface"></a>Interfaz de usuario induce

En este tema se describe el modelo de interfaz de usuario conocido como interfaz de usuario induce (IUI). También se denomina navegación induce, el modelo IUI sugiere cómo hacer que las aplicaciones de software sean más sencillas al dividir las características en pantallas o páginas que son fáciles de explicar y comprender. Este modelo IUI es evidente en varios proyectos de Microsoft, como Microsoft Money 2000, las applets del panel de control de Windows, varias pantallas y cuadros de diálogo de Microsoft Visual Studio 2010 y los paneles de tareas de Microsoft Office.

-   [Introducción](#introduction)
-   [IUI en acción: solucionar un problema de diseño común](#iui-in-action-solving-a-common-design-problem)
    -   [Problema: el software es difícil de usar](#the-problem-software-is-hard-to-use)
    -   [Interfaz de usuario de deducción](#deductive-user-interface)
    -   [Una solución: interfaz de usuario induce](#a-solution-inductive-user-interface)
-   [Pasos para crear una interfaz de usuario induce](#steps-for-creating-an-inductive-user-interface)
    -   [Paso 1: centrar cada página en una sola tarea](#step-one-focus-each-page-on-a-single-task)
    -   [Paso dos: estado de la tarea](#step-two-state-the-task)
    -   [Paso tres: hacer que el contenido de la página se ajuste a la tarea](#step-three-make-the-pages-contents-suit-the-task)
    -   [Paso cuatro: ofrecer vínculos a las tareas secundarias](#step-four-offer-links-to-secondary-tasks)
-   [Directrices adicionales](#additional-guidelines)
    -   [Usar plantillas de pantalla coherentes](#use-consistent-screen-templates)
    -   [Hacer que sea obvio cómo llevar a cabo la tarea con los controles de la pantalla](#make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen)
    -   [Proporcionar una manera fácil de completar una tarea e iniciar una nueva](#provide-screens-for-starting-tasks)
    -   [Hacer obvio el siguiente paso de navegación](#make-the-next-navigational-step-obvious)
-   [Asistencia al usuario](#user-assistance)
    -   [Ayuda principal](#primary-assistance)
    -   [Asistencia secundaria](#secondary-assistance)
-   [Apéndice: diseño y prueba de Microsoft Money 2000](#appendix-designing-and-testing-microsoft-money-2000)
    -   [Diseño y prueba de Money 2000](#designing-and-testing-money-2000)
    -   [Pruebas de facilidad de uso](#usability-tests)
    -   [Comparación con sitios web](#comparison-with-web-sites)

## <a name="introduction"></a>Introducción

IUI es un modelo de interfaz de usuario que sugiere cómo hacer que las aplicaciones de software sean más sencillas mediante la división de características en pantallas o páginas que son fáciles de explicar y comprender. Microsoft ha implementado este modelo en Money 2000, una aplicación de software comercial de gran tamaño. Las pruebas informales sugieren que los usuarios pueden realizar tareas tan rápidamente en este modelo como en las interfaces tradicionales y pueden encontrar cosas más fácilmente.

Muchas aplicaciones de software comercial incluyen interfaces de usuario en las que una pantalla presenta un conjunto de controles, pero la deja al usuario para deducir el propósito de la página y cómo usar los controles para lograr ese propósito.

Los principios descritos en este documento no requieren ni implican ningún conjunto rígido determinado de diseños, controles o elementos visuales. Al igual que las interfaces gráficas de usuario en general, los principios de este documento dejan una gran cantidad de espacio para la flexibilidad y la creatividad en el diseño.

Los principios generales de la interfaz de usuario inductoras se muestran con ejemplos obtenidos de Money 2000.

> [!IMPORTANT]
> El concepto general de IUI se encuentra en su conjunto. Los diseñadores que emplean estas técnicas son el aprendizaje y la detección de más información a medida que la usan para su software. La información de este documento evolucionará con el tiempo a medida que aumenta la investigación y el conocimiento de esta área. En este tema se proporciona una introducción a IUI, en lugar de un conjunto integral de instrucciones.

 

## <a name="iui-in-action-solving-a-common-design-problem"></a>IUI en acción: solucionar un problema de diseño común

En esta sección se describe un problema de diseño común con los productos de software de hoy en día y se presenta IUI como técnica para superar el problema.

### <a name="the-problem-software-is-hard-to-use"></a>Problema: el software es difícil de usar

La mayoría de los programas de software son demasiado difíciles de usar. Esta conclusión se obtiene de las pruebas de facilidad de uso, evidencia de anécdota y experiencias personales de los diseñadores de software. El concepto de IUI se creó mediante la realización de la investigación, lo que hizo que se propongan las conjeturas en lo que hace que el software actual sea difícil de usar y, después, proponga soluciones. Los diseñadores que usan IUI deben confiar en la satisfacción del cliente para determinar el éxito final del diseño.

La mayoría de los productos de software actuales son difíciles de usar por los siguientes motivos generales:

-   Los usuarios no parecen construir un modelo mental adecuado del producto.

    El diseño de la interfaz para la mayoría de los productos de software actual supone que los usuarios comprenderán un modelo conceptual que los diseñadores diseñaron cuidadosamente. Desafortunadamente, la mayoría de los usuarios no parecen adquirir un modelo mental que sea lo suficientemente exhaustivo y preciso como para guiar su navegación. Es probable que estos usuarios estén muy ocupados y estén sobrecargados con información. No tienen el tiempo, la energía o el deseo de estudiar un modelo conceptual para su software.

-   Incluso muchos usuarios de larga duración nunca dominan los procedimientos comunes.

    Los diseñadores saben que los nuevos usuarios pueden tener problemas al principio, pero esperan que estos problemas desaparecen a medida que los usuarios aprenden tareas comunes. Los datos de facilidad de uso indican que esto no suele ocurrir. En un estudio, los investigadores configuran equipos automatizados para los usuarios de videocintas en casa. Las cintas mostraron que los usuarios que se centran en la tarea a mano no detectan necesariamente el procedimiento que siguen y no aprenden de la experiencia. La próxima vez que los usuarios realicen la misma operación, pueden caso de la misma manera.

-   Los usuarios deben trabajar de forma difícil para averiguar cada característica o pantalla.

    La mayoría de los productos de software están diseñados para (los pocos) usuarios que entienden su modelo conceptual y tienen procedimientos comunes con patrones. Para la mayoría de los clientes, cada característica o procedimiento es un rompecabezas frustrante y no deseado. Los usuarios podrían suponer que estos rompecabezas son un costo inevitable del uso de equipos, pero ciertamente serían más contentos sin esta carga.

La mejor solución para estos problemas es encontrar una estrategia general para que las características de los productos de software sean más evidentes y fáciles de entender. Los usuarios deben poder encontrar una característica cada vez que la necesiten, y deben poder usar esa característica cada vez que deseen usarla.

### <a name="deductive-user-interface"></a>Interfaz de usuario de deducción

La mayoría de los elementos del software hoy en día requieren que el usuario los estudie y deduzca su comportamiento, tal como se muestra en la siguiente captura de pantalla.

![captura de pantalla de un cuadro de diálogo de propiedades de ejemplo.](images/iuiguidelines01.png)

Los usuarios experimentados de equipos, incluidos los diseñadores de software, reconocen rápidamente que este cuadro de diálogo les permite administrar una lista de cosas. Comprenden los botones que aparecen debajo de la lista pueden agregar, quitar y proporcionar información sobre los elementos de la lista. Sin embargo, tenga en cuenta que ninguno de estos comportamientos se indica explícitamente en el propio cuadro de diálogo.

Eche un vistazo a este cuadro de diálogo desde el punto de vista de un usuario ocasional. Muchos usuarios, cuando se enfrentan a este cuadro de diálogo, preguntarán "¿qué se supone hacer con esto?". Cuando aparece el cuadro de diálogo, el usuario debe detenerse y averiguar qué hacer a continuación. En primer lugar, el usuario debe deducir el hecho de que el rectángulo blanco grande es un cuadro de lista vacío que se va a rellenar con elementos. La etiqueta de texto pequeño del cuadro, "cosas", ofrece una sugerencia imprecisa. Algunos usuarios intentarían escribir en el cuadro de lista, ya que se parece a un cuadro de texto de edición.

Después, el usuario debe deducir que los botones situados debajo de la lista afecten a su contenido. Algunos de los botones están deshabilitados inicialmente, que es otro origen potencial de confusión del usuario. El usuario debe experimentar con los controles para obtener información sobre cómo funciona el cuadro de diálogo.

El usuario también podría plantear otras preguntas: "¿cuántos elementos debo incluir en la lista? ¿Debo escribir elementos en un orden específico? ¿Por qué se obtiene este cuadro de diálogo en primer lugar? ¿Para qué sirve? "

Los usuarios se distraerán de sus objetivos siempre que deban averiguar el propósito de una pantalla y cómo usarla. En última instancia, representa un costo en el tiempo y la satisfacción del usuario. Incluso peor, los usuarios pagan este costo una y otra vez cuando se reinician a través de la interfaz cada vez que usan una característica.

Una pantalla debe tener un título que explique claramente su finalidad. Cuando los diseñadores crean una pantalla, rara vez necesitan tener un propósito claramente invisible. En su lugar, puede ser simplemente parte de un modelo conceptual más grande que el usuario debe deducir.

Los estudios demuestran que muchos usuarios están confundidos incluso por operaciones básicas en el software. Tienen dificultades para comprender lo que puede hacer el producto para ellos, dónde ir para realizar una operación y cómo realizar esa operación una vez que se han encontrado. La simplificación del software mediante la realización de cambios fundamentales es una manera eficaz de satisfacer mejor a los clientes existentes y atraer a los nuevos usuarios.

### <a name="a-solution-inductive-user-interface"></a>Una solución: interfaz de usuario induce

Como una nueva forma de diseñar el software, el objetivo de IUI es reducir la cantidad de pensamiento extraño que los usuarios deben hacer para moverse correctamente entre las partes de un producto y usar sus características. La palabra inductivo proviene de la inducción del verbo, lo que significa que debe conducir o moverse por influencia o PERSUASION.

IUI es una extensión de la interfaz de estilo Web común. En el entorno Web, las páginas deben ser simples y basadas en tareas, ya que cada fragmento de información se tiene que enviar a un servidor a través de una conexión relativamente lenta. Después, el servidor responde con el paso siguiente, y así sucesivamente. Un buen diseño web significa centrarse en una sola tarea por página y proporcionar navegación a través de las páginas. Del mismo modo, la navegación induce comienza con centrar la actividad en cada página en una única tarea principal.

Una interfaz induzca bien diseñada ayuda a los usuarios a responder a dos preguntas básicas a las que se encuentran al mirar una pantalla:

-   ¿Qué debo hacer ahora?
-   ¿Dónde puedo ir desde aquí para realizar la siguiente tarea?

El software diseñado según estos principios responde a estas preguntas a partir de una premisa fundamental: una pantalla con un solo propósito explícito y claramente indicado es más fácil de entender que una página sin este propósito. Si la pantalla es más fácil de entender, será más fácil que el usuario sepa qué hacer y dónde ir a continuación.

Esta premisa fundamental se puede expandir en una serie de cuatro pasos para diseñar software que use IUI:

-   Centrar cada pantalla en una sola tarea.
-   Indique la tarea.
-   Haga que el contenido de la pantalla se ajuste a la tarea.
-   Ofrecen vínculos a las tareas secundarias.

Aunque en este documento se describen los principios generales de IUI, también se muestran los principios de acción al mostrar ejemplos de Money 2000 y otro software. Debería pensar en estos ejemplos como expresiones particulares de IUI, no en un modelo estricto de implementación.

Además de los cuatro pasos indicados anteriormente, puede reforzar la interfaz siguiendo estas cinco instrucciones:

-   Use plantillas de pantalla coherentes.
-   Proporcionar pantallas para iniciar tareas.
-   Sea obvio cómo llevar a cabo la tarea con los controles de la pantalla.
-   Proporcionar una manera fácil de completar una tarea e iniciar una nueva.
-   Haga obvio el siguiente paso de navegación.

### <a name="processes"></a>Procesos

Muchas tareas requieren que los usuarios naveguen por una serie de pantallas. Un usuario que realiza una tarea puede hacer clic en un vínculo a una tarea secundaria que se aleja de la secuencia de pantallas que componen la tarea principal. Cuando el usuario completa la tarea secundaria, debe haber una manera fácil de devolver el usuario directamente al punto de bifurcación en la tarea original. Es probable que los usuarios tengan problemas al usar controles de navegación convencionales, como los botones **atrás** y **adelante** , para volver a la ubicación en la que se iniciaron.

Para proporcionar esta capacidad, IUI define un concepto de navegación denominado proceso, una pantalla o una serie de pantallas que realizan una tarea. Un proceso actúa como una subrutina de navegación. Los usuarios pueden iniciar un proceso, trabajar en su serie de pantallas y, a continuación, en la última página, hacer clic en un botón "listo" para volver rápidamente a la página donde comenzaron el proceso.

## <a name="steps-for-creating-an-inductive-user-interface"></a>Pasos para crear una interfaz de usuario induce

En esta sección se describen detalladamente los cuatro pasos que puede usar para crear un IUI.

### <a name="step-one-focus-each-page-on-a-single-task"></a>Paso 1: centrar cada página en una sola tarea

El primer paso para diseñar un IUI es tomar una característica o un conjunto de características y dividirla en pantallas independientes. Cada pantalla debe centrarse en una sola tarea, denominada tarea principal de la pantalla.

Esta idea suena simple, pero pocas aplicaciones la siguen. La mayoría de las aplicaciones presentan una pantalla en la que se realizan todas las características relacionadas. Este diseño requiere que los usuarios puedan averiguar (deducir) lo que se puede hacer y cómo hacerlo.

La tarea principal puede ser específica o ser abierta. Por ejemplo, en un programa de finanzas personal, una tarea específica podría ser "seleccionar la factura que desea pagar", mientras que una tarea abierta podría ser "revisar el rendimiento de las inversiones".

La tarea principal debe ser algo que tenga sentido para el usuario, en lugar de un reflejo de un detalle de implementación u otro concepto abstracto. La tarea debe ser algo que los usuarios piensan hacer, preferiblemente descritos en sus propias palabras.

### <a name="example"></a>Ejemplo

En esta sección se comparan dos versiones diferentes de Money. Los ejemplos muestran características muy similares que permiten a los usuarios ver y administrar cuentas financieras.

El modelo IUI se desarrolló durante la creación de Money 2000, una aplicación para administrar la economía personal. Money 2000 es la octava versión principal del producto. Money 2000 es un programa grande de Windows con más de 1 millón líneas de código.

Money 2000 es una aplicación de estilo Web. No es un sitio web, pero comparte muchos atributos con sitios Web. Su interfaz de usuario se compone de páginas de pantalla completa que se muestran en un marco compartido, con herramientas para retroceder y avanzar a través de una pila de navegación. En esta base, Money 2000 agrega un conjunto de nuevas convenciones de interfaz de usuario que crean una experiencia de usuario más estructurada.

Aunque IUI se usó por primera vez en el diseño de estilo Web de Money 2000, también se puede usar con elementos de interfaz tradicionales como ventanas y cuadros de diálogo.

En Money 99, los usuarios suelen realizar una gran variedad de tareas en una sola pantalla. Por ejemplo, en la siguiente captura de pantalla se muestra el **Administrador de cuentas** que presentó todas las características relacionadas con la cuenta en Money 99 en una sola pantalla.

![captura de pantalla del administrador de cuentas en Money 99.](images/iuiguidelines02.png)

Esta pantalla agrupa una tarea común, navegando a una cuenta, así como tareas poco frecuentes, como la creación y eliminación de cuentas. Ninguna de estas tareas específicas se expresa directamente en el título de la pantalla, en el **Administrador de cuentas**. Muchos usuarios pueden encontrar esta pantalla como un desafío como el cuadro de diálogo de ejemplo en la figura 1. En ambos casos, el usuario debe deducir el propósito de la pantalla y cómo usarla.

Money 2000, que sigue a IUI, ofrece un conjunto casi idéntico de características relacionadas con la cuenta, pero las proporciona en dos pantallas independientes. En la captura de pantalla siguiente se muestra la primera de estas pantallas, que se centra completamente en obtener el usuario para elegir una cuenta.

![captura de pantalla de la pantalla de selección de cuenta en Money 2000.](images/iuiguidelines03.png)

La pantalla de Money 2000 contiene aproximadamente el mismo número de elementos visuales que la pantalla de Money 99 anteriores, pero ahora la página se centra completamente en la obtención del usuario para elegir una cuenta. Por ejemplo, en la versión Money 99, un usuario tenía que hacer dos clics para abrir una cuenta: una para seleccionarla y otra para seleccionar la operación de apertura. En la versión Money 2000, la única razón por la que un usuario hace clic en una cuenta es abrirla, por lo que un solo clic puede bastar. De este modo, aunque el número de pantallas puede aumentar, el número de clics necesarios para realizar una tarea común suele reducirse.

En ocasiones, los usuarios querrán agregar o quitar una cuenta. Para realizar esta tarea en Money 2000, los usuarios navegan a una segunda pantalla (que se muestra en la siguiente captura de pantalla), que se centra en la configuración de las cuentas.

![captura de pantalla de la pantalla de configuración de la cuenta en Money 2000.](images/iuiguidelines04.png)

El propósito de cada pantalla es más claro en la versión IUI de Money 2000. Además, cada pantalla tiene más espacio para dedicar a su propósito. Por ejemplo, el administrador de **cuentas** de Money 99 podría proporcionar muy poco espacio al botón **eliminar cuenta** , porque rara vez se usaba en comparación con los demás comandos de la pantalla. En cambio, la pantalla de configuración de la cuenta de Money 2000 puede incluir este comando de forma más destacada, lo que facilita su detección y su explicación.

### <a name="what-is-a-single-task"></a>¿Qué es una sola tarea?

¿Cómo se puede saber si una pantalla se centra realmente en una sola tarea? Es posible que se explique que una pantalla que admite muchas tareas tiene solo un propósito si ese propósito es lo suficientemente breve. Esta es una regla general: una pantalla se centra en un propósito si el diseñador puede expresar ese propósito con un título de pantalla conciso, significativo y de sonido natural.

Los diseñadores de Money 2000 consideró la división de estas pantallas (**Elija una cuenta para usar** y **Configure sus cuentas en Money**) en más pantallas. Sin embargo, dado que cada pantalla ya tiene un título conciso, significativo y natural, los diseñadores creían que las pantallas se centraron en lo suficiente. Al diseñar una pantalla, si no puede pensar en un título claro y sencillo, es probable que esté intentando conseguir demasiadas cosas en la pantalla.

### <a name="step-two-state-the-task"></a>Paso dos: estado de la tarea

Cada pantalla debe tener un título con una instrucción concisa y explícita de su tarea principal. Puede tratarse de una instrucción directa ("seleccione la cuenta que desea equilibrar") o una pregunta que desee que el usuario responda ("¿qué cuenta desea equilibrar?").

Este es otro principio de sonido sencillo que a menudo no se practica. Por ejemplo, las versiones anteriores de Money tenían pantallas con títulos como el **Administrador de servicios financieros en línea** y el **saldo de cuenta**. Los usuarios tenían que deducir el propósito y el comportamiento de estas pantallas de la organización y las etiquetas de sus controles.

El título de la pantalla o la página es muy importante. Si el producto utiliza ventanas, páginas de estilo Web, cuadros de diálogo u otro diseño, no se debe permitir que el título se desplace.

### <a name="usable-screens-have-clear-titles"></a>Las pantallas que se pueden usar tienen títulos claros

Las pantallas que realizan muchas tareas requieren títulos abstractos o complejos. Por ejemplo, la pantalla de Money 99 que se muestra en la figura 2 permitía al usuario navegar a cuentas y configurar cuentas. El título abstracto "Account Manager" se asignó a esta página en un intento de capturar ambos propósitos. Aunque es posible que los usuarios tengan algunas ideas sobre lo que podría hacer una página de "Administrador de cuentas", es posible que no se dé cuenta de que la tarea más común para esta pantalla era simplemente elegir una cuenta.

Algunas pantallas o comandos tienen fines abstractos que no sugieren fácilmente títulos claros. En estas pantallas, los diseñadores pueden elegir nombres que sean deliberadamente imprecisos, como "configuración", "acuñó buzzwords, como" QuickStep; "o jerga que revela los detalles de implementación (" compactación de base de datos "). Estos tipos de nombres suelen ser confusos o engañosos a los usuarios. Además, estos nombres suelen ser nombres que no expresan la acción que el usuario desea realizar, lo que agrega a la confusión.

A menudo, los títulos de pantalla y otros nombres no se determinan hasta cerca del final del proceso de diseño. A menudo, los diseñadores piden a los redactores que presenten un nombre adecuado para una pantalla una vez diseñado y codificado. En ese momento, no hay ningún recurso en caso de que se encuentre un buen nombre, por lo que es posible que el equipo tenga que pagar los nombres que no estén claros. La solución a este problema es que los diseñadores piensen sobre la claridad en las funciones de pantalla y los títulos al principio del proceso de diseño.

Las funciones de pantalla y los títulos deben centrarse en las tareas más comunes realizadas por los clientes. A menudo, los diseñadores se ven tentados a proporcionar enormes cantidades de funcionalidad en un intento de satisfacer el mayor número de clientes, junto con el deseo del equipo de diseño. Sin embargo, las características adicionales siempre agregan complejidad y otros costos.

### <a name="screen-title-indicates-design-clarity"></a>El título de la pantalla indica claridad del diseño

En el modelo IUI, los diseñadores eligen los títulos de pantalla en las primeras fases del proceso de diseño. En lugar de seleccionar un título para justificar el modo en que funciona la pantalla, el título se usa para determinar si la pantalla tiene sentido. Si no se puede encontrar ningún título adecuado, se rediseña la característica. Si ningún diseño permite un título claro y conciso (es decir, si no hay ninguna manera de explicar la característica), los diseñadores podrían abandonar la característica. En las siguientes capturas de pantalla, compare la pantalla de pago de factura de Money 99 de la izquierda, que proporciona una etiqueta estática para la página ("próximas facturas & depósitos") y la pantalla de Money 2000 correspondiente a la derecha, que tiene un título explícito ("haga clic en la factura que desea pagar"):

![captura de pantalla que muestra un título estático en Money 99 y un título activo en Money 2000.](images/iuiguidelines05.png)

Un título de pantalla, que es simplemente una frase o frase, es más fácil de cambiar que un diseño o código. A pesar de este hecho, la experiencia con IUI ha demostrado que la incumplimiento de un título claro de la pantalla genera mejores diseños. Los títulos deben elegirse con la entrada de los miembros del equipo de educación y facilidad de uso, así como con los diseñadores de productos.

En ocasiones, es posible que los miembros del equipo intenten posponer esta decisión, suponiendo que los clientes compartan la finalidad de la pantalla. Cuando se fuerza a ofrecer una instrucción clara y concisa de este propósito, sin embargo, las diferencias de opinión se suelen revelar. Al resolver estas diferencias y seleccionar un título al principio, las discusiones de diseño pueden continuar de forma más fluida.

Una vez que se elige un título, no debe considerarse inalterable. Los diseñadores probablemente refinan los títulos a lo largo del tiempo, como con cualquier diseño. Sin embargo, el primer título elegido debe ser tan seguro como sea posible en esa fase de desarrollo.

### <a name="guidelines-for-choosing-screen-titles&quot;></a>Directrices para elegir títulos de pantalla

En esta sección se describe una técnica sencilla para elegir buenos títulos de pantalla. Para usar esta técnica, los diseñadores supongan que un amigo pregunta, &quot;¿Qué es esta pantalla?&quot;. y, a continuación, se incluye una respuesta clara y útil que completa la frase &quot;esta es la pantalla donde se encuentra?&quot;. Las palabras que completan la oración se convierten en el título de la pantalla.

Durante el desarrollo de Money 2000, los escritores de documentación del equipo crearon instrucciones de título de pantalla para garantizar la calidad y la coherencia. Por ejemplo, estas instrucciones sugieren títulos que usaban verbos y eran frases como preguntas o instrucciones directas. Los diseñadores evitan nombres estáticos que permitían más abstracción y podrían ser imprecisas.

Para simplificar los títulos, los diseñadores han evitado frases compuestas e intentó usar el lenguaje de conversación, evitando términos y jerga extraños. Si los diseñadores no pueden describir la tarea sin tener que recurrir a conjunciones (&quot;and&quot;, &quot;or"), es probable que la pantalla esté intentando realizar más de una tarea, y es menos probable que el usuario pueda comprender inmediatamente qué hacer.

Incluso cuando se elige un título cuidadosamente, es posible que la región del título sea demasiado pequeña para explicar de manera adecuada una tarea compleja. Para mitigar este problema, puede incluir un breve párrafo descriptivo en la parte superior del área de contenido de la pantalla que se elabora en la tarea.

La tabla siguiente contiene algunos ejemplos de títulos de pantalla en Money 99 y títulos para la misma pantalla o las pantallas relacionadas en Money 2000.



| Títulos de pantalla en Money 99             | Nuevos títulos de pantalla en Money 2000                         | Comentario                                         |
|---------------------------------------|---------------------------------------------------------|-------------------------------------------------|
| **Administrador de cuentas**                   | **Selección de una cuenta** **Configure sus cuentas**<br/> | Título estático cambiado a títulos activos.          |
| **Detalles de la cuenta**                   | **Cambiar la configuración de la cuenta**                                | Título estático cambiado a título específico activo. |
| **Calendario de pago**                  | **Pagar una factura**                                          | Título impreciso: descriptivo.                   |
| **Administrador de servicios financieros en línea** |                                                         | Página no necesaria después del rediseño.                 |



 

### <a name="making-the-screen-title-prominent"></a>Destacar el título de la pantalla

Una vez que haya realizado la liquidación en un título de pantalla útil, es importante asegurarse de que la atención del usuario se dibuje en él. Algunos estudios han demostrado que los usuarios rara vez leen texto informativo. Para ayudar a solucionar este problema, los títulos de pantalla deben diseñarse de forma destacada y atractiva con el fin de atraer la atención del usuario. El diseño visual de la pantalla debe informar al usuario de que el título es lo más importante que se debe leer.

### <a name="step-three-make-the-pages-contents-suit-the-task"></a>Paso tres: hacer que el contenido de la página se ajuste a la tarea

Al crear software que sigue las instrucciones de IUI, el diseño más difícil del trabajo suele implicar las características más importantes en pantallas o páginas. El siguiente paso consiste en determinar qué controles se utilizarán en cada pantalla para realizar su tarea principal. Estos controles conforman el contenido de la página, donde el usuario realiza el trabajo. El título y el contenido de la pantalla son dos mitades de un diálogo entre el programa y el usuario. El título representa la pregunta del programa o proporciona una instrucción y el usuario responde a través de la interfaz de la pantalla.

Si el título de la pantalla es claro y sencillo, el diseño de la pantalla suele ser sencillo. Por ejemplo, una de las pantallas de Money 2000 mostradas anteriormente se titula "elegir una cuenta para usar". Dado este título, la pantalla obviamente debe contener una lista sencilla de cuentas de las que el usuario puede elegir. Otra pantalla de Money 2000 tiene el título "comprobación de los elementos que se van a incluir en los impuestos". Naturalmente, esta pantalla contiene una lista de comprobación de elementos.

Los usuarios deben poder averiguar fácilmente cómo usar los controles para lograr la tarea principal de la pantalla. Cuando se indica a los usuarios que seleccionen una cuenta y pueden buscar una lista de cuentas, confirman su comprensión de la tarea. Esto aumenta la posibilidad de que los usuarios se realicen correctamente, lo que también aumenta su confianza en la realización de otras tareas.

### <a name="screen-content-areas"></a>Áreas de contenido de pantalla

La ubicación exacta y la forma de las áreas de contenido de pantalla dependen del diseño del software. En Money 2000, la región de contenido de pantalla es todo debajo del título de la pantalla y a la derecha de la lista de tareas. Esta región puede desplazarse en pantallas largas. Algunos contenidos no esenciales también pueden aparecer en el área de estado debajo de la lista de tareas.

Los diseñadores pueden optar por elaborar la tarea principal de la pantalla en un párrafo situado en la parte superior de la región de contenido. No es necesario que los usuarios lean este texto, pero pueden resultar útiles. Muchos usuarios pueden omitirla y seguir usando la pantalla correctamente. A diferencia del título, esta descripción puede desplazarse si la pantalla es desplazable. Para obtener más información, consulte [directrices para elegir títulos de pantalla](#guidelines-for-choosing-screen-titles).

Si los diseñadores quieren que una página muestre avisos no esenciales, alertas u otra información de estado, se puede mostrar a la izquierda del área de contenido principal, en la lista de tareas en el lado izquierdo de la pantalla. Funcionalmente, esta área de estado es una región adicional para el contenido de la pantalla. Esta área no es lo suficientemente destacada como para contener controles esenciales.

### <a name="provide-a-clear-exit-from-the-page"></a>Proporcionar una salida clara en la página

Después de completar correctamente una tarea, el usuario se enfrenta a otro problema: Cuándo y cómo salir de la pantalla. En el caso de las pantallas cuya tarea principal es la navegación, la realización de la propia tarea mueve al usuario a la pantalla siguiente. En otras pantallas, puede ser más difícil para el usuario saber cómo proceder. Por ejemplo, en una pantalla que pide al usuario que escriba información en los campos, es posible que el usuario necesite ayuda para averiguar cuándo y cómo moverse. En estas páginas, a menudo resulta útil ofrecer un botón Borrar **siguiente** o **listo** en una ubicación coherente.

Los estudios de facilidad de uso han demostrado que los usuarios prefieren usar tales botones incluso cuando están disponibles botones de navegación globales, como los botones **atrás** o **Inicio** de una barra de herramientas. A menudo, los usuarios están incómodos en las pantallas sin salir sin cifrar, incluso las pantallas cuyo único propósito es proporcionar información que se va a leer.

Para obtener más información sobre este tema, vea [proporcionar una manera fácil de completar una tarea e iniciar una nueva](#provide-screens-for-starting-tasks) en la sección directrices adicionales.

### <a name="step-four-offer-links-to-secondary-tasks"></a>Paso cuatro: ofrecer vínculos a las tareas secundarias

El último paso en el diseño de una pantalla es proporcionar vínculos a las tareas secundarias, que son características que no realizan directamente la tarea principal, sino que están relacionadas con la pantalla. Por ejemplo, si la tarea principal de una pantalla es escribir una letra, las tareas secundarias en esa pantalla podrían ser buscar una dirección de correo electrónico o imprimir un sobre.

Las tareas secundarias pueden mostrar cuadros de diálogo, cambiar la presentación visual del contenido de la pantalla o desplazarse al usuario a otra pantalla. Una tarea secundaria podría realizar indirectamente la tarea principal o podría redirigir a los usuarios perdidos al lugar en el que están buscando.

Si una página es una conversación entre el equipo y el usuario, una tarea secundaria permite al usuario omitir la pregunta actual del equipo y pedir al equipo que haga otra cosa. Por ejemplo, Imagine este cuadro de diálogo: equipo: "¿qué factura desea pagar?" Usuario: "en realidad, lo que realmente quiero hacer es encontrar una factura que me he pagado una vez".

Algunas pantallas del producto no tendrán tareas secundarias, mientras que otras tendrán varias. Debe evitar crear una larga lista de tareas que probablemente sean difíciles de examinar para el usuario. Si una pantalla tiene una lista relativamente larga de tareas secundarias, las tareas más comunes deben colocarse primero, agruparse en una sección independiente o, de lo contrario, resaltarse visualmente.

La lista no debe incluir cada tarea secundaria imaginable, siempre y cuando el siguiente paso de navegación sea obvio. En lugar de ofrecer muchas tareas secundarias, una pantalla puede proporcionar tareas secundarias que desplazan a las páginas de subsidiarias que muestran más tareas.

### <a name="visual-design-of-secondary-tasks"></a>Diseño visual de tareas secundarias

Las tareas secundarias deben aparecer en una posición subordinada en la pantalla, donde se puede acceder a ellas si es necesario, pero no distraer al usuario de la tarea principal. Colocar esta lista en una posición coherente en cada pantalla ayuda a los usuarios a encontrar la lista rápidamente cuando la necesiten.

Si muestra la lista de tareas secundarias en el lado izquierdo de la pantalla, la propia lista no debe ser desplazable, ni debe desplazarse por la página, como se muestra en la siguiente captura de pantalla de la pantalla de **pago de facturación** de Money 2000.

![captura de pantalla de la pantalla de pago de facturación en Money 2000.](images/iuiguidelines07.png)

## <a name="additional-guidelines"></a>Directrices adicionales

En esta sección se describen cinco instrucciones útiles para crear un IUI de acuerdo con los cuatro pasos descritos en la sección anterior.

### <a name="use-consistent-screen-templates"></a>Usar plantillas de pantalla coherentes

Al diseñar software que sigue el modelo IUI, debe crear una plantilla que se usará como guía para cada pantalla. El modelo inductor no indica que se use una plantilla determinada. Existen muchas variaciones posibles que pueden satisfacer un diseño inductivo. Es posible que el producto solo necesite una plantilla para todas sus pantallas, o puede crear varias plantillas diferentes para distintos propósitos.

Una buena plantilla permite a un nuevo usuario comprender rápidamente el funcionamiento de las pantallas del producto. El uso coherente de la plantilla en las pantallas del producto proporciona un buen flujo de la interfaz de usuario de la pantalla a la pantalla. A medida que los usuarios aprenden a esperar que los mismos elementos aparezcan en los mismos lugares, pueden examinar y empezar a usar cada pantalla nueva con mayor rapidez.

### <a name="provide-screens-for-starting-tasks"></a>Proporcionar pantallas para iniciar tareas

Los productos diseñados con IUI suelen usar pantallas especiales diseñadas para iniciar usuarios en conjuntos de tareas. Estas pantallas se denominan páginas de actividad porque organizan grupos relacionados de tareas comunes. Las páginas de actividad proporcionan un punto de partida para los usuarios. Normalmente, una página de actividad presenta vínculos a otras páginas en las que el usuario realmente realiza el trabajo. Páginas de actividades pregunte al usuario "¿qué desea hacer ahora?" y presentan una lista de respuestas posibles. Las páginas de actividad pueden seguir una plantilla especial para ayudar a los usuarios a reconocerlas.

Una página de actividad crea una buena página de inicio predeterminada para un producto. Cuando los usuarios inician una aplicación, generalmente tienen una idea sobre la tarea que quieren realizar. Normalmente, el motivo por el que se inicia el producto es uno de un número reducido de tareas muy comunes. La página de inicio predeterminada del producto lo reconoce haciéndolo obvio cómo comenzar las tareas comunes.

La página **principal** de Money 2000 es un ejemplo de una página de actividad. De forma predeterminada, los usuarios ven esta pantalla, donde se muestra el acceso a las tareas financieras comunes, como pagar una factura y equilibrar una cuenta, cuando inician la aplicación.

En la captura de pantalla siguiente se muestra la página **principal** de Money 2000.

![captura de pantalla de la Página principal de Money 2000. Página de actividad en la que se enumeran algunas tareas comunes y se proporcionan vínculos a conjuntos de tareas en otras páginas.](images/iuiguidelines08.png)

Dado que Money proporciona muchas características financieras, solo las tareas financieras más comunes se ajustan a la página **principal** . Para todas las demás tareas, la página **principal** se vincula a un conjunto subsidiario de páginas de actividad denominadas centros financieros. Cada área principal de Money proporciona un centro financiero. Estas pantallas presentan el siguiente nivel de tareas, que actúa como punto de partida para todas las características de cada área.

Por ejemplo, el área de **impuestos** de dinero contiene las características relacionadas con los impuestos del producto. El área de **impuestos** ofrece vínculos a estas características en una página del **centro de impuestos** , tal como se muestra en la siguiente captura de pantalla.

![captura de pantalla de la página del centro de impuestos de Money 2000. ](images/iuiguidelines09.png)

Una página de actividad también puede ser mucho más sencilla si hay menos opciones disponibles. En la captura de pantalla siguiente se muestra cómo se puede usar una página de actividad para administrar cuentas de usuario de Windows.

![captura de pantalla de una página de actividades de Money 2000 para administrar cuentas de usuario de Windows. ](images/iuiguidelines10.png)

### <a name="make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen"></a>Hacer que sea obvio cómo llevar a cabo la tarea con los controles de la pantalla

La mejor manera de seguir esta directriz es elegir un título de pantalla adecuado y limitar el ámbito de las tareas principales a la más común. Una vez que haya llegado a un título y propósito claros para la página, la elección del conjunto de controles correcto será sencilla.

### <a name="provide-an-easy-way-to-complete-a-task-and-start-a-new-one"></a>Proporcionar una manera fácil de completar una tarea e iniciar una nueva

El último obstáculo al que un usuario se enfrenta en una pantalla es determinar cuándo y cómo abandonar. Normalmente, el usuario deja la pantalla haciendo clic en un vínculo o ejecutando un comando que navega a otra pantalla. Estos vínculos pueden aparecer en el área de contenido de pantalla, en la lista de tareas o en las barras de herramientas de navegación. Los usuarios también pueden dejar una pantalla cerrando el archivo actual o la propia aplicación.

La tarea en algunas pantallas es preparar una operación que el usuario debe confirmar o cancelar. Estas pantallas suelen ofrecer un vínculo que realiza y confirma la operación, y otro vínculo que cancela. Si el usuario omite estas opciones y hace clic en otro vínculo, el programa debe realizar la opción menos destructiva. Las pantallas deben indicar lo que ocurrirá si el usuario toma esta ruta de acceso. Puede formular los vínculos para que resulten más obvios. Por ejemplo, un botón de confirmación con la etiqueta "Guardar cambios" implica que los cambios realizados en la pantalla no surtirán efecto hasta que se haga clic en ese botón.

Incluso si los usuarios pueden dejar de usar siempre que lo deseen, es posible que siga ofreciendo un vínculo que sugiera una salida obvia de la página. Lo mismo se aplica a las páginas que simplemente muestran información estática. Para obtener más información sobre este tema, consulte la sección [proporcionar una salida clara en la página](#provide-a-clear-exit-from-the-page).

### <a name="starting-and-completing-processes"></a>Inicio y finalización de procesos

Para los fines de este artículo, los procesos son técnicas para tratar con las tareas que llevan al usuario a más de una pantalla.

Supongamos que un usuario hace clic en un vínculo de la lista de tareas o el contenido de una pantalla y se lleva a otra pantalla. Esa página, a su vez, puede ser la primera de una serie de pantallas que realiza algunos resultados generales. Al final de esta serie de pantallas, el usuario desea volver a la pantalla que precedía al proceso. ¿Hay al menos dos maneras de que el usuario pueda volver? ¿hacer clic en el botón atrás repetidamente o volver a la Página principal y navegar desde ahí? pero ninguno de estos métodos es obvio o natural. La mayoría de los usuarios esperan encontrar un botón en la pantalla final que los devuelve directamente a la pantalla original.

El modelo IUI admite este escenario a través del concepto de un proceso, una pantalla o una serie de pantallas que se tratan como una unidad de navegación. Los usuarios pueden entrar en el proceso, trabajar en sus pantallas y, en la última pantalla, buscar un botón que los devuelva en el lugar donde se iniciaron. Lo importante es que el usuario puede iniciar el proceso desde varios lugares del producto. Los usuarios siempre se devuelven en el lugar donde se iniciaron, sin importar en qué momento empezaron a iniciar el proceso.

### <a name="process-name"></a>Nombre del proceso

Cada proceso debe recibir un nombre y el nombre debe aparecer en alguna parte de cada pantalla del proceso. Money 2000 usa este enfoque. Cada pantalla que forma parte de un proceso general incluye el nombre de ese proceso en la parte superior. Este nombre de proceso se muestra menos destacado que el título único de la pantalla porque es menos importante. El nombre del proceso recuerda a los usuarios qué proceso están llevando a cabo y refuerza la noción de que todas las pantallas del proceso forman parte de una sola característica. Por ejemplo, el área de **impuestos de dinero** incluye un proceso de **estimación de impuestos** que abarca varias pantallas. Cada pantalla de este proceso muestra el nombre del proceso colectivo y su título de pantalla único.

### <a name="implementation-of-processes"></a>Implementación de procesos

El mismo proceso se puede iniciar desde varios vínculos en diferentes pantallas y los usuarios siempre se devolverán a la página de inicio correcta. Este comportamiento no se puede lograr a través de un vínculo codificado de forma rígida en la última pantalla del proceso, ya que el destino del vínculo variará. En su lugar, la aplicación puede implementar este comportamiento manteniendo una pila de procesos activos, independientemente de la pila de navegación normal usada por los comandos **atrás** y **adelante** . Cuando el usuario inicia un proceso, la pantalla de inicio se inserta en la pila de procesos. Cuando el usuario hace clic en el botón **listo** en la pantalla final del proceso, la aplicación extrae la pantalla de inicio más reciente de la pila y devuelve el usuario a esa pantalla.

Cuando los usuarios navegan fuera de una pantalla en un proceso, el proceso permanece activo en la pila de procesos. Los usuarios pueden completar el proceso de copia de seguridad en la pantalla donde lo dejó y continuar. Esto permite a los usuarios realizar un desvío, realizar una copia de seguridad y, a continuación, continuar con el proceso. Para ver cómo funciona este comportamiento, inicie cualquier proceso de compra en línea en el World Wide Web, deje el sitio y, a continuación, presione el botón **atrás** . Por lo general, podrá seleccionar el lugar donde lo dejó.

### <a name="done-button"></a>Botón Listo

Para finalizar una pantalla y pasar a la siguiente pantalla del proceso, las pantallas pueden mostrar un botón cerca de la parte inferior de la página. La etiqueta de este botón es "siguiente", "listo" o algo similar. Si el botón finaliza el proceso y se puede llamar al proceso desde varias ubicaciones, el título del botón **listo** puede incluir el nombre de la ubicación de llamada.

### <a name="navigation-bar"></a>Barra de navegación

En cualquier pantalla, los usuarios pueden decidir que han terminado con el área actual del producto y desean iniciar otra cosa. Es posible que no deseen completar explícitamente la pantalla actual antes de pasar a otra parte del producto. Una barra de herramientas de navegación puede ofrecer al usuario un conjunto de vínculos para iniciar nuevas tareas. Al igual que con otras listas de vínculos de tareas, estos deben seguir el principio de hacer que el siguiente paso de navegación sea obvio, que se describe detalladamente en la sección siguiente.

### <a name="make-the-next-navigational-step-obvious"></a>Hacer obvio el siguiente paso de navegación

Pocos programas pueden hacer que todas sus características estén disponibles al mismo tiempo. Los usuarios generalmente deben navegar a través de un programa para encontrar una característica determinada. Los usuarios tienen más éxito en la navegación si pueden ver fácilmente cómo obtener al menos un paso más cerca del resultado deseado. Las pantallas que usan IUI están diseñadas pensando en este principio.

Por ejemplo, las páginas de actividad no muestran necesariamente cada tarea o destino imaginable que el usuario podría querer conseguir a partir de ese punto. En su lugar, las páginas de actividad proporcionan una lista de tareas que se completan lo suficiente para que los usuarios puedan determinar con facilidad el vínculo adecuado para hacer clic, incluso si solo las lleva a otra página de vínculos. Las tareas más frecuentes deben ser más destacadas y requieren la menor cantidad de navegación. Las tareas menos frecuentes pueden requerir más pasos.

A continuación se muestra un ejemplo de Money 2000. Supongamos que los usuarios quieren realizar una operación que solo realizan ocasionalmente, como la comprobación de la cantidad estimada del pago de impuestos de ingresos del año siguiente. Los usuarios primero inician la búsqueda de esta característica en la Página principal de Money 2000. Dado que la característica no aparece en la lista de tareas comunes, debe examinar la lista de áreas financieras. El área de **impuestos** suena en riesgo, por lo que hace clic en ella. La página **centro de impuestos** contiene un vínculo a la característica de estimación de impuestos que están buscando, por lo que hacen clic en ella y completan su tarea. Al aplicar los principios de IUI, Money 2000 permite a los usuarios encontrar de forma intuitiva lo que buscan.

## <a name="user-assistance"></a>Asistencia al usuario

En esta sección se describe un conjunto de directrices sugeridas para integrar el texto de ayuda del usuario en un producto que usa IUI.

La ayuda principal hace referencia a todo el texto que está visible en la pantalla (como se muestra en la siguiente captura de pantalla). La asistencia primaria proporciona indicaciones textuales centradas en las tareas para que los usuarios puedan comprender fácilmente toda la información que se presenta en la pantalla. Comprenden el propósito de la página y el modo en que los objetos se relacionan entre sí para ayudar a realizar tareas. Dado que el texto está directamente en la pantalla, la información que responde a preguntas inexpertas como "¿Qué debo hacer?" es fácil de acceder y muy visible sin que el usuario tenga que realizar ninguna acción.

![captura de pantalla de la pantalla de configuración de la cuenta de Money 2000.](images/iuiguidelines11.png)

La asistencia secundaria consiste en todo el texto que no está visible en la pantalla y requiere cierta interacción del usuario para acceder, como hacer clic o mantener el mouse sobre un elemento de la interfaz de usuario. Este contenido no es esencial para realizar la tarea a mano, pero todavía está directamente relacionado.

### <a name="primary-assistance"></a>Ayuda principal

La ayuda principal puede incluir algunos o todos los componentes siguientes:

-   Título de la pantalla

    Ejemplo: cambiar la imagen

    El título de la pantalla es el primer elemento y el más importante que aparece en la pantalla. Su finalidad es describir en el idioma del usuario la tarea que se puede completar en esta página. El título de la pantalla debe evitar describir los detalles de cómo completar la tarea. El texto del título de la pantalla solo debe hacer referencia a la tarea principal de la pantalla. Como regla general, cuanto más simple y más corta es la descripción de la tarea, mayor será la definición de la tarea. Para obtener información más detallada sobre este tema, vea el paso dos: [Estado de la tarea](#step-two-state-the-task).

-   Subtítulo de pantalla

    Ejemplo: también puede descargar una nueva imagen de Internet.

    Incluso con cuidado, es posible que el título de la pantalla no sea suficiente para explicar una tarea compleja de manera adecuada. El subtítulo le permite elaborar el propósito de la pantalla. Puede usar un subtítulo para ayudar a aclarar el propósito de la página, proporcionar una descripción de la tarea adicional o establecer las expectativas. Los usuarios que no lean el subtítulo deberían poder usar la página correctamente. Al igual que el título, el subtítulo debe evitar describir los detalles para completar la tarea.

-   Tareas

    Ejemplo: cambiar el protector de pantalla

    Las tareas se pueden presentar como vínculos de texto o imágenes gráficas que requieran la interacción del usuario. Los comandos que se presentan como vínculos de texto deben estar basados en verbos y escribirse como tareas claras y concisas.

-   Etiquetas para botones de comando

    Ejemplo: crear contraseña

    Hay tres tipos de botones de comando:

    -   Cancelar
    -   Listo
    -   Commit

    Los botones cancelar y listo simplemente usan "Cancelar" y "listo" como etiquetas. Los botones de confirmación deben usar etiquetas de texto activas en lugar de "Aceptar". Por ejemplo, use "Crear contraseña" en lugar de "Aceptar".

-   Etiquetas para otros controles

    Ejemplo: escriba la contraseña

    Las etiquetas de los controles, como botones de radio, casillas y cuadros de texto, deben escribirse de forma clara y concisa para que los usuarios sepan exactamente para qué sirven los controles, los que se deben usar y la información que se debe proporcionar para realizar su tarea.

-   Vínculos "tareas relacionadas"

    Ejemplo: tareas relacionadas: cambiar otra cuenta

    Los vínculos "tareas relacionadas" son puntos de entrada explícitos para otras tareas relacionadas con la característica actual. Deben escribirse como vínculos basados en tareas.

-   Vínculos "vea también"

    Ejemplo: vea también cambiar el tema.

    Los vínculos "vea también" son tareas secundarias. Están relacionados con la tarea principal, pero sacarán al usuario del contexto actual. Deberían aparecer como vínculos de tareas normales. Para obtener más información sobre las tareas secundarias, consulte [diseño visual de las tareas secundarias](#visual-design-of-secondary-tasks).

### <a name="secondary-assistance"></a>Asistencia secundaria

La asistencia secundaria puede incluir algunos o todos los componentes siguientes:

-   Recuadros informativos

    Puede usar un recuadro informativo para proporcionar al usuario información adicional sobre un vínculo de tarea o un botón de comando. Por ejemplo, un recuadro informativo de un vínculo de tarea podría ser "Mostrar una página donde puede seleccionar una imagen para usarla con su cuenta". El recuadro informativo aparece cuando el usuario mantiene el mouse sobre el objeto asociado. Debe crear recuadros informativos para todos los elementos de la interfaz de usuario en los que el usuario puede hacer clic.

-   Temas de ayuda "más información"

    Ejemplo: información acerca de la descarga de un archivo

    Los vínculos "más información" abren temas de ayuda, como información general sobre características, información conceptual, información complementaria e información de procedimientos. Para reducir la aglomeración, debe minimizar el número de temas de ayuda de "información acerca de" en la pantalla.

## <a name="appendix-designing-and-testing-microsoft-money-2000"></a>Apéndice: diseño y prueba de Microsoft Money 2000

Esta sección se ha adaptado a las descripciones de primera mano de los diseñadores. Describe cómo el equipo de Money 2000 modificó el proceso de diseño y pruebas para acomodar el modelo IUI.

### <a name="designing-and-testing-money-2000"></a>Diseño y prueba de Money 2000

El diseño de Money 2000 con el modelo de navegación inducto condujo al equipo a los diseños que han estado en el producto durante mucho tiempo. Dado que los principios del modelo son sencillos, era fácil adoptar el modelo en el proceso de diseño y permanecer con él. Al final, los diseñadores consideran que el modelo les ayudó a tomar mejores diseños de los que podían haber generado sin él.

### <a name="clearer-titles-and-designs"></a>Títulos y diseños más claros

Los diseñadores de Money 2000 han observado que, a menudo, describen características con palabras que realmente no aparecían en la pantalla. En el modelo IUI, las pantallas deben explicarse a sí mismas. Por ejemplo, el equipo explicó que la pantalla con la etiqueta **calendario de pago** estaba pensada para pagar facturas. En Money 2000, esa pantalla se denomina **pagar facturas**. Todos los elementos que no están relacionados con ese propósito se han pasado a las pantallas subsidiarias, lo que da lugar a un diseño más claro.

Otro ejemplo implica una pantalla denominada **Administrador de servicios financieros en línea**. El equipo ha tenido problemas para obtener una explicación sencilla del propósito de esta pantalla. Cuando no pudieron llegar a uno, quitaron esta pantalla y distribuyeban sus características entre más páginas definidas lógicamente.

### <a name="helping-new-designers"></a>Ayudar a los nuevos diseñadores

El equipo ha descubierto que es fácil enseñar las técnicas de diseño de IUI a los nuevos diseñadores de software inmejorados. Las técnicas permiten a los diseñadores de todos los niveles de experiencia evaluar sus diseños usando títulos de pantalla como prueba de claridad. Cuando se fuerza a poner un título claro y conciso en una pantalla mal diseñada, los diseñadores reconocen rápidamente que ningún título era lo suficientemente bueno para la página. Se ha dado cuenta de que el problema no se basó en elegir palabras para un título, sino en un diseño de pantalla con errores. Con este conocimiento, podrían volver a diseñar la pantalla para admitir una interacción del usuario más clara y, por lo tanto, un título más claro.

### <a name="including-writers"></a>Inclusión de escritores

A medida que progresa el diseño, el equipo ha dado cuenta de que los escritores y editores de documentación deben participar en la creación de títulos de pantalla. Los escritores estaban limitados en su capacidad para elegir buenos títulos en versiones anteriores porque solo estaban implicados en una fase de tiempo de ejecución. Normalmente, los diseñadores o programadores han dado puestos de trabajo temporales a las pantallas. Estos títulos se usaron hasta el final del ciclo del producto cuando se pidió a los escritores que se encontraran con los títulos finales de la pantalla. En ese momento, era demasiado tarde para cambiar las pantallas de diseño deficiente.

Por el contrario, el equipo de Money 2000 participa en las primeras fases del proceso de diseño. Esto contrajo una valiosa entrada en los títulos de pantalla cuando podría servir de ayuda para el diseño. Si una pantalla es demasiado compleja para permitir un título claro, los escritores podrían sugerir que se Rediseñe la página.

Al final del proyecto, los escritores y diseñadores creían que los títulos de pantalla eran más claros y más seguros que en las versiones anteriores. Los escritores también han descubierto que es más fácil explicar las nuevas páginas, por lo que el trabajo de documentar el producto es más sencillo. Todos los miembros del equipo pensaban que, en la fase de diseño, el producto era mejor y más fácil de usar.

### <a name="usability-tests"></a>Pruebas de facilidad de uso

Al desarrollar Money 2000, el equipo llevó a cabo varias pruebas de facilidad de uso para ver las diferencias entre la antigua estructura de navegación de Money 99 y los cambios que se realizaron como resultado de aplicar el modelo IUI.

### <a name="prototype-testing"></a>Pruebas de prototipos

En las primeras fases del proceso de desarrollo del producto, los diseñadores crearon un prototipo para explorar cómo los usuarios reaccionarían a IUI. Este trabajo se realizaba muy pronto en el proceso de desarrollo para permitir el tiempo necesario para refinar los principios del modelo antes de que los programadores comenzaran a recurrir al producto.

El equipo creó un prototipo en Microsoft Visual Basic y HTML que simulaba actividades financieras personales que normalmente se realizaban en Money. En el prototipo, los usuarios pueden navegar a más de 50 páginas que representan las áreas principales del producto. En estas áreas, pueden configurar cuentas financieras, pagar facturas, ver informes y trabajar con sus inversiones.

Once participantes realizaron el mismo conjunto de tareas tanto en Money 99 como en el prototipo IUI. Se asignaron aleatoriamente para usar uno de los productos en primer lugar. Cuatro participantes eran usuarios actuales de Money, cuatro eran usuarios actuales de un producto competidor y tres no usaban nunca un producto financiero personal antes.

Las preferencias generales indican que los cuatro usuarios actuales de Money prefieren Money 99 (la versión que habían usado en casa) mientras que los siete usuarios restantes prefieren el nuevo prototipo a la versión actual. Para todas las demás medidas, no había ninguna diferencia entre los usuarios de los tres grupos. En lo que se refiere al rendimiento general, los usuarios se encontraban en el área equivocada del producto dos veces 2,82 99 como en el prototipo (1,45 veces por tarea). Otros datos de preferencias y medidas de rendimiento, aunque no son significativos, aparecían para favorecer el prototipo. En función de estos datos y otras pruebas, el equipo del producto de Money decidió incorporar los principios de IUI en Money 2000.

### <a name="product-testing"></a>Pruebas de productos

Una vez completada la mayoría del código del producto, el equipo realizó otro estudio de uso para examinar la implementación final de IUI. En esta prueba, se seleccionaron 10 participantes que nunca usaban un producto financiero personal antes de usar Money 99 o Money 2000. Todos los usuarios realizaron las mismas tareas.

Los usuarios de Money 2000 han completado correctamente el 89% de las tareas, mientras que los usuarios de Money 99 han completado correctamente solo el 74% de las tareas. Al igual que con el prototipo, los usuarios también parecían ser más rápidos, pero no muy diferentes, al navegar en Money 2000 en comparación con Money 99. Además, las medidas generales de satisfacción subjetiva de la navegación también solían ser mayores para Money 2000 que para Money 99.

### <a name="controlled-testing"></a>Pruebas controladas

Dado que Money 2000 es enorme y complejo, no es adecuado para llevar a cabo experimentos controlados sobre los efectos de aplicar IUI. En su lugar, el equipo creó un entorno más restringido para la prueba.

La prueba contenía una aplicación "Visor de mercado de acciones" que permitía a los usuarios modificar la presentación de un informe de mercado de existencias que se muestra en la pantalla. Los usuarios pueden cambiar las columnas de datos que se incluyeron en el informe, el orden de las columnas del informe, su alineación y el número de posiciones decimales utilizadas. Los diseñadores quieren ver cómo realizaría un enfoque IUI en esta tarea en comparación con una interfaz gráfica de usuario convencional.

En la captura de pantalla siguiente se muestra la interfaz de usuario convencional que se usa en la prueba. Un único cuadro de diálogo realiza todas las tareas de personalización de informes. Muchas aplicaciones proporcionan un cuadro de diálogo similar para seleccionar un subconjunto de una lista de elementos. El cuadro de diálogo contiene dos listas: en la lista de la izquierda se muestran todas las columnas disponibles del informe y la derecha muestra el subconjunto de columnas que el usuario ha seleccionado para el informe. Los controles adicionales modifican los atributos de formato y orden de las columnas de informe seleccionadas en la lista de la derecha.

![captura de pantalla de un cuadro de diálogo convencional.](images/iuiguidelines12.png)

Para la versión IUI de esta tarea, el equipo creó una aplicación de estilo Web. Cada tarea de personalización se colocó en una página independiente. La aplicación también incluía una página principal, que se muestra en la siguiente captura de pantalla, que pide a los usuarios cómo quieren personalizar el informe.

![captura de pantalla de una pantalla de prueba de IUI.](images/iuiguidelines13.png)

Al hacer clic en los vínculos de esta página principal, el usuario toma las páginas adicionales para realizar tareas de personalización específicas. Por ejemplo, en la siguiente captura de pantalla se muestra la página que se usa para seleccionar las columnas del informe.

![captura de pantalla de una pantalla de prueba de IUI para seleccionar las columnas del informe.](images/iuiguidelines14.png)

En las pruebas de ambas versiones, se pidió a los temas que personalizaran informes desde un estado de inicio determinado (que se muestra en la pantalla) a un estado de objetivo especificado (se muestra en un documento de papel). El equipo realizó un seguimiento de la cantidad de tiempo y el número de intentos realizados para personalizar el informe. El equipo informaba a los usuarios cuando habían personalizado el informe correctamente.

La prueba incluía 88 participantes. Se pidió a cada participante que personalizara un conjunto de 11 informes con una de las dos versiones de la aplicación. Además, 72 de estos participantes devolvieron una semana después para personalizar otro conjunto de 11 informes con la misma versión de la primera sesión. Cada asunto se clasificó como un usuario de equipo inexperto, principalmente usando el equipo para el correo electrónico, jugando al solitario y navegando por Internet.

No hubo diferencias significativas entre los usuarios de las dos versiones o cualquiera de las otras variables de interés. Los usuarios realizan tareas a la misma velocidad, se recorren en iteración en la tarea el mismo número de veces y tenían las mismas valoraciones generales de satisfacción subjetiva para las dos versiones. Por lo tanto, esta prueba no pudo mostrar ninguna medida en la que IUI haya dado lugar a una mejora o degradación en el rendimiento o en las clasificaciones subjetivas.

Podría argumentarse que si el usuario tiene que navegar más para realizar la tarea, la cantidad de tiempo para realizar la tarea debe ser mayor. Aunque este experimento no sugiere este resultado, es importante tener en cuenta que los tiempos de rendimiento medio y sus desviaciones estándar asociadas para los dos enfoques diferentes para esta tarea eran casi idénticos.

Será necesario realizar más investigaciones para determinar si se han realizado mejoras mensurables del uso de IUI. Como mínimo, esta prueba no proporcionó ninguna evidencia de que IUI dañe el rendimiento o el uso del producto.

### <a name="comparison-with-web-sites"></a>Comparación con sitios web

Muchos sitios web bien diseñados usan principios similares al modelo IUI que se describe en este documento. Este es probablemente un efecto secundario de la forma en que funciona la Web. Dado que es difícil implementar interacciones complejas entre los controles en una sola página web, los diseñadores suelen dividir las tareas en partes que implican más de un viaje al servidor para obtener una nueva página. Algunos sitios incluso incluyen títulos de página que indican claramente el propósito de la página.

Los diseñadores de aplicaciones tradicionales tienen un conjunto mucho más completo de herramientas disponibles. Esto proporciona más flexibilidad, pero también proporciona más oportunidades para crear páginas complejas y confusas. Al crear interfaces de usuario innecesarias, los diseñadores deben usar esta capacidad con prudencia y recordar la claridad y la simplicidad del valor.

 

 





