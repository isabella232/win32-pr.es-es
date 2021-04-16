---
title: Diseñar una interfaz de usuario
description: En esta sección se describen detalladamente algunas de las tareas asociadas al diseño de una interfaz de usuario para una aplicación Windows.
ms.assetid: 22deda0c-bf03-4fcd-9cc9-6381b601c152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97d5027baf7276b1353e03254478545e554daa5e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488027"
---
# <a name="designing-a-user-interface"></a>Diseñar una interfaz de usuario

En esta sección se describen detalladamente algunas de las tareas asociadas al diseño de una interfaz de usuario para una aplicación Windows.

-   [Introducción](#introduction)
-   [Requisitos funcionales](#functional-requirements)
-   [Análisis de usuarios](#user-analysis)
    -   [Instrucciones problemáticas](#problem-statements)
    -   [Fija](#priorities)
-   [Diseño conceptual](#conceptual-design)
-   [Diseño lógico](#logical-design)
-   [Diseño físico](#physical-design)

## <a name="introduction"></a>Introducción

El diseño de la interfaz de usuario se puede dividir en tres elementos esenciales: funcionalidad, estética y rendimiento.

Con mayor frecuencia que no, el enfoque principal durante el desarrollo de aplicaciones es la funcionalidad. ¿Se puede usar la aplicación? ¿Permite a los usuarios completar tareas? Sin embargo, la funcionalidad es solo una parte de la historia.

Los aspectos estéticos describen cómo se muestran y presentan las cosas, el estilo en el que se comunican los elementos al usuario. La estética es muy subjetiva y mucho más difícil de cuantificar que los requisitos funcionales y las métricas de rendimiento. Las estéticas suelen ser opciones sencillas, cómo se complementan los colores entre sí o cómo los elementos de la interfaz de usuario transmiten su significado, que a menudo afectan al modo en que una persona se siente sobre algo e influye en el éxito de su uso.

El rendimiento se mide no solo con la velocidad, sino también con la confiabilidad. Si una aplicación tiene un aspecto fantástico, es fácil de usar, pero se bloquea repetidamente, es probable que no sea muy satisfactorio. La aplicación tiene que proporcionar a un usuario que tenga plena confianza en su confiabilidad.

A continuación se muestran algunas tareas de la fase de diseño que pueden contribuir a una interfaz de usuario correcta para una aplicación Windows.

## <a name="functional-requirements"></a>Requisitos funcionales

Tenga en cuenta las siguientes sugerencias en el principio de la fase de diseño para optimizar la experiencia del usuario en la audiencia más amplia posible:

-   Siga las directrices de diseño de la interfaz de usuario.

    Familiarícese con las [directrices de interacción](../uxguide/guidelines.md) de la experiencia del usuario de Windows y haga referencia a ellas con frecuencia a medida que progresa el diseño, la implementación y las pruebas de la interfaz de usuario de la aplicación.

-   Asegúrese de que la interfaz de usuario está accesible.

    Asegúrese de integrar la accesibilidad en el diseño de la interfaz de usuario desde el principio del ciclo de vida del producto. La accesibilidad de los reajustes puede ser extremadamente costosa porque parte del desarrollo de accesibilidad requiere atención en el nivel arquitectónico. Para obtener más información, descargue el [libro electrónico de Engineering Software for Accessibility](https://www.microsoft.com/download/details.aspx?id=19262).

-   Compatibilidad con marketplace internacional.

    Windows incluye tecnologías que permiten la compatibilidad con muchas referencias culturales y lenguajes escritos en una aplicación Windows. Si la aplicación está destinada al Marketplace internacional, es importante incluir la compatibilidad con la internacionalización en el diseño de la interfaz de usuario desde el principio del proyecto. Para obtener más información, vea [internacionalización para aplicaciones Windows](../intl/international-support.md).

## <a name="user-analysis"></a>Análisis de usuarios

Un paso crítico para diseñar una interfaz correcta es lograr un conocimiento básico de lo que los usuarios necesitan y desean de una aplicación antes de escribir cualquier código. Recuerde que los posibles usuarios de una aplicación ya están haciendo su trabajo de alguna manera y las herramientas y los procesos existentes deben entenderse lo máximo posible. No diseñe sin tener en cuenta estos problemas.

El enfoque más sencillo y informal está hablando con los usuarios previstos del producto. Obtener información directamente del origen: Evite usar administradores o ejecutivos como servidores proxy para los consumidores reales. Considere la posibilidad de que los pequeños grupos de desarrolladores y administradores de programas paguen visitas informales a los usuarios de sus lugares de trabajo, donde existe la oportunidad de analizar cómo funcionan y recopilar los detalles de los problemas a los que se encuentran con sus herramientas actuales.

Recuerde que no debe plantear preguntas iniciales o sesgadas, ya que esto afectará directamente a la calidad y la validez de los comentarios de los usuarios. Tenga en cuenta lo siguiente al redactar preguntas durante esta fase:

-   ¿Quiénes son nuestros usuarios? ¿Qué Aptitudes y conocimientos tienen?
-   ¿Qué diferentes orígenes de datos se pueden usar para entender su experiencia?
-   ¿Qué objetivos y tareas usarán nuestro producto para completarse?
-   ¿Qué suposiciones se están realizando y cómo se pueden comprobar?
-   ¿Qué orígenes de datos tenemos? (Los estudios de facilidad de uso y las evaluaciones heurística son buenos lugares para empezar).

### <a name="problem-statements"></a>Instrucciones problemáticas

Una vez que se han recopilado todos los comentarios de los usuarios, analice y divierta en problemas y requisitos relacionados. Intente evitar pensar en las soluciones en este momento. Asegúrese de que los problemas se identifican por completo, no solo de los síntomas.

A menudo resulta útil crear una lista de instrucciones problemáticas (desde la perspectiva de los usuarios) para cada problema o requisito. Por ejemplo, "cambiar el ancho del cuadro de edición a 15 caracteres" no es un problema. Pero "es demasiado difícil escribir en términos de búsqueda largos" es una declaración de problema válida. La diferencia es considerable. Intente no definir la solución y el problema al mismo tiempo: a menudo se pierde el problema real. En este ejemplo, puede haber muchas otras formas de solucionar el problema de los términos de búsqueda, incluido cambiar el tamaño del cuadro de edición. Siempre tenga en cuenta las soluciones alternativas.

A continuación se muestran ejemplos adicionales de instrucciones problemáticas:

-   Es difícil desplazarse de una sección del sitio web a otra.
-   Los usuarios tienen que esperar demasiado tiempo para cargar el software.
-   Los mensajes de error de seguridad son difíciles de entender.
-   La página de registro tiene demasiadas preguntas y los usuarios suelen abandonarla.
-   La búsqueda de un producto específico en el índice del sitio es demasiado difícil de completar.

Si las instrucciones problemáticas son lo suficientemente amplias, es probable que haya muchas formas innovadoras y creativas de resolverlas.

### <a name="priorities"></a>Prioridades

La acción de tomar una lista de elementos y clasificarlos por prioridad define una versión. Sin claras prioridades, los equipos pueden combatir y discutir qué cosas deben realizarse y qué cosas deben cortar. El trabajo necesario para establecer las prioridades debe ser más fácil con la investigación completa, pero siempre es un reto.

La configuración de prioridades requiere la capacidad de evaluar al menos tres criterios: programación, equipo y negocio. Puede haber un conjunto de programación predefinido para el proyecto, lo que limita el tamaño y la escala del trabajo que se puede realizar. Un problema que es probable que requiera la reescritura de la mitad del código base no debe intentarse durante un ciclo de versión pequeño.

La composición y la naturaleza de un equipo definen qué tipos de trabajo se pueden realizar. ¿Qué otros compromisos tiene el equipo? ¿Hay algún Ingeniero de diseñador o de facilidad de uso en el equipo? ¿Qué conocimientos tiene el diseño web o de la interfaz de usuario que tiene el equipo? Por último, y lo más importante, son consideraciones empresariales. ¿Cuáles son los objetivos de ingresos para este proyecto? ¿Quiénes son los competidores? ¿Cuáles son las ventajas de resolver determinados problemas? ¿Qué asociaciones se pueden falsificar? También debe identificarse cualquier otra consideración antes de dar prioridad a la lista.

Una vez establecida la prioridad, la lista de instrucciones problemáticas establece la dirección del producto y garantiza que el desarrollo está dirigido a las áreas adecuadas.

## <a name="conceptual-design"></a>Diseño conceptual

Normalmente, la interfaz de usuario no se trata en la fase de diseño conceptual. Sin embargo, esta fase requiere un modelo de negocio completo con los perfiles de usuario completos y los escenarios de uso que son imprescindibles para una experiencia de usuario correcta.

## <a name="logical-design"></a>Diseño lógico

La fase de diseño lógico es cuando se desarrollan los prototipos iniciales que admiten el diseño conceptual.

Las tecnologías de hardware y software específicas que se van a usar durante el desarrollo también se identifican en esta fase, que puede determinar las capacidades de la interfaz de usuario en el producto final. Para obtener más información, consulte [tecnologías de interfaz de usuario](user-interface-technologies-for-windows-applications.md).

Además de las herramientas de desarrollo, deben identificarse los diversos requisitos de hardware y factores de forma que se van a usar como destino de la aplicación.

## <a name="physical-design"></a>Diseño físico

La fase de diseño físico determina cómo se va a implementar un diseño de la interfaz de usuario para el hardware específico y los factores de forma que se identificaron en el diseño lógico.

Durante esta fase, las limitaciones de hardware o de factor de forma pueden presentar restricciones inesperadas en la interfaz de usuario que requieran mejoras significativas en el diseño.

 

 