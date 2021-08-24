---
title: Ineducción Interfaz de usuario
description: En este tema se describe el modelo de interfaz de usuario conocido como interfaz de usuario inerte (IUI).
ms.assetid: d99dc30a-68e5-4b7a-8cbd-0ac77a90a354
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a16282248e1942070f5dc3e1418016657de2e84f39e1f8473eaedcbc0eeccbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589424"
---
# <a name="inductive-user-interface"></a>Ineducción Interfaz de usuario

En este tema se describe el modelo de interfaz de usuario conocido como interfaz de usuario inerte (IUI). También denominado navegación inerte, el modelo de IUI sugiere cómo hacer que las aplicaciones de software sean más sencillas mediante la separación de características en pantallas o páginas que son fáciles de explicar y comprender. Este modelo de IUI es evidente en varios proyectos de Microsoft, como Microsoft Money 2000, los applets del panel de control de Windows, varias pantallas y diálogos de Microsoft Visual Studio 2010 y los paneles de tareas de Microsoft Office.

-   [Introducción](#introduction)
-   [IUI in Action: Solving a Common Design Problem](#iui-in-action-solving-a-common-design-problem)
    -   [El problema: el software es difícil de usar](#the-problem-software-is-hard-to-use)
    -   [Interfaz de usuario de deserción](#deductive-user-interface)
    -   [Una solución: Interfaz de usuario](#a-solution-inductive-user-interface)
-   [Pasos para crear un Interfaz de usuario](#steps-for-creating-an-inductive-user-interface)
    -   [Paso uno: Centrar cada página en una sola tarea](#step-one-focus-each-page-on-a-single-task)
    -   [Paso dos: Estado de la tarea](#step-two-state-the-task)
    -   [Paso tres: Hacer que el contenido de la página se adapte a la tarea](#step-three-make-the-pages-contents-suit-the-task)
    -   [Paso cuatro: Ofrecer vínculos a tareas secundarias](#step-four-offer-links-to-secondary-tasks)
-   [Directrices adicionales](#additional-guidelines)
    -   [Uso de plantillas de pantalla coherentes](#use-consistent-screen-templates)
    -   [Hacer evidente cómo llevar a cabo la tarea con los controles en la pantalla](#make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen)
    -   [Proporcionar una manera sencilla de completar una tarea e iniciar una nueva](#provide-screens-for-starting-tasks)
    -   [Hacer que el siguiente paso de navegación sea obvio](#make-the-next-navigational-step-obvious)
-   [Asistencia al usuario](#user-assistance)
    -   [Asistencia principal](#primary-assistance)
    -   [Asistencia secundaria](#secondary-assistance)
-   [Apéndice: Diseño y prueba de Microsoft Money 2000](#appendix-designing-and-testing-microsoft-money-2000)
    -   [Diseño y prueba de Money 2000](#designing-and-testing-money-2000)
    -   [Pruebas de facilidad de uso](#usability-tests)
    -   [Comparación con sitios web](#comparison-with-web-sites)

## <a name="introduction"></a>Introducción

IUI es un modelo de interfaz de usuario que sugiere cómo hacer que las aplicaciones de software sean más sencillas mediante la separación de características en pantallas o páginas que son fáciles de explicar y comprender. Microsoft ha implementado este modelo en Money 2000, una aplicación de software comercial de gran tamaño. Las pruebas informales sugieren que los usuarios pueden realizar tareas tan rápidamente en este modelo como en las interfaces tradicionales y pueden encontrar las cosas más fácilmente.

Muchas aplicaciones de software comercial incluyen interfaces de usuario en las que una pantalla presenta un conjunto de controles, pero deja al usuario deducir el propósito de la página y cómo usar los controles para lograr ese propósito.

Los principios descritos en este documento no requieren ni implican ningún conjunto estricto concreto de diseños, controles o elementos visuales. Al igual que las interfaces gráficas de usuario en general, los principios de este documento dejan mucho espacio para la flexibilidad y la creatividad en el diseño.

Los principios generales de la interfaz de usuario inerte se muestran con ejemplos extraídos de Money 2000.

> [!IMPORTANT]
> El concepto general de IUI está en su inactividad. Los diseñadores que emplean estas técnicas están aprendiendo y desciendo más información al respecto a medida que lo usan para su software. La información de este documento evolucionará con el tiempo a medida que aumente la investigación y el conocimiento en esta área. En este tema se proporciona una introducción a la IUI, en lugar de un conjunto completo de directrices.

 

## <a name="iui-in-action-solving-a-common-design-problem"></a>IUI in Action: Solving a Common Design Problem

En esta sección se describe un problema de diseño común con los productos de software actuales y se presenta IUI como una técnica para superar el problema.

### <a name="the-problem-software-is-hard-to-use"></a>El problema: el software es difícil de usar

La mayoría del software es demasiado difícil de usar. Esta conclusión se extrae de las pruebas de facilidad de uso, la evidencia anecdética y las experiencias personales de los diseñadores de software. El concepto de IUI se creó mediante la realización de investigaciones, la realización de conjeturas sobre lo que dificulta el uso del software actual y, a continuación, la propuesta de soluciones. Los diseñadores que usan IUI deben basarse en la satisfacción del cliente para determinar el éxito final del diseño.

La mayoría de los productos de software actuales son difíciles de usar por las siguientes razones generales:

-   Los usuarios no parecen construir un modelo mental adecuado del producto.

    El diseño de la interfaz de la mayoría de los productos de software actuales supone que los usuarios comprenderán un modelo conceptual que los diseñadores diseñaron cuidadosamente. Desafortunadamente, la mayoría de los usuarios no parecen adquirir nunca un modelo mental que sea lo suficientemente preciso como para guiar su navegación. Es probable que estos usuarios estén muy ocupados y sobrecargados con información. No tienen el tiempo, la energía o el deseo de estudiar un modelo conceptual para su software.

-   Incluso muchos usuarios de larga duración nunca maestron procedimientos comunes.

    Los diseñadores saben que los nuevos usuarios pueden tener problemas al principio, pero esperan que estos problemas desaparezcan a medida que los usuarios aprenden tareas comunes. Los datos de facilidad de uso indican que esto a menudo no sucede. En un estudio, los investigadores configuraron equipos automatizados para grabar a los usuarios en casa. Las cintas mostraron que los usuarios que se centran en la tarea en la mano no necesariamente observan el procedimiento que están siguiendo y no aprenden de la experiencia. La próxima vez que los usuarios realicen la misma operación, pueden atravesarla exactamente de la misma manera.

-   Los usuarios deben trabajar duro para averiguar cada característica o pantalla.

    La mayoría de los productos de software están diseñados para (los pocos) usuarios que comprenden su modelo conceptual y tienen procedimientos comunes maestros. Para la mayoría de los clientes, cada característica o procedimiento es un efecto frustrante y no deseado. Los usuarios pueden suponer que estos problemas suponen un costo inevitable de usar equipos, pero sin duda serían insoportables sin esta carga.

La mejor solución a estos problemas es encontrar una estrategia general para hacer que las características de los productos de software sea más evidente y explicativa. Los usuarios deben poder encontrar una característica cada vez que la necesiten y deben poder usar esa característica cada vez que quieran usarla.

### <a name="deductive-user-interface"></a>Interfaz de usuario de deserción

En la actualidad, la mayoría de los elementos del software requieren que el usuario los estudie y deduzca su comportamiento, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de un cuadro de diálogo de propiedades de ejemplo.](images/iuiguidelines01.png)

Los usuarios de equipos experimentados, incluidos los diseñadores de software, reconocen rápidamente que este cuadro de diálogo les permite administrar una lista de cosas. Comprenden los botones que aparecen debajo de la lista pueden agregar, quitar y proporcionar información sobre los elementos de lista. Sin embargo, tenga en cuenta que ninguno de estos comportamientos se indica explícitamente en el propio cuadro de diálogo.

Ahora, echa otro vistazo al cuadro de diálogo desde el punto de vista de un usuario ocasional. Muchos usuarios, cuando se enfrentan a este cuadro de diálogo, preguntarán"¿ Qué debo hacer con esto?" Cuando aparezca el cuadro de diálogo, el usuario debe detenerse y averiguar qué hacer a continuación. En primer lugar, el usuario debe deducir el hecho de que el rectángulo blanco grande es un cuadro de lista vacío que se va a rellenar con elementos. La etiqueta de texto pequeña del cuadro, "Things", ofrece una sugerencia imprecisa. Algunos usuarios intentarían escribir en el cuadro de lista, porque parece un cuadro de texto de edición.

A continuación, el usuario debe deducir que los botones situados debajo de la lista afectan a su contenido. Algunos de los botones están deshabilitados inicialmente, lo que es otra posible fuente de confusión del usuario. El usuario debe experimentar con los controles para obtener información sobre cómo funciona el cuadro de diálogo.

El usuario también podría hacer otras preguntas: "¿Cuántos elementos debo incluir en la lista? ¿Debo escribir elementos en un orden específico? ¿Por qué he tenido este cuadro de diálogo en primer lugar? ¿Para qué es esto?"

Los usuarios se distraen de sus objetivos cada vez que deben averiguar el propósito de una pantalla y cómo usarla. En última instancia, esto representa un costo en el tiempo y la satisfacción del usuario. Peor aún, los usuarios pagan este costo una y otra vez a medida que se desconcierte sobre la interfaz cada vez que usan una característica.

Una pantalla debe tener un título que explique claramente su propósito. Cuando los diseñadores crean una pantalla, rara vez la necesitan para tener un propósito claramente expresable. En su lugar, puede formar parte de un modelo conceptual mayor que el usuario debe deducir.

Los estudios muestran que muchos usuarios están confusos incluso por las operaciones básicas en el software. Tienen dificultades para comprender lo que el producto puede hacer por ellos, dónde ir para realizar una operación y cómo realizar esa operación una vez que la han encontrado. Simplificar el software mediante la realización de cambios fundamentales es una manera eficaz de satisfacer mejor a los clientes existentes y atraer a nuevos usuarios.

### <a name="a-solution-inductive-user-interface"></a>Una solución: Interfaz de usuario

Como nueva forma de diseñar software, el objetivo de IUI es reducir la cantidad de ideas extraneosas que los usuarios deben hacer para moverse correctamente entre partes de un producto y usar sus características. La palabra ineducción procede del verbo induce, lo que significa dirigir o moverse por influencia o persuasión.

IUI es una extensión de la interfaz de estilo web común. En el entorno web, las páginas deben ser sencillas y basadas en tareas, ya que cada parte de la información debe enviarse a un servidor a través de una conexión relativamente lenta. A continuación, el servidor responde con el paso siguiente, y así sucesivamente. Un buen diseño web significa centrarse en una sola tarea por página y proporcionar navegación por las páginas. De forma similar, la navegación inductiva comienza por centrar la actividad de cada página en una sola tarea principal.

Una interfaz inductiva bien diseñada ayuda a los usuarios a responder a dos preguntas fundamentales a las que se enfrentan al mirar una pantalla:

-   ¿Qué debo hacer ahora?
-   ¿Dónde puedo ir desde aquí para realizar mi siguiente tarea?

El software diseñado según estos principios responde a estas preguntas empezando por una idea fundamental: una pantalla con un único propósito explícito y claramente indicado es más fácil de entender que una página sin este propósito. Si la pantalla es más fácil de entender, será más fácil para el usuario saber qué hacer y dónde ir a continuación.

Esta local fundamental se puede expandir en una serie de cuatro pasos para diseñar software que usa IUI:

-   Centre cada pantalla en una sola tarea.
-   Estado de la tarea.
-   Haga que el contenido de la pantalla se ajuste a la tarea.
-   Ofrezca vínculos a tareas secundarias.

Aunque en este documento se describen los principios generales de IUI, también se muestran esos principios en acción mostrando ejemplos de Money 2000 y otro software. Debe considerar estos ejemplos como expresiones concretas de IUI, no como un modelo estricto para la implementación.

Además de los cuatro pasos mencionados anteriormente, puede reforzar la interfaz siguiendo estas cinco directrices:

-   Use plantillas de pantalla coherentes.
-   Proporcione pantallas para iniciar tareas.
-   Haga que sea obvio cómo llevar a cabo la tarea con los controles en la pantalla.
-   Proporcione una manera sencilla de completar una tarea e iniciar una nueva.
-   Haga que el siguiente paso de navegación sea obvio.

### <a name="processes"></a>Procesos

Muchas tareas requieren que los usuarios naveguen por una serie de pantallas. Un usuario que realiza una tarea puede hacer clic en un vínculo a una tarea secundaria que se aleja de la secuencia de pantallas que la forma parte de la tarea principal. Cuando el usuario complete la tarea secundaria, debería haber una manera sencilla de devolver el usuario directamente al punto de bifurcación de la tarea original. Es probable que los usuarios tengan problemas  con el uso de controles de navegación convencionales, como los botones **Atrás** y Adelante, para volver a donde empezaron.

Para proporcionar esta capacidad, IUI define un concepto de navegación denominado proceso, una pantalla o una serie de pantallas que realizan una tarea. Un proceso actúa como una especie de subrutina de navegación. Los usuarios pueden comenzar un proceso, trabajar a través de su serie de pantallas y, a continuación, en la última página, hacer clic en un botón "Listo" para volver rápidamente a la página donde empezaron el proceso.

## <a name="steps-for-creating-an-inductive-user-interface"></a>Pasos para crear un Interfaz de usuario

En esta sección se describen en profundidad los cuatro pasos que puede usar para crear una IUI.

### <a name="step-one-focus-each-page-on-a-single-task"></a>Paso uno: Centrar cada página en una sola tarea

El primer paso para diseñar una IUI es tomar una característica o un conjunto de características y dividirla en pantallas independientes. Cada pantalla debe centrarse en una sola tarea, denominada tarea principal de la pantalla.

Esta idea suena sencilla, pero pocas aplicaciones la siguen. La mayoría de las aplicaciones presentan una pantalla desde la que se logran todas las características relacionadas. Este diseño requiere que los usuarios puedan averiguar (deducir) lo que se puede hacer y cómo hacerlo.

La tarea principal puede ser específica o abierta. Por ejemplo, en un programa de finanzas personales, una tarea específica podría ser "Seleccionar la factura que desea pagar", mientras que una tarea abierta podría ser "Revisar el rendimiento de las inversiones".

La tarea principal debe ser algo que tenga sentido para el usuario, en lugar de un reflejo de un detalle de implementación u otro concepto abstracto. La tarea debe ser algo que los usuarios puedan pensar hacer, preferiblemente descrito en sus propias palabras.

### <a name="example"></a>Ejemplo

En esta sección se comparan dos versiones diferentes de Money. En los ejemplos se muestran características muy similares que permiten a los usuarios ver y administrar cuentas financieras.

El modelo de IUI se desarrolló durante la creación de Money 2000, una aplicación para administrar las finanzas personales. Money 2000 es la octavo versión principal del producto. Money 2000 es un programa Windows con más de un millón de líneas de código.

Money 2000 es una aplicación de estilo web. No es un sitio web, pero comparte muchos atributos con sitios web. Su interfaz de usuario consta de páginas de pantalla completa que se muestran en un marco compartido, con herramientas para moverse hacia atrás y hacia delante a través de una pila de navegación. En esta base, Money 2000 agrega un conjunto de nuevas convenciones de interfaz de usuario que crean una experiencia de usuario más estructurada.

Aunque IUI se usó por primera vez en el diseño de estilo web de Money 2000, también se puede usar con elementos de interfaz tradicionales, como ventanas y cuadros de diálogo.

En Money 99, los usuarios a menudo realizan una gran variedad de tareas en una sola pantalla. Por ejemplo, en la siguiente captura de pantalla se muestra **el** Administrador de cuentas que presenta todas las características relacionadas con la cuenta de Money 99 en una sola pantalla.

![captura de pantalla del administrador de cuentas en dinero 99.](images/iuiguidelines02.png)

Esta pantalla agrupa una tarea común, navegando a una cuenta, así como tareas poco frecuentes, como la creación y eliminación de cuentas. Ninguna de estas tareas específicas se expresa directamente en el título de la pantalla, **Account Manager**. Muchos usuarios pueden encontrar esta pantalla tan complicada como el cuadro de diálogo de ejemplo de la figura 1. En ambos casos, el usuario debe deducir el propósito de la pantalla y cómo usarlo.

Money 2000, que sigue a IUI, ofrece un conjunto casi idéntico de características relacionadas con la cuenta, pero las proporciona en dos pantallas independientes. En la captura de pantalla siguiente se muestra la primera de estas pantallas, que se centra completamente en que el usuario elija una cuenta.

![captura de pantalla de la pantalla de selección de cuenta en money 2000.](images/iuiguidelines03.png)

La pantalla Money 2000 contiene aproximadamente el mismo número de elementos visuales que la pantalla money 99 anterior, pero la página ahora se centra completamente en que el usuario elija una cuenta. Por ejemplo, en la versión Money 99, un usuario tenía que hacer dos clics para abrir una cuenta: una para seleccionarla y otra para seleccionar la operación de apertura. En la versión Money 2000, la única razón por la que un usuario hace clic en una cuenta es abrirla, por lo que un solo clic puede ser suficiente. De este modo, aunque el número de pantallas pueda aumentar, el número de clics necesarios para realizar una tarea común a menudo se reduce.

En ocasiones, los usuarios querrán agregar o quitar una cuenta. Para realizar esta tarea en Money 2000, los usuarios navegan a una segunda pantalla (que se muestra en la siguiente captura de pantalla) que se centra en la configuración de cuentas.

![captura de pantalla de la pantalla de configuración de la cuenta en money 2000.](images/iuiguidelines04.png)

El propósito de cada pantalla es más claro en la versión de IUI de Money 2000. Además, cada pantalla tiene más espacio para dedicarse a cumplir su propósito. Por ejemplo, el administrador de cuentas money 99 podría dar muy poco espacio al botón Eliminar cuenta, porque rara vez se usó en comparación con los otros comandos de la pantalla.   Por el contrario, la pantalla de configuración de la cuenta de Money 2000 puede tener este comando de forma más destacada, lo que lo hace más reconocible y explicativo.

### <a name="what-is-a-single-task"></a>¿Qué es una sola tarea?

¿Cómo sabe si una pantalla está realmente centrada en una sola tarea? Una pantalla que admite muchas tareas podría explicarse como que solo tiene un propósito si ese propósito es suficientemente abstracto. Esta es una regla general: una pantalla se centra en un propósito si el diseñador puede expresar ese propósito con un título de pantalla conciso, significativo y natural.

Los diseñadores de Money 2000 consideraron dividir estas pantallas **(elegir** una cuenta para usar y configurar las cuentas en **Money)** en más pantallas. Sin embargo, dado que cada pantalla ya tiene un título conciso, significativo y natural, los diseñadores creen que las pantallas estaban lo suficientemente centradas. Al diseñar una pantalla, si no puede pensar en un título claro y sencillo, probablemente esté intentando realizar demasiado en la pantalla.

### <a name="step-two-state-the-task"></a>Paso dos: Estado de la tarea

Cada pantalla debe estar titulada con una instrucción concisa y explícita de su tarea principal. Puede ser una instrucción directa ("Seleccione la cuenta que desea equilibrar") o una pregunta que desea que el usuario responda ("¿Qué cuenta desea equilibrar?").

Este es otro principio de sonido simple que a menudo no se practicará. Por ejemplo, las versiones anteriores de Money tenían pantallas con títulos como **Online Financial Services Manager** y Balance **Account**. Los usuarios tenían que deducir el propósito y el comportamiento de estas pantallas de la organización y las etiquetas de sus controles.

El título de la pantalla o página es muy importante. Si el producto usa ventanas, páginas de estilo web, cuadros de diálogo u otro diseño, no se debe permitir que el título se desplace hacia fuera.

### <a name="usable-screens-have-clear-titles"></a>Las pantallas utilizables tienen títulos claros

Las pantallas que realizan muchas tareas requieren títulos abstractos o complejos. Por ejemplo, la pantalla Money 99 que se muestra en la figura 2 permitía al usuario navegar a las cuentas y configurar las cuentas. El título abstracto "Administrador de cuentas" se ha dado a esta página en un intento de capturar ambos propósitos. Aunque los usuarios pueden tener algunas ideas sobre lo que podría hacer una página de "Administrador de cuentas", es posible que no se den cuenta de que la tarea más común para esta pantalla era simplemente elegir una cuenta.

Algunas pantallas o comandos tienen fines abstractos que no sugieren fácilmente títulos claros. Para estas pantallas, los diseñadores pueden elegir nombres deliberadamente imprecisos, como "Configuración;", palabras de timbre acuñadas, como "QuickStep;" o jerga que revela los detalles de implementación ("Compactación de base de datos"). Estos tipos de nombres suelen ser confusos o engañosos para los usuarios. Además, estos nombres suelen ser sustantivos que no expresan la acción que el usuario quiere realizar, lo que aumenta la confusión.

Los títulos de pantalla y otros nombres a menudo no se determinan hasta casi el final del proceso de diseño. A menudo, los diseñadores piden a los escritores que se les asigne un nombre adecuado para una pantalla después de que se haya diseñado y codificado. En ese momento, no hay ningún recurso si no se encuentra un buen nombre, por lo que es posible que el equipo tenga que resolver los nombres que no están claros. La solución a este error es que los diseñadores piensen en la claridad en las funciones de pantalla y los títulos al principio del proceso de diseño.

Las funciones de pantalla y los títulos deben centrarse en las tareas más comunes que realizan los clientes. Los diseñadores suelen tener la tentación de proporcionar enormes cantidades de funcionalidad en un intento de satisfacer el mayor número de clientes, junto con los deseo del propio equipo de diseño. Sin embargo, las características adicionales siempre agregan complejidad y otros costos.

### <a name="screen-title-indicates-design-clarity"></a>El título de la pantalla indica claridad de diseño

En el modelo de IUI, los diseñadores eligen los títulos de pantalla en las primeras fases del proceso de diseño. En lugar de elegir un título para justificar el funcionamiento de la pantalla, se usa para determinar si la pantalla tiene sentido. Si no se encuentra ningún título adecuado, se rediseña la característica. Si ningún diseño permite un título claro y conciso (es decir, si no hay ninguna manera de explicar la característica), los diseñadores podrían abandonar la característica. En las capturas de pantalla siguientes, compare la pantalla de pago de factura Money 99 de la izquierda, que proporciona una etiqueta estática para la página ("Facturas próximas & Depósitos") y la pantalla Money 2000 correspondiente a la derecha, que tiene un título explícito ("Haga clic en la factura que le gustaría pagar"):

![captura de pantalla que muestra un título estático en money 99 y un título activo en money 2000.](images/iuiguidelines05.png)

Un título de pantalla, que por supuesto es simplemente una frase o frase, es más fácil de cambiar que un diseño o código. A pesar de este hecho, la experiencia con IUI ha demostrado que la mente en un título de pantalla clara al principio genera mejores diseños. Los títulos deben elegirse con la entrada de los miembros del equipo de educación y facilidad de uso del usuario, así como de los diseñadores de productos.

A veces, los miembros del equipo pueden intentar posponer esta decisión, suponiendo que los clientes compartan su comprensión del propósito de una pantalla. Sin embargo, cuando se fuerza a ofrecer una declaración clara y concisa de este propósito, a menudo se revelan diferencias de opinión. Al resolver estas diferencias y elegir un título al principio, las discusiones de diseño pueden continuar más sin problemas.

Una vez elegido un título, no debe considerarlo inmutable. Es probable que los diseñadores refinen los títulos de pantalla con el tiempo, como con cualquier diseño. Sin embargo, el primer título elegido debe ser tan fuerte como sea posible en esa fase de desarrollo.

### <a name="guidelines-for-choosing-screen-titles&quot;></a>Directrices para elegir títulos de pantalla

En esta sección se describe una técnica sencilla para elegir buenos títulos de pantalla. Para usar esta técnica, los diseñadores se imaginan a un amigo que pregunta: &quot;¿Para qué es esta pantalla?&quot; y, a continuación, se ofrece una respuesta clara y útil que completa la frase &quot;Esta es la pantalla donde se encuentra?&quot;. Las palabras que completan la frase se convierten en el título de la pantalla.

Durante el desarrollo de Money 2000, los escritores de documentación del equipo crearon directrices de título de pantalla para garantizar la calidad y la coherencia. Por ejemplo, estas directrices sugieren títulos que usaban verbos y se frases como preguntas o instrucciones directas. Los diseñadores evitaron nombres estáticos que permitían más abstracción y podrían ser imprecisos.

Para simplificar los títulos, los diseñadores evitaron las oraciones compuestas e intentaron usar el lenguaje conversacional, evitando términos y jerga difíciles. Si los diseñadores no pueden describir la tarea sin recurrir a las conjunciones (&quot;and&quot;, &quot;or"), la pantalla probablemente está intentando realizar más de una tarea y es menos probable que el usuario pueda comprender inmediatamente qué hacer.

Incluso cuando se elige cuidadosamente un título, la región del título puede ser demasiado pequeña para explicar adecuadamente una tarea compleja. Para mitigar este problema, puede incluir un breve párrafo descriptivo en la parte superior del área de contenido de la pantalla que se elabora en la tarea.

La tabla siguiente contiene algunos ejemplos de títulos de pantalla en Money 99 y títulos para la misma pantalla o pantallas relacionadas en Money 2000.



| Títulos de pantalla en Money 99             | Nuevos títulos de pantalla en Money 2000                         | Comentario                                         |
|---------------------------------------|---------------------------------------------------------|-------------------------------------------------|
| **Administrador de cuentas**                   | **Seleccionar una cuenta** **Configure your accounts (Configurar las cuentas)**<br/> | El título estático ha cambiado a títulos activos.          |
| **Detalles de la cuenta**                   | **Cambio de la configuración de la cuenta**                                | El título estático ha cambiado a un título activo y específico. |
| **Calendario de pago**                  | **Pago de una factura**                                          | Título impreciso hecho descriptivo.                   |
| **Administrador de servicios financieros en línea** |                                                         | La página no es necesaria después del rediseño.                 |



 

### <a name="making-the-screen-title-prominent"></a>Hacer que el título de la pantalla se resalte

Una vez que se asenta en un título de pantalla útil, es importante asegurarse de que se llama la atención del usuario. Algunos estudios han demostrado que los usuarios rara vez leen texto informativo. Para ayudar a solucionar este problema, los títulos de pantalla deben diseñarse para que sean destacados y atractivos con el fin de llamar la atención del usuario. El diseño visual de la pantalla debe informar al usuario de que el título es lo más importante que se debe leer.

### <a name="step-three-make-the-pages-contents-suit-the-task"></a>Paso tres: Hacer que el contenido de la página se adapte a la tarea

Al crear software que siga las directrices de IUI, el trabajo de diseño más duro suele implicar la separación de características en pantallas o páginas. El siguiente paso consiste en determinar qué controles se usarán en cada pantalla para realizar su tarea principal. Estos controles son el contenido de la página, donde el usuario realiza el trabajo. El título de la pantalla y el contenido son dos mitades de un diálogo entre el programa y el usuario. El título plantea la pregunta del programa o proporciona una instrucción, y el usuario responde a través de la interfaz de la pantalla.

Si el título de la pantalla es claro y sencillo, el diseño de la pantalla suele ser sencillo. Por ejemplo, una de las pantallas de Money 2000 mostradas anteriormente se ha titulado "Elegir una cuenta para usarla". Dado este título, la pantalla obviamente debe contener una lista simple de cuentas entre las que el usuario puede elegir. Otra pantalla money 2000 tiene el título "Compruebe los elementos que se incluirán en los impuestos". Naturalmente, esta pantalla contiene una lista de comprobación de elementos.

Los usuarios deben poder averiguar fácilmente cómo usar controles para lograr la tarea principal de la pantalla. Cuando se le pide a los usuarios que seleccionen una cuenta y puedan buscar en la pantalla una lista de cuentas, confirman su comprensión de la tarea. Esto aumenta la posibilidad de que los usuarios se realicen correctamente, lo que también aumenta su confianza en la realización de otras tareas.

### <a name="screen-content-areas"></a>Áreas de contenido de pantalla

La ubicación y forma exactas de las áreas de contenido de la pantalla dependen del diseño del software. En Money 2000, la región de contenido de pantalla está todo debajo del título de la pantalla y a la derecha de la lista de tareas. Esta región puede desplazarse en pantallas largas. Es posible que también aparezca algún contenido no esencial en el área de estado debajo de la lista de tareas.

Los diseñadores pueden optar por elaborar la tarea principal de la pantalla en un párrafo en la parte superior de la región de contenido. Los usuarios nunca deben leer este texto, pero pueden resultar útiles. Muchos usuarios pueden omitirlo y seguir utilizando la pantalla correctamente. A diferencia del título, esta descripción puede desplazarse si la pantalla se puede desplazar. Para más información, consulte [Directrices para elegir títulos de pantalla.](#guidelines-for-choosing-screen-titles)

Si los diseñadores quieren que una página muestre recordatorios no esenciales, alertas u otra información de estado, se puede mostrar a la izquierda del área de contenido principal, en la lista de tareas del lado izquierdo de la pantalla. Funcionalmente, este área de estado es una región adicional para el contenido de la pantalla. Esta área no es lo suficientemente destacada como para contener controles esenciales.

### <a name="provide-a-clear-exit-from-the-page"></a>Proporcionar una salida clara de la página

Después de completar correctamente una tarea, el usuario se enfrenta a otro problema: cuándo y cómo salir de la pantalla. En el caso de las pantallas cuya tarea principal es la navegación, la realización de la propia tarea mueve al usuario a la pantalla siguiente. En otras pantallas, puede ser más difícil que el usuario sepa cómo continuar. Por ejemplo, en una pantalla que pide al usuario que escriba información en campos, es posible que el usuario necesite ayuda para averiguar cuándo y cómo avanzar. En estas páginas, a menudo resulta útil ofrecer un botón **Borrar** **Siguiente** o Listo en una ubicación coherente.

Los estudios de facilidad de uso han demostrado que los usuarios  prefieren  usar estos botones incluso cuando los botones de navegación global, como los botones Atrás o Inicio de una barra de herramientas, están disponibles. A menudo, los usuarios no son prácticos en las pantallas sin salida clara, incluso las pantallas cuyo único propósito es proporcionar información que se va a leer.

Para obtener más información sobre este tema, vea Proporcionar una manera fácil de completar una tarea e [iniciar](#provide-screens-for-starting-tasks) una nueva en la sección Directrices adicionales.

### <a name="step-four-offer-links-to-secondary-tasks"></a>Paso cuatro: Ofrecer vínculos a tareas secundarias

El último paso para diseñar una pantalla es proporcionar vínculos a tareas secundarias, que son características que no logran directamente la tarea principal, pero están relacionadas con la pantalla. Por ejemplo, si la tarea principal de una pantalla es escribir una letra, las tareas secundarias en esa pantalla podrían ser buscar una dirección de correo electrónico o imprimir un sobre.

Las tareas secundarias pueden abrir cuadros de diálogo, cambiar la presentación visual del contenido de la pantalla o navegar al usuario a otra pantalla. Una tarea secundaria podría realizar indirectamente la tarea principal o redirigir a los usuarios perdidos al lugar que está buscando.

Si una página es una conversación entre el equipo y el usuario, una tarea secundaria permite al usuario omitir la pregunta actual del equipo y pedir al equipo que haga otra cosa en su lugar. Por ejemplo, imagine este cuadro de diálogo: Equipo: "¿Qué factura quiere pagar?" Usuario: "En realidad, lo que realmente quiero hacer es encontrar una factura que he pagado hace un tiempo".

Algunas pantallas del producto no tendrán tareas secundarias, mientras que otras tendrán varias. Debe evitar la creación de una larga lista de tareas que probablemente serán difíciles de examinar para el usuario. Si una pantalla tiene una lista relativamente larga de tareas secundarias, las tareas más comunes deben colocarse en primer lugar, agruparse en una sección independiente o resaltar visualmente de otro modo.

La lista no debe incluir todas las tareas secundarias reconocibles, siempre y cuando sea obvio el siguiente paso de navegación. En lugar de ofrecer muchas tareas secundarias, una pantalla puede proporcionar tareas secundarias que navegan a páginas subsidiarias que enumeran más tareas.

### <a name="visual-design-of-secondary-tasks"></a>Diseño visual de tareas secundarias

Las tareas secundarias deben aparecer en una posición subordinada en la pantalla, donde son accesibles si es necesario, pero no distraen al usuario de la tarea principal. Colocar esta lista en una posición coherente en cada pantalla ayuda a los usuarios a encontrar la lista rápidamente cuando la necesiten.

Si muestra la lista de tareas secundarias en el lado izquierdo de la pantalla, la propia lista no debe ser desplazable ni debe desplazarse con la página, como se muestra en la siguiente captura de pantalla de la pantalla Pago de factura desde Money 2000. 

![captura de pantalla de la pantalla de pago de factura en 2000 dólares.](images/iuiguidelines07.png)

## <a name="additional-guidelines"></a>Directrices adicionales

En esta sección se describen cinco directrices útiles para crear una IUI según los cuatro pasos descritos en la sección anterior.

### <a name="use-consistent-screen-templates"></a>Uso de plantillas de pantalla coherentes

Al diseñar software que sigue el modelo de IUI, debe crear una plantilla para usarla como guía para cada pantalla. El modelo inductivo no dicta que use ninguna plantilla determinada. Hay muchas variaciones posibles que pueden satisfacer un diseño inductivo. Es posible que el producto solo necesite una plantilla para todas sus pantallas, o puede crear varias plantillas diferentes para varios fines.

Una buena plantilla permite que un nuevo usuario comprenda rápidamente cómo funcionan las pantallas del producto. El uso coherente de la plantilla en las pantallas del producto proporciona un buen flujo de interfaz de usuario de pantalla a pantalla. A medida que los usuarios aprenden a esperar que los mismos elementos aparezcan en los mismos lugares, pueden examinar y empezar a usar cada nueva pantalla más rápidamente.

### <a name="provide-screens-for-starting-tasks"></a>Proporcionar pantallas para iniciar tareas

Los productos diseñados con IUI suelen usar pantallas especiales diseñadas para iniciar a los usuarios en conjuntos de tareas. Estas pantallas se denominan páginas de actividad porque organizan grupos relacionados de tareas comunes. Las páginas de actividad proporcionan un punto de partida para los usuarios. Normalmente, una página de actividad presenta vínculos a otras páginas en las que el usuario realmente realiza el trabajo. Las páginas de actividad preguntan al usuario "¿Qué quiere hacer ahora?" y presentan una lista de posibles respuestas. Las páginas de actividad pueden seguir una plantilla especial para ayudar a los usuarios a reconocerlas.

Una página de actividad crea una página de inicio predeterminada para un producto. Cuando los usuarios inician una aplicación, generalmente tienen una idea en mente sobre la tarea que desean realizar. Normalmente, el motivo para iniciar el producto es una de un pequeño número de tareas muy comunes. La página de inicio predeterminada del producto lo reconoce haciendo evidente cómo comenzar tareas comunes.

La página Principal de  Money 2000 es un ejemplo de una página de actividad. De forma predeterminada, los usuarios ven esta pantalla, donde se muestra el acceso a tareas financieras comunes, como pagar una factura y equilibrar una cuenta, cuando inician la aplicación.

En la siguiente captura de pantalla se muestra la página De inicio **de Money** 2000.

![captura de pantalla de la página principal de money 2000. una página de actividad que enumera algunas tareas comunes y proporciona vínculos a conjuntos de tareas en otras páginas.](images/iuiguidelines08.png)

Dado que Money proporciona muchas características financieras, solo caben en la página Inicio las **tareas financieras más** comunes. Para todas las demás tareas, la **página Principal** se vincula a un conjunto de páginas de actividad subsidiarias denominadas centros financieros. Cada área principal de Money proporciona un centro financiero. Estas pantallas presentan el siguiente nivel de tareas, que sirve como punto de partida para todas las características dentro de cada área.

Por ejemplo, el área **Money Tax** contiene las características relacionadas con los impuestos del producto. El **área Impuestos** ofrece vínculos a estas características en una página **del Centro de** impuestos, como se muestra en la siguiente captura de pantalla.

![captura de pantalla de la página del centro fiscal money 2000. ](images/iuiguidelines09.png)

Una página de actividad también puede ser mucho más sencilla si hay menos opciones disponibles. En la siguiente captura de pantalla se muestra cómo se puede usar una página de actividad para administrar Windows cuentas de usuario.

![captura de pantalla de una página de actividad money 2000 para administrar cuentas de usuario de Windows. ](images/iuiguidelines10.png)

### <a name="make-it-obvious-how-to-carry-out-the-task-with-the-controls-on-the-screen"></a>Hacer evidente cómo llevar a cabo la tarea con los controles de la pantalla

La mejor manera de seguir esta guía es elegir un título de pantalla adecuado y limitar el ámbito de las tareas principales a solo la más común. Una vez que haya llegado a un título y un propósito claros para la página, elegir el conjunto correcto de controles será sencillo.

### <a name="provide-an-easy-way-to-complete-a-task-and-start-a-new-one"></a>Proporcionar una manera sencilla de completar una tarea e iniciar una nueva

El último obstáculo al que se enfrenta un usuario en una pantalla es averiguar cuándo y cómo salir. Normalmente, el usuario sale de la pantalla haciendo clic en un vínculo o realizando un comando que navega a otra pantalla. Estos vínculos pueden aparecer en el área de contenido de la pantalla, la lista de tareas o en las barras de herramientas de navegación. Los usuarios también pueden salir de una pantalla cerrando el archivo actual o la propia aplicación.

La tarea en algunas pantallas es prepararse para una operación que el usuario debe confirmar o cancelar. Estas pantallas suelen ofrecer un vínculo que realiza y confirma la operación y otro vínculo que se cancela. Si el usuario omite estas opciones y hace clic en otro vínculo, el programa debe realizar la opción menos destructiva. Las pantallas deben indicar lo que ocurrirá si el usuario toma esta ruta de acceso. Puede frases en los vínculos para que esto sea más obvio. Por ejemplo, un botón de confirmación con la etiqueta "Guardar cambios" implica que los cambios realizados en la pantalla no se harán efectivos hasta que se haga clic en ese botón.

Aunque los usuarios puedan salir siempre que quieran, es posible que todavía ofrezca un vínculo que sugiere una salida obvia de la página. Lo mismo se aplica a las páginas que simplemente muestran información estática. Para obtener más información sobre este tema, vea la sección [Proporcionar una salida clara de la página](#provide-a-clear-exit-from-the-page).

### <a name="starting-and-completing-processes"></a>Inicio y finalización de procesos

Para los fines de este artículo, los procesos son técnicas para trabajar con tareas que llevan al usuario a más de una pantalla.

Supongamos que un usuario hace clic en un vínculo de la lista de tareas o contenido de una pantalla y se le traslada a otra pantalla. A su vez, esa página podría ser la primera de una serie de pantallas que logra algún resultado general. Al final de esta serie de pantallas, el usuario quiere volver a la pantalla anterior al proceso. Hay al menos dos maneras de que el usuario pueda recuperar ? hacer clic botón Atrás varias veces o volver a la página principal y navegar desde allí ? pero ninguno de estos métodos es obvio o natural. La mayoría de los usuarios esperan encontrar un botón en la pantalla final que los devuelva directamente a la pantalla original.

El modelo de IUI admite este escenario a través del concepto de un proceso, una pantalla o una serie de pantallas que se tratan como una unidad de navegación. Los usuarios pueden entrar en el proceso, trabajar a través de sus pantallas y, en la última pantalla, buscar un botón que los devuelva a donde se iniciaron. Lo más importante es que el usuario puede iniciar el proceso desde varios lugares del producto. Los usuarios siempre se devuelven al lugar donde se iniciaron, independientemente de dónde estuvieran cuando iniciaron el proceso.

### <a name="process-name"></a>Nombre del proceso

A cada proceso se le debe dar un nombre y el nombre debe aparecer en alguna parte de cada pantalla del proceso. Money 2000 usa este enfoque. Cada pantalla que forma parte de un proceso general incluye el nombre de ese proceso en la parte superior. Este nombre de proceso se muestra de forma menos destacada que el título único de la pantalla porque es menos importante. El nombre del proceso recuerda a los usuarios qué proceso están realizando y refuerza la noción de que todas las pantallas del proceso forman parte de una sola característica. Por ejemplo, el **área Money Tax incluye** un proceso de **estimador de impuestos** que abarca varias pantallas. Cada pantalla de este proceso muestra el nombre del proceso colectivo y su título de pantalla único.

### <a name="implementation-of-processes"></a>Implementación de procesos

El mismo proceso se puede iniciar desde varios vínculos en distintas pantallas y los usuarios siempre se devolverán a la página de inicio correcta. Este comportamiento no se puede lograr a través de un vínculo codificado de forma fuerte en la pantalla final del proceso, porque el destino del vínculo variará. En su lugar, la aplicación puede implementar este comportamiento manteniendo una pila de procesos activos, independientemente de la pila de navegación normal que usan los comandos **Back** y **Forward.** Cuando el usuario inicia un proceso, la pantalla de inicio se inserta en la pila de procesos. Cuando el usuario  hace clic en el botón Listo en la pantalla final del proceso, la aplicación muestra la pantalla de inicio más reciente de la pila y devuelve el usuario a esa pantalla.

Cuando los usuarios se alejan de una pantalla de un proceso, el proceso permanece activo en la pila de procesos. Los usuarios pueden completar la copia de seguridad del proceso en la pantalla donde la abandonaron y, a continuación, continuar. Esto permite a los usuarios realizar un desviado, realizar una copia de seguridad y, a continuación, seguir con el proceso. Para ver cómo funciona este comportamiento, inicie cualquier proceso de compra en línea en el World Wide Web, salga del sitio y, a continuación, presione el **botón** Atrás. Por lo general, podrá recoger donde lo dejó.

### <a name="done-button"></a>Botón Listo

Para finalizar una pantalla y pasar a la siguiente pantalla del proceso, las pantallas pueden mostrar un botón cerca de la parte inferior de la página. La etiqueta de este botón es "Siguiente", "Listo" o algo similar. Si el botón finaliza el proceso y se puede  llamar al proceso desde varias ubicaciones, el título del botón Listo puede incluir el nombre de la ubicación de llamada.

### <a name="navigation-bar"></a>Barra de navegación

En cualquier pantalla, los usuarios pueden decidir que han terminado con el área actual del producto y quieren iniciar otra cosa. Es posible que no quiera completar explícitamente la pantalla actual antes de pasar a otra parte del producto. Una barra de herramientas de navegación puede ofrecer al usuario un conjunto de vínculos para iniciar nuevas tareas. Al igual que con otras listas de vínculos de tareas, deben seguir el principio de hacer que el siguiente paso de navegación sea obvio, que se describe con detalle en la sección siguiente.

### <a name="make-the-next-navigational-step-obvious"></a>Hacer que el siguiente paso de navegación sea obvio

Algunos programas pueden hacer que todas sus características estén disponibles al mismo tiempo. Por lo general, los usuarios deben navegar por un programa para encontrar una característica determinada. Los usuarios tienen más éxito en la navegación si pueden ver fácilmente cómo acercarse al menos un paso al resultado deseado. Las pantallas que usan IUI están diseñadas con este principio en mente.

Por ejemplo, las páginas de actividad no muestran necesariamente todas las tareas o destinos que el usuario podría querer lograr desde ese punto. En su lugar, las páginas de actividad proporcionan una lista de tareas lo suficientemente completas para que los usuarios puedan determinar fácilmente el vínculo adecuado para hacer clic, incluso si solo las lleva a otra página de vínculos. Las tareas más frecuentes deben ser más destacadas y requerir la menor cantidad de navegación. Las tareas menos frecuentes pueden requerir más pasos.

Este es un ejemplo de Money 2000. Supongamos que los usuarios desean realizar una operación que solo realizan ocasionalmente, como comprobar el importe estimado del pago de impuestos sobre la ingresos del próximo año. En primer lugar, los usuarios comienzan a buscar esta característica en la página Principal de Money 2000. Dado que la característica no aparece en la lista de tareas comunes, deben examinar la lista de áreas financieras. El **área Impuestos** parece ser una promesa, por lo que hacen clic en él. La **página Centro de** impuestos contiene un vínculo a la característica de estimación fiscal que buscan, por lo que hacen clic en ella y completan su tarea. Al aplicar los principios de IUI, Money 2000 permite a los usuarios encontrar intuitivamente lo que buscan.

## <a name="user-assistance"></a>Asistencia al usuario

En esta sección se describe un conjunto de directrices sugeridas para integrar el texto de asistencia del usuario en un producto que usa IUI.

La asistencia principal hace referencia a todo el texto que está visible en la pantalla (como se muestra en la siguiente captura de pantalla). La asistencia principal proporciona pistas textuales centradas en tareas para que los usuarios puedan comprender fácilmente toda la información presentada en la pantalla. Comprenden el propósito de la página y la forma en que los objetos se relacionan entre sí para ayudar a realizar tareas. Dado que el texto está directamente en la pantalla, la información que responde a preguntas no técnicas como "¿Qué debo hacer?" es fácil de acceder y altamente visible sin que el usuario tenga que realizar ninguna acción.

![captura de pantalla de la pantalla de configuración de la cuenta de money 2000.](images/iuiguidelines11.png)

La asistencia secundaria consta de todo el texto que no está visible en la pantalla y requiere cierta interacción del usuario para acceder, como hacer clic o mantener el puntero sobre un elemento de la interfaz de usuario. Este contenido no es esencial para realizar la tarea en curso, pero sigue estando directamente relacionado.

### <a name="primary-assistance"></a>Asistencia principal

La asistencia principal puede incluir algunos o todos los componentes siguientes:

-   Título de la pantalla

    Ejemplo: Cambiar la imagen

    El título de la pantalla es el primer elemento más importante que aparece en la pantalla. Su finalidad es describir en el propio lenguaje del usuario la tarea que se puede completar en esta página. El título de la pantalla debe evitar describir los detalles de cómo completar la tarea. El texto del título de la pantalla solo debe hacer referencia a la tarea principal de la pantalla. Como regla general, cuanto más sencilla y más corta sea la descripción de la tarea, es probable que la tarea esté mejor definida. Para obtener información más detallada sobre este tema, vea Paso dos: [Estado de la tarea](#step-two-state-the-task).

-   Subtítulo de pantalla

    Ejemplo: también puede descargar una nueva imagen de Internet.

    Incluso con un esfuerzo cuidadoso, es posible que el título de la pantalla no sea suficiente para explicar adecuadamente una tarea compleja. El subtítulo le permite elaborar en función del propósito de la pantalla. Puede usar un subtítulo para ayudar a aclarar el propósito de la página, proporcionar una descripción adicional de la tarea o ayudar a establecer las expectativas. Los usuarios que no lean el subtítulo deben poder usar la página correctamente. Al igual que el título, el subtítulo debe evitar describir los detalles para completar la tarea.

-   Tareas

    Ejemplo: Cambio del protector de pantalla

    Las tareas se pueden presentar como vínculos de texto o imágenes gráficas que requieren la interacción del usuario. Los comandos que se presentan como vínculos de texto deben basarse en verbos y escribirse como tareas claras y concisas.

-   Etiquetas para los botones de comando

    Ejemplo: Crear contraseña

    Hay tres tipos de botones de comando:

    -   Cancelar
    -   Listo
    -   Commit

    Los botones Cancelar y Listo simplemente usan "Cancelar" y "Listo" como etiquetas. Los botones de confirmación deben usar etiquetas de texto activas en lugar de "Aceptar". Por ejemplo, use "Crear contraseña" en lugar de "Aceptar".

-   Etiquetas para otros controles

    Ejemplo: Escriba la contraseña.

    Las etiquetas de los controles, como los botones de radio, las casillas y los cuadros de texto, deben escribirse de forma clara y concisa para que los usuarios sepan exactamente para qué son los controles, cuáles usar y qué información se debe proporcionar para realizar su tarea.

-   Vínculos "Tareas relacionadas"

    Ejemplo: Tareas relacionadas: cambio de otra cuenta

    Los vínculos "Tareas relacionadas" son puntos de entrada explícitos a otras tareas relacionadas con la característica actual. Deben escribirse como vínculos basados en tareas.

-   Vínculos "Ver también"

    Ejemplo: Consulte también: Cambio del tema

    Los vínculos "Ver también" son tareas secundarias. Están relacionados con la tarea principal, pero sacarán al usuario del contexto actual. Deben aparecer como vínculos de tareas normales. Para obtener más información sobre las tareas secundarias, [vea Diseño visual de tareas secundarias.](#visual-design-of-secondary-tasks)

### <a name="secondary-assistance"></a>Asistencia secundaria

La asistencia secundaria puede incluir algunos o todos los componentes siguientes:

-   Información sobre información

    Puede usar una información sobre información para proporcionar al usuario información adicional sobre un vínculo de tarea o un botón de comando. Por ejemplo, una información sobre información sobre un vínculo de tarea podría leer "Muestra una página donde puede elegir una imagen para usarla con su cuenta". La información sobre información aparece cuando el usuario mantiene el mouse sobre el objeto asociado. Debe crear información sobre todos los elementos de la interfaz de usuario en los que el usuario pueda hacer clic.

-   Temas de ayuda sobre "Más información"

    Ejemplo: Más información sobre la descarga de un archivo

    Los vínculos "Más información" abren temas de Ayuda, como información general de características, información conceptual, información de soporte técnico e información de procedimientos. Para reducir el desorden, debe minimizar el número de temas de ayuda de "Más información" en la pantalla.

## <a name="appendix-designing-and-testing-microsoft-money-2000"></a>Apéndice: Diseño y prueba de Microsoft Money 2000

Esta sección se ha adaptado a partir de las propias descripciones de primera mano de los diseñadores. Se describe cómo el equipo de Money 2000 modificó el proceso de diseño y pruebas para adaptarse al modelo de IUI.

### <a name="designing-and-testing-money-2000"></a>Diseño y prueba de Money 2000

El diseño de Money 2000 mediante el modelo de navegación inducido llevó al equipo a interrogar a los diseños que habían estado en el producto durante mucho tiempo. Dado que los principios del modelo son simples, era fácil adoptar el modelo en el proceso de diseño y permanecer con él. Al final, los diseñadores creen que el modelo les ha ayudado a crear mejores diseños de los que podrían haber producido sin él.

### <a name="clearer-titles-and-designs"></a>Títulos y diseños más claros

Los diseñadores de Money 2000 observaron que a menudo describen características con palabras que no aparecían realmente en la pantalla. En el modelo de IUI, las pantallas deben explicarse a sí mismas. Por ejemplo, el equipo explicó que la pantalla etiquetada Calendario de **pago** estaba pensada para pagar facturas. En Money 2000, esa pantalla se denomina **Pago de facturas.** Todos los elementos que no están relacionados con ese propósito se han movido a pantallas subsidiarias, lo que da lugar a un diseño más claro.

Otro ejemplo implica una pantalla denominada **Online Financial Services Manager**. El equipo tuvo dificultades para obtener una explicación sencilla del propósito de esta pantalla. Cuando no pudieron llegar a una, quitaron esta pantalla y distribuyeron sus características entre páginas más definidas lógicamente.

### <a name="helping-new-designers"></a>Ayudar a los nuevos diseñadores

Al equipo le ha resultado fácil enseñar técnicas de diseño de IUI a nuevos diseñadores de software sin experiencia. Las técnicas permiten a los diseñadores de todos los niveles de experiencia evaluar sus diseños mediante el uso de títulos de pantalla como prueba de claridad. Cuando se le obliga a colocar un título claro y conciso en una pantalla mal diseñada, los diseñadores reconocen rápidamente que ningún título era lo suficientemente bueno para la página. Se dieron cuenta de que el problema no era elegir palabras para un título, sino en un diseño de pantalla defectuoso. Con esta comprensión, podrían rediseñar la pantalla para admitir una interacción más clara del usuario y, por tanto, un título más claro.

### <a name="including-writers"></a>Inclusión de escritores

A medida que avanzaba el diseño, el equipo se dio cuenta de que los escritores y editores de documentación deberían participar en la creación de títulos de pantalla. Los escritores estaban limitados en su capacidad de elegir buenos títulos en versiones anteriores porque solo estaban implicados en una fase tardía. Los diseñadores o programadores suelen dar títulos de trabajo temporales a las pantallas. Estos títulos se usaron hasta finales del ciclo del producto cuando se solicitó a los escritores que crearan los títulos finales de la pantalla. En ese momento, era demasiado tarde para volver a trabajar con pantallas mal diseñadas.

Por el contrario, el equipo de Money 2000 ha implicado a escritores en las primeras fases del proceso de diseño. Esto hizo que se incluyese información valiosa en los títulos de pantalla cuando todavía podía ayudar al diseño. Si una pantalla era demasiado compleja para permitir un título claro, los escritores podrían sugerir que la página se rediseñase.

Al final del proyecto, los escritores y diseñadores creen que los títulos de pantalla eran más claros y más fuertes que en versiones anteriores. A los escritores también les resulta más fácil explicar nuevas páginas, lo que facilita el trabajo de documentar el producto. Todos los miembros del equipo pensaron que la implicación de todas las materias en la fase de diseño ha hecho que el producto sea mejor y más fácil de usar.

### <a name="usability-tests"></a>Pruebas de facilidad de uso

Durante el desarrollo de Money 2000, el equipo realizó varias pruebas de facilidad de uso para ver las diferencias entre la antigua estructura de navegación de Money 99 y los cambios que se realizaron como resultado de aplicar el modelo de IUI.

### <a name="prototype-testing"></a>Pruebas de prototipos

Al principio del proceso de desarrollo de productos, los diseñadores crearon un prototipo para explorar cómo reaccionarían los usuarios a IUI. Este trabajo se hizo muy pronto en el proceso de desarrollo para dar tiempo a refinar los principios del modelo antes de que los programadores empezaran a revisar el propio producto.

El equipo creó un prototipo en Microsoft Visual Basic y HTML que simulaba finanzas personales actividades realizadas normalmente en Money. En el prototipo, los usuarios podrían navegar a más de 50 páginas que representan las áreas principales del producto. En estas áreas, podrían configurar cuentas financieras, pagar facturas, ver informes y trabajar con sus inversiones.

Once participantes realizaron el mismo conjunto de tareas tanto en Money 99 como en el prototipo de IUI. Se asignaron aleatoriamente para usar uno de los productos en primer lugar. Cuatro participantes eran usuarios actuales de Money, cuatro eran usuarios actuales de un producto de la competencia y tres nunca habían usado un finanzas personales anterior.

Las preferencias generales indicaron que los cuatro usuarios actuales de Money preferían Money 99 (la versión que habían estado usando en casa), mientras que los siete usuarios restantes preferían el nuevo prototipo a la versión actual. Para todas las demás medidas, no hubo ninguna diferencia entre los usuarios de los tres grupos. En términos de rendimiento general, los usuarios se encontraban en el área incorrecta del producto el doble de veces que usaban Money 99 (2,82 veces por tarea) que en el prototipo (1,45 veces por tarea). Otras medidas de rendimiento y datos de preferencia, aunque no son significativas, parece que favorecen el prototipo. En función de estos datos y otras pruebas, el equipo del producto Money decidió incorporar los principios de IUI en Money 2000.

### <a name="product-testing"></a>Pruebas de productos

Una vez completada la mayor parte del código del producto, el equipo realizó otro estudio de facilidad de uso para examinar la implementación final de IUI. En esta prueba, 10 participantes que nunca habían usado un producto finanzas personales antes se seleccionaron para usar Money 99 o Money 2000. Todos los usuarios realizaron las mismas tareas.

Los usuarios de Money 2000 completaron correctamente el 89 % de las tareas, mientras que los usuarios de Money 99 completaron correctamente solo el 74 % de las tareas. Al igual que con el prototipo, los usuarios también aparecían más rápidos, pero no significativamente diferentes, al navegar en Money 2000 en comparación con Money 99. Además, las medidas de satisfacción subjetiva generales para la navegación también tienden a ser más altas para Money 2000 que para Money 99.

### <a name="controlled-testing"></a>Pruebas controladas

Dado que Money 2000 es enorme y complejo, no es adecuado para llevar a cabo experimentos controlados sobre los efectos de aplicar IUI. En su lugar, el equipo creó un entorno más restringido para la prueba.

La prueba implicaba una aplicación "Visor del mercado de valores" que permitía a los usuarios modificar la presentación de un informe de la bolsa que se muestra en la pantalla. Los usuarios podían cambiar qué columnas de datos se incluían en el informe, el orden de las columnas del informe, su alineación y el número de posiciones decimales usadas. Los diseñadores querían ver cómo funcionaría un enfoque de IUI para esta tarea en comparación con una interfaz gráfica de usuario convencional.

En la siguiente captura de pantalla se muestra la interfaz de usuario convencional utilizada en la prueba. Un solo cuadro de diálogo realiza todas las tareas de personalización de informes. Muchas aplicaciones proporcionan un cuadro de diálogo similar para seleccionar un subconjunto de una lista de elementos. El cuadro de diálogo contiene dos listas: la lista izquierda muestra todas las columnas de informe disponibles y la derecha muestra el subconjunto de columnas que el usuario ha seleccionado para el informe. Los controles adicionales modifican el orden y los atributos de formato de las columnas de informe seleccionadas en la lista de la derecha.

![captura de pantalla de un cuadro de diálogo convencional.](images/iuiguidelines12.png)

Para la versión de IUI de esta tarea, el equipo creó una aplicación de estilo web. Cada tarea de personalización se colocó en una página independiente. La aplicación también incluía una página principal, que se muestra en la siguiente captura de pantalla, que pregunta a los usuarios cómo quieren personalizar el informe.

![captura de pantalla de una pantalla de prueba de iui.](images/iuiguidelines13.png)

Al hacer clic en los vínculos de esta página principal, el usuario se lleva a páginas adicionales para realizar tareas de personalización específicas. Por ejemplo, la siguiente captura de pantalla muestra la página que se usa para seleccionar columnas de informe.

![captura de pantalla de una pantalla de prueba de iui para seleccionar columnas de informe.](images/iuiguidelines14.png)

En las pruebas de ambas versiones, se solicitó a los asuntos que personalizaran los informes de un estado inicial determinado (que se muestra en la pantalla) a un estado objetivo especificado (que se muestra en un documento de entrega). El equipo realizó un seguimiento de la cantidad de tiempo y el número de intentos que los sujetos realizaron para personalizar el informe. El equipo informó a los usuarios cuando habían personalizado correctamente el informe.

La prueba incluyó 88 participantes. Se ha pedido a cada participante que personalice un conjunto de 11 informes con una de las dos versiones de la aplicación. Además, 72 de estos participantes devolvieron una semana después para personalizar otro conjunto de 11 informes con la misma versión de la primera sesión. Cada asunto se clasificó como un usuario de equipo principiante, usando principalmente el equipo para el correo electrónico, jugar a la música y navegar por la Web.

No hubo diferencias significativas entre los usuarios de las dos versiones ni ninguna de las otras variables de interés. Los usuarios realizaron tareas a la misma velocidad, se iteraron en la tarea el mismo número de veces y tenían las mismas clasificaciones de satisfacción subjetiva generales para las dos versiones. Por lo tanto, esta prueba no pudo mostrar ninguna medida en la que la IUI provocara una mejora o degradación en el rendimiento o las clasificaciones subjetivas.

Podría considerarse que si el usuario tiene que navegar más para realizar la tarea, la cantidad de tiempo para realizar la tarea debe ser mayor. Aunque este experimento no sugiere este resultado, es importante tener en cuenta que los tiempos de rendimiento medio y sus desviaciones estándar asociadas para los dos enfoques diferentes de esta tarea eran casi idénticos.

Será necesario realizar investigaciones adicionales para determinar si hay mejoras cuantificables del uso de IUI. Como mínimo, esta prueba no proporciona ninguna evidencia de que la IUI dañe el rendimiento o el uso del producto.

### <a name="comparison-with-web-sites"></a>Comparación con sitios web

Muchos sitios web bien diseñados usan principios similares al modelo de IUI descrito en este documento. Probablemente se trata de un efecto secundario de la forma en que funciona la Web. Dado que es difícil implementar interacciones complejas entre controles en una sola página web, los diseñadores suelen dividir las tareas en partes que implican más de un viaje al servidor para obtener una página nueva. Algunos sitios incluso incluyen títulos de página que muestran claramente el propósito de la página.

Los diseñadores de aplicaciones tradicionales tienen un conjunto mucho más completo de herramientas disponibles. Esto les proporciona más flexibilidad, pero también proporciona más oportunidad para crear páginas complejas y confusas. Al crear interfaces de usuario inertes, los diseñadores deben usar esta eficacia con discreción y recordar valorar la claridad y la simplicidad.

 

 





