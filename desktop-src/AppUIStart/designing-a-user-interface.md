---
title: Diseño de un Interfaz de usuario
description: En esta sección se describen en detalle algunas de las tareas asociadas al diseño de una interfaz de usuario para una Windows aplicación.
ms.assetid: 22deda0c-bf03-4fcd-9cc9-6381b601c152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914f8a2bf2afb532e3deed8876ce0ddea0fe71a0e8ad5457e5967e5f48eeb2c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440315"
---
# <a name="designing-a-user-interface"></a>Diseño de un Interfaz de usuario

En esta sección se describen en detalle algunas de las tareas asociadas al diseño de una interfaz de usuario para una Windows aplicación.

-   [Introducción](#introduction)
-   [Requisitos funcionales](#functional-requirements)
-   [Análisis de usuarios](#user-analysis)
    -   [Instrucciones de problema](#problem-statements)
    -   [Prioridades](#priorities)
-   [Diseño conceptual](#conceptual-design)
-   [Diseño lógico](#logical-design)
-   [Diseño físico](#physical-design)

## <a name="introduction"></a>Introducción

El diseño de la interfaz de usuario se puede dividir en tres elementos esenciales: funcionalidad, apariencia y rendimiento.

Con más frecuencia que no, el enfoque principal durante el desarrollo de aplicaciones es la funcionalidad. ¿Se puede hacer uso de la aplicación? ¿Permite a los usuarios completar tareas? Sin embargo, la funcionalidad es solo una parte de la historia.

En las apariencias se describe cómo se muestran y presentan las cosas, el estilo en el que se comunican las cosas al usuario. La apariencia es muy subjetiva y mucho más difícil de cuantificar que los requisitos funcionales y las métricas de rendimiento. Las emociones suelen llegar a opciones sencillas( cómo los colores se complementan entre sí o cómo los elementos de la interfaz de usuario transmiten su significado) que a menudo afectan a la manera en que una persona se siente sobre algo e influyen en su éxito.

El rendimiento se mide no solo por la velocidad, sino también por la confiabilidad. Si una aplicación tiene un aspecto excelente, es fácil de usar, pero se bloquea repetidamente, es probable que no sea muy correcta. La aplicación tiene que proporcionar a un usuario plena confianza en su confiabilidad.

Las siguientes son algunas tareas de fase de diseño que pueden contribuir a una interfaz de usuario correcta para una Windows aplicación.

## <a name="functional-requirements"></a>Requisitos funcionales

Tenga en cuenta las siguientes sugerencias al principio de la fase de diseño para optimizar la experiencia del usuario en el público más amplio posible:

-   Siga las directrices de diseño de la interfaz de usuario.

    Familiarícese con las [Windows](../uxguide/guidelines.md) de interacción de la experiencia del usuario y haga referencia a ellas a menudo a medida que progresa el diseño, la implementación y las pruebas de la interfaz de usuario de la aplicación.

-   Asegúrese de que la interfaz de usuario sea accesible.

    Asegúrese de integrar la accesibilidad en el diseño de la interfaz de usuario desde el principio del ciclo de vida del producto. La accesibilidad de la retroajuste puede ser muy costosa porque parte del desarrollo de accesibilidad requiere atención en el nivel arquitectónico. Para obtener más información, descargue el libro electrónico [Software de ingeniería para accesibilidad](https://www.microsoft.com/download/details.aspx?id=19262).

-   Compatibilidad con Marketplace internacional.

    Windows incluye tecnologías que permiten la compatibilidad con muchas referencia culturales y lenguajes escritos en una Windows aplicación. Si la aplicación tiene como destino marketplace internacional, es importante incluir la compatibilidad con la internacionalización en el diseño de la interfaz de usuario desde el principio del proyecto. Para obtener más información, vea [Internacionalización para Windows Aplicaciones](../intl/international-support.md).

## <a name="user-analysis"></a>Análisis de usuarios

Un paso fundamental para diseñar una interfaz correcta es lograr un conocimiento básico de lo que los usuarios necesitan y desean de una aplicación antes de escribir cualquier código. Recuerde que los usuarios potenciales de una aplicación ya están realizando su trabajo de alguna manera y las herramientas y los procesos existentes deben entenderse lo máximo posible. No diseñe sin tener en cuenta completamente estos problemas.

El enfoque más sencillo e informal es hablar con los usuarios previstos del producto. Obtenga información directamente del origen: evite el uso de administradores o ejecutivos como servidores proxy para los consumidores reales. Considere la posibilidad de que grupos pequeños de desarrolladores y administradores de programas paguen visitas informales a los usuarios de sus lugares de trabajo, donde existe la oportunidad de analizar cómo funcionan y recopilar detalles de los problemas a los que se enfrentan con sus herramientas actuales.

Recuerde que no debe hacer preguntas iniciales o sesgadas, ya que esto afectará directamente a la calidad y validez de los comentarios del usuario. Tenga en cuenta lo siguiente al crear preguntas durante esta fase:

-   Quién Son nuestros usuarios? ¿Qué aptitudes y conocimientos tienen?
-   ¿Qué diferentes orígenes de datos podemos usar para comprender su experiencia?
-   ¿Qué objetivos y tareas usarán nuestro producto para completarse?
-   ¿Qué suposiciones se están realizando y cómo se pueden comprobar?
-   ¿Qué orígenes de datos tenemos? (Los estudios de facilidad de uso y las evaluaciones heurísticas son buenos lugares para empezar).

### <a name="problem-statements"></a>Instrucciones de problema

Una vez que se hayan recopilado todos los comentarios de los usuarios, analice y resalte los problemas y requisitos relacionados. Intente evitar pensar en soluciones en este momento. Asegúrese de que los problemas están totalmente identificados, no solo los síntomas.

A menudo resulta útil crear una lista de instrucciones de problema de una frase (desde la perspectiva de los usuarios) para cada problema o requisito. Por ejemplo, "Cambiar el tamaño del ancho del cuadro de edición a 15 caracteres" no es un problema. Pero "Es demasiado difícil escribir en términos de búsqueda largos" es una instrucción de problema válida. La diferencia es drástica. Intente no definir la solución y el problema al mismo tiempo: a menudo se pierde el problema real. En este ejemplo, puede haber muchas otras formas de resolver el problema de los términos de búsqueda, incluido el cambio del tamaño del cuadro de edición. Tenga siempre en cuenta soluciones alternativas.

A continuación se muestran ejemplos adicionales de instrucciones de problema:

-   Es difícil navegar de una sección del sitio web a otra.
-   Los usuarios tienen que esperar demasiado tiempo para que se cargue el software.
-   Nuestros mensajes de error de seguridad son difíciles de entender.
-   La página de registro tiene demasiadas preguntas y los usuarios suelen abandonarla.
-   Encontrar un producto específico en el índice del sitio es demasiado difícil de completar.

Si las declaraciones del problema son lo suficientemente amplias, es probable que haya muchas maneras innovadoras y creadoras de resolverlas.

### <a name="priorities"></a>Prioridades

El acto de tomar una lista de elementos y clasificarlos por prioridad define una versión. Sin prioridades claras, los equipos pueden enfrentarse y argumentar qué cosas se deben hacer y qué cosas se deben cortar. El trabajo implicado en la definición de prioridades debe ser más fácil con la investigación completa, pero siempre es un desafío.

Establecer prioridades requiere la capacidad de evaluar al menos en tres criterios: programación, equipo y negocio. Puede haber una programación predefinida establecida para el proyecto, que limita el tamaño y la escala del trabajo que se puede realizar. No se debe intentar un problema que requiera volver a escribir la mitad del código base durante un ciclo de versión pequeño.

La composición y la naturaleza de un equipo definen qué tipos de trabajo se pueden realizar. ¿Qué otros compromisos tiene el equipo? ¿Hay un diseñador o un ingeniero de facilidad de uso en el equipo? ¿Qué aptitudes tiene el equipo con el diseño web o de interfaz de usuario? Por último, y lo más importante, son las consideraciones empresariales. ¿Cuáles son los objetivos de ingresos de este proyecto? Quién son los competidores? ¿Cuáles son las ventajas de resolver ciertos problemas? ¿Qué asociaciones se pueden falsificación? Cualquier otra consideración también debe identificarse antes de priorizar la lista.

Una vez priorizado, la lista de instrucciones de problema establece la dirección del producto y garantiza que el desarrollo se dirigirá a las áreas correctas.

## <a name="conceptual-design"></a>Diseño conceptual

Normalmente, la interfaz de usuario no se aborda en la fase de diseño conceptual. Sin embargo, esta fase requiere un modelo de negocio exhaustivo con perfiles de usuario completos y escenarios de uso que son imperativos para una experiencia de usuario correcta.

## <a name="logical-design"></a>Diseño lógico

La fase de diseño lógico es cuando se desarrollan los prototipos iniciales que admiten el diseño conceptual.

Las tecnologías específicas de hardware y software que se usarán durante el desarrollo también se identifican en esta fase, que puede determinar las funcionalidades de la interfaz de usuario en el producto final. Para obtener más información, [vea Interfaz de usuario Technologies](user-interface-technologies-for-windows-applications.md).

Además de las herramientas de desarrollo, se deben identificar los distintos requisitos de hardware y los factores de forma a los que se dirigirá la aplicación.

## <a name="physical-design"></a>Diseño físico

La fase de diseño físico determina cómo se va a implementar un diseño de interfaz de usuario para el hardware y los factores de forma específicos que se identificaron en el diseño lógico.

Durante esta fase, las limitaciones de hardware o factor de forma pueden introducir restricciones inesperadas en la interfaz de usuario que requieren mejoras significativas en el diseño.

 

 