---
description: Las API de InkAnalysis proporcionan a los desarrolladores de Tablet PC herramientas eficaces para examinar mediante programación la entrada manuscrita. La API clasifica la entrada manuscrita en categorías significativas como palabras, líneas, párrafos y dibujos.
ms.assetid: d9521a8c-f61a-40ea-8603-e8afbba75a4e
title: Información general de análisis de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e383d16c01cd9475d4c54587b4b5fb4c09791a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540438"
---
# <a name="ink-analysis-overview"></a>Información general de análisis de tinta

Las API de InkAnalysis proporcionan a los desarrolladores de Tablet PC herramientas eficaces para examinar mediante programación la entrada manuscrita. La API clasifica la entrada manuscrita en categorías significativas como palabras, líneas, párrafos y dibujos.

Puede usar cada clasificación de varias maneras, incluida la mejora de los resultados de reconocimiento de escritura a mano.

## <a name="ink-analysis-basics"></a>Aspectos básicos del análisis de tinta

En esta sección se presenta la tecnología de análisis de tinta de la plataforma de Tablet PC y se explica cuándo y cómo utilizarla.

Las API de InkAnalysis combinan eficazmente dos tecnologías distintas pero gratuitas: reconocimiento de escritura a mano y clasificación de diseño. La combinación de estas dos tecnologías proporciona resultados más definitivos que las partes tomadas por sí sola.

El reconocimiento de escritura a mano es el análisis computacional de la tinta digital manuscrita para devolver la interpretación basada en caracteres en un idioma determinado. Es decir, el reconocimiento de escritura a mano es el modo en que el equipo "Lee" la escritura a mano de una persona.

El análisis de tinta se puede desglosar aún más en el análisis de diseño y clasificación de tinta. La clasificación de tinta es la división computacional de la entrada manuscrita en unidades semánticamente significativas como párrafos, líneas, palabras y dibujos. El análisis de diseño es el examen computacional de la entrada manuscrita para determinar la posición de la tinta en la superficie de entrada manuscrita y cómo se relacionan los trazos entre sí espacialmente e incluso semánticamente. Por ejemplo, el análisis de diseño puede indicar que una parte de la tinta determinada es una anotación o una llamada.

### <a name="recognition"></a>Reconocimiento

Un ejemplo de cómo la combinación de reconocimiento con el análisis de tinta en la API InkAnalysis ayuda al desarrollador a mejorar el reconocimiento de los resultados. Los motores de reconocimiento de escritura a mano de Tablet PC se han diseñado principalmente para reconocer una única línea horizontal de tinta. Sin embargo, las personas tienden a escribir varias líneas al tomar notas y no se garantiza que esas líneas sean horizontales respecto a la página. Con la API InkAnalysis, el analizador de tinta preprocesa la entrada de lápiz antes de enviarla al reconocedor. La tinta analizada se transforma a horizontal antes de que se reconozca, mejorando los resultados del reconocimiento.

Otras ventajas del reconocimiento se derivan al hacer que el analizador de tinta corrija la información de orden de trazos incorrecta antes de enviar la tinta al reconocedor. Además, los resultados de reconocimiento ahora están disponibles de manera selectiva. Es decir, el desarrollador puede recuperar rápidamente los resultados de reconocimiento para una sola palabra, línea o párrafo en una llamada.

### <a name="ink-classification"></a>Clasificación de tinta

Por supuesto, hay una serie de escenarios en los que puede mantener intactos los datos de tinta, en lugar de convertirlos inmediatamente en texto. El análisis de tinta proporciona también beneficios aquí. En concreto, las API de InkAnalysis proporcionan la capacidad de dividir trazos de tinta en función de si están escribiendo o dibujando dibujos. Los trazos de lápiz que se clasifican como escritura son los que componen una palabra o caracteres. Todos los demás trazos son dibujos. Esto le proporciona una nueva manera de tener acceso a los datos de tinta, lo que permite nuevos escenarios de usuario. Por ejemplo, puede implementar la selección para que sea diferente en función del tipo de trazo que el usuario pulse. Si un usuario pulsa un trazo de escritura, la aplicación selecciona el conjunto completo de trazos que componen la palabra, si el usuario pulsa un dibujo Stoke, la aplicación selecciona solo ese trazo.

### <a name="layout-analysis"></a>Análisis de diseño

En realidad, un análisis de diseño útil va más allá del desglose relativamente simple de la entrada de lápiz en componentes de escritura y dibujo.

El análisis de tinta también incluye un desglose más completo de los trazos de escritura y dibujo. Como ejemplo muy sencillo, tome un BLOB de tinta como se muestra en la siguiente ilustración.

![dos líneas simples de escritura a mano](images/12e7a221-59c1-4d69-b7aa-67f2caebe375.jpg)

Una vez que la plataforma ha analizado estos trazos, devuelve una representación en árbol de estos trazos, tal y como se muestra en la siguiente ilustración. En este caso simple, el árbol solo contiene información de párrafo, línea y palabra, pero la riqueza de este árbol aumenta a medida que aumenta la complejidad del documento de tinta.

![representación de árbol de raíz, párrafo, líneas y palabras](images/be5a7635-0abc-45ad-bcb5-98fddee5e148.jpg)

Dado que esta información está ahora separada en unidades administrables, ahora puede crear características más eficaces. Por ejemplo, la aplicación puede extender la característica en la que el usuario puntea para seleccionar una palabra en una característica en la que el usuario pulsa una vez para seleccionar la palabra, se puntea dos veces para seleccionar la línea completa y se pulsa tres veces para seleccionar todo el párrafo. Al aprovechar la estructura de árbol devuelta por la operación de análisis, la aplicación puede relacionar el área punteada de nuevo con un trazo en el árbol. Una vez que la aplicación encuentra un trazo, puede recorrer el árbol para determinar cómo y qué trazos vecinos seleccionar.

La selección de una línea completa es un ejemplo simplista de las ventajas del análisis de tinta, pero las posibilidades son excelentes cuando uno tiene en cuenta los diferentes tipos de estructuras jerárquicas que el analizador de tinta es capaz de detectar:

-   Listas ordenadas y no ordenadas
-   Formas
-   Comentarios anotativos escritos en línea con el texto

Los tipos de características varían de una aplicación a una aplicación y se basan en los requisitos y en los motores de análisis y reconocimiento de tinta disponibles.

### <a name="key-ink-analysis-features"></a>Características de análisis de tinta de claves

Las funcionalidades clave de la API de InkAnalysis incluyen las siguientes características:

-   Análisis incremental
-   Persistencia
-   Proxy de datos
-   Conciliación
-   Extensibilidad

### <a name="incremental-analysis"></a>Análisis incremental

Cuando los usuarios finales trabajan con tinta, normalmente lo tratan como escritura a mano. La tinta está continuamente sujeta a operaciones de edición como la adición de nueva tinta, la eliminación de la tinta existente y la modificación de las propiedades de entrada manuscrita, todo ello de la misma forma que la escritura a mano se edita continuamente. Estas operaciones de edición afectan a los resultados del análisis. Cuando se producen modificaciones, normalmente se pueden aislar en secciones del documento en momentos concretos. Por ejemplo, supongamos que un usuario escribe cinco líneas de tinta. La manera estándar en que las aplicaciones analizan la tinta es esperar hasta que el usuario haya terminado de escribir las cinco líneas de tinta (un párrafo, por ejemplo) y, a continuación, analizar los resultados, ya sea de forma sincrónica o asincrónica.

Puede optimizar el tiempo total empleado en el análisis de estas cinco líneas al aislar las áreas que se analizan a medida que se escriben y, a continuación, volver a analizar solo las partes de los resultados que han cambiado. Una vez analizada la primera línea, nunca se reconocerá de nuevo a menos que la modifique el usuario final. El reconocimiento de la segunda línea se trata como una operación de reconocimiento independiente.

Este enfoque incremental funciona bien en el nivel de línea para las operaciones de reconocimiento, pero debe funcionar en un nivel superior para la operación de análisis de tinta. Dado que el analizador de tintas puede detectar distintas clasificaciones de nivel superior para estas cinco líneas de tinta (por ejemplo, podría ser un párrafo estándar o cinco elementos de una lista), el enfoque incremental para el analizador de tinta es que tiene que analizar estas estructuras más altas. Es decir, después de que el analizador de tintas clasifique la primera línea de entrada de lápiz como una línea, comprueba que sigue siendo una línea cuando clasifica la segunda línea. Sin embargo, el analizador de tintas aísla esta doble comprobación en el párrafo y omite el primer párrafo al analizar un segundo párrafo, tratando el segundo párrafo como una operación independiente del analizador de tinta. Este enfoque incremental para el análisis ahorra drásticamente tiempo de procesamiento cuando ya existen grandes cantidades de tinta en la aplicación.

### <a name="persistence"></a>Persistencia

El análisis incremental funciona bien dentro de una sesión o instancia determinada de un objeto [**InkAnalyzer**](inkanalyzer.md) . Sin embargo, la primera generación de API de la plataforma de Tablet PC no puede realizar un análisis incremental después de que la tinta se conserve en el disco. La API de InkAnalysis permite guardar la entrada manuscrita en el disco junto con un formulario guardado de los resultados del análisis. Los resultados del análisis se pueden cargar cuando la tinta se carga y se puede insertar en una nueva instancia de un **InkAnalyzer**. Una nueva instancia del objeto **InkAnalyzer** tiene el mismo estado de resultados que tenía anteriormente y ahora puede aceptar cualquier modificación como cambios incrementales en el estado existente, en lugar de analizar todo de nuevo.

### <a name="data-proxy"></a>Proxy de datos

Muchas aplicaciones ya tienen algún tipo de estructura de documento existente en sus aplicaciones. por ejemplo, un grafo o una base de datos. [**InkAnalyzer**](inkanalyzer.md) también presenta los resultados en un formato estructurado, en un árbol de objetos [**ContextNode**](icontextnode.md) . La estructura **InkAnalyzer** y la estructura existente de la aplicación deben interoperar en dos direcciones: los resultados se extraen de la **InkAnalyzer** a la aplicación y el estado se inserta desde la aplicación en el **InkAnalyzer**.

Si se extraen los resultados de [**InkAnalyzer**](inkanalyzer.md) en la estructura de la aplicación, sería relativamente sencillo. Las aplicaciones iterarán en el árbol de resultados y copiarán (integrarán) todos los elementos de los resultados que necesiten en la estructura de datos existente. Sin embargo, dado que muchas aplicaciones horizontales requieren análisis incremental y persistencia en el disco, el problema se vuelve bidireccional. El estado (resultados anteriores) debe extraerse de la estructura de la aplicación e insertarse en el **InkAnalyzer**.

Para cumplir este requisito, el [**InkAnalyzer**](inkanalyzer.md) contiene una serie de eventos que genera en el momento adecuado durante una operación de análisis para permitir que las aplicaciones representen la solicitud de datos de vuelta a sus estructuras existentes. Estos eventos solo se generan para los objetos [**ContextNode**](icontextnode.md) que requiere la operación incremental.

### <a name="reconciliation"></a>Conciliación

La mayoría de las aplicaciones querrán analizar la tinta en segundo plano para mantener al mínimo las interrupciones de la interfaz de usuario. El análisis de la tinta en segundo plano causa problemas, sin embargo, si el usuario cambia la tinta (o la tinta adyacente) que se está analizando. Por ejemplo, si el usuario elimina la entrada manuscrita durante la operación en segundo plano, la estructura resultante reflejará el estado del documento cuando se inició la operación en segundo plano, en lugar de cuando se completó.

Para ayudar a las aplicaciones, [**InkAnalyzer**](inkanalyzer.md) concilia las diferencias en el estado del documento entre el principio y el final de la operación de análisis. Los cambios realizados por el usuario o la aplicación mientras el análisis se ejecuta en segundo plano reemplazan siempre los resultados calculados en segundo plano. Después de la conciliación, solo se muestran las partes de la estructura de resultados que no entran en conflicto con los cambios de documento y los trazos en conflicto se etiquetan para un análisis futuro. La próxima vez que se ejecute la operación de análisis en segundo plano, los resultados se volverán a calcular en función del nuevo estado.

En el diagrama siguiente se muestra este proceso. La hora se expresa linealmente de arriba abajo en el diagrama.

![proceso para reconciliar los cambios de estado de documento durante la operación de análisis](images/6323e0b5-b6b3-4adc-8c73-da3fad5b4bc2.jpg)

1.  En el momento 1 (T1), la aplicación está recopilando la tinta del usuario final, incluido cualquier tipo de modificación de la tinta, como agregar, quitar o modificar.
2.  En T2, la aplicación invoca la operación de análisis en segundo plano. El [**InkAnalyzer**](inkanalyzer.md) determina qué tinta no tiene resultados y qué tinta se debe comprobar doble. Copia los datos de tinta necesarios para permitir que el subproceso en segundo plano se ejecute de forma independiente.
3.  En T3, [**InkAnalyzer**](inkanalyzer.md) devuelve la ejecución del subproceso de la interfaz de usuario a la aplicación. **InkAnalyzer** crea un segundo subproceso, el subproceso de análisis en segundo plano y los motores de análisis y reconocimiento de tinta, y analiza los datos de tinta copiados.
4.  Mientras la operación de análisis se está produciendo en el segundo subproceso en segundo plano, el usuario final continúa editando el documento, agregando y quitando los datos de trazo, en T4 y T5. Estas modificaciones pueden entrar en conflicto con el trabajo que se está procesando en segundo plano.
5.  En T6, el subproceso en segundo plano ha finalizado la operación de análisis y los resultados están listos. Antes de que [**InkAnalyzer**](inkanalyzer.md) comunique los resultados a la aplicación, ejecuta un algoritmo de conciliación para determinar si las modificaciones realizadas por el usuario mientras se calculaba la operación de análisis (T4 y T5) entran en conflicto con los resultados. Si se detectan conflictos, los trazos en conflicto se marcan para su reanálisis, que se produce la próxima vez que la aplicación invoca la operación de análisis en segundo plano.
6.  Por último, en T7, con todas las colisiones detectadas, [**InkAnalyzer**](inkanalyzer.md) presenta los resultados a la aplicación.

### <a name="extensibility"></a>Extensibilidad

Las API de InkAnalysis permiten que las aplicaciones usen nuevos tipos de motores de análisis, de forma que la aplicación no tenga que volver a escribir todas las ventajas de la API de InkAnalysis, incluida la reconciliación, el proxy de datos, la persistencia y el análisis incremental.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft. Ink](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 
