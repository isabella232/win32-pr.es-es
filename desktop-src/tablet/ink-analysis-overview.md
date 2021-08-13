---
description: Las API InkAnalysis proporcionan a los desarrolladores de Tabletas PC herramientas eficaces para examinar mediante programación la entrada de lápiz. La API clasifica la entrada de lápiz en categorías significativas, como palabras, líneas, párrafos y dibujos.
ms.assetid: d9521a8c-f61a-40ea-8603-e8afbba75a4e
title: Información general sobre análisis de entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3056a5e5fbff8be82f6df2de2a34fadd9761e50f451ee2d48c112589d1aff397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718923"
---
# <a name="ink-analysis-overview"></a>Información general sobre análisis de entrada de lápiz

Las API InkAnalysis proporcionan a los desarrolladores de Tabletas PC herramientas eficaces para examinar mediante programación la entrada de lápiz. La API clasifica la entrada de lápiz en categorías significativas, como palabras, líneas, párrafos y dibujos.

Puede usar cada clasificación de varias maneras, incluida la mejora de los resultados de reconocimiento para la escritura a mano.

## <a name="ink-analysis-basics"></a>Conceptos básicos del análisis de entrada de lápiz

En esta sección se presenta la tecnología de análisis de lápiz de tablet PC Platform y se explica cuándo y cómo usarla.

Las API InkAnalysis combinan eficazmente dos tecnologías distintas pero gratuitas: reconocimiento de escritura a mano y clasificación de diseño. La combinación de estas dos tecnologías proporciona resultados definitivamente mayores que las partes tomadas por sí solas.

El reconocimiento de escritura a mano es el análisis computacional de la entrada manuscrita digital para devolver la interpretación basada en caracteres en un idioma determinado. Es decir, el reconocimiento de escritura a mano es la forma en que el equipo "lee" la escritura a mano de una persona.

Análisis de entrada de lápiz se puede dividir aún más en la clasificación de entrada de lápiz y el análisis de diseño. La clasificación de lápiz es la división computacional de la entrada de lápiz en unidades semánticamente significativas, como párrafos, líneas, palabras y dibujos. El análisis de diseño es el examen computacional de la entrada de lápiz para determinar la posición de la entrada de lápiz en la superficie de entrada manuscrita y cómo se relacionan los trazos entre sí espacial e incluso semánticamente. Por ejemplo, el análisis de diseño puede avisarle de que un fragmento de lápiz determinado es una anotación o una llamada.

### <a name="recognition"></a>Reconocimiento

Un ejemplo de cómo la combinación de reconocimiento con análisis de lápiz en InkAnalysis API ayuda al desarrollador es la mejora en los resultados del reconocimiento. Los motores de reconocimiento de escritura a mano de Tablet PC se han diseñado principalmente para reconocer una sola línea horizontal de lápiz. Sin embargo, las personas tienden a escribir varias líneas al tomar notas y no se garantiza que esas líneas sean horizontales en relación con la página. Con InkAnalysis API, el analizador de lápiz preprocesa la entrada de lápiz antes de enviarse al reconocedor. La entrada de lápiz analizada se transforma en horizontal antes de ser reconocida, lo que mejora los resultados del reconocimiento.

Otras ventajas del reconocimiento se derivan de que el analizador de lápiz corrija la información de orden de trazo incorrecta antes de enviar la entrada de lápiz al reconocedor. Además, los resultados del reconocimiento ahora están disponibles de forma selectiva. Es decir, el desarrollador puede recuperar rápidamente los resultados del reconocimiento de una sola palabra, línea o párrafo en una sola llamada.

### <a name="ink-classification"></a>Clasificación de entrada de lápiz

Por supuesto, hay una variedad de escenarios en los que puede mantener intactos los datos de entrada de lápiz, en lugar de convertirlos inmediatamente en texto. El análisis de lápiz también proporciona ventajas aquí. En concreto, las API InkAnalysis proporcionan la capacidad de dividir trazos de lápiz en función de si están escribiendo o dibujando. Los trazos de lápiz que se clasifican como escritura son aquellos que compone una palabra o caracteres. Todos los demás trazos son dibujos. Esto proporciona una nueva manera de acceder a los datos de entrada de lápiz, lo que permite nuevos escenarios de usuario. Por ejemplo, puede implementar la selección para que sea diferente en función del tipo de trazo que pulse el usuario. Si un usuario pulsa un trazo de escritura, la aplicación selecciona todo el conjunto de trazos que componen la palabra; si el usuario pulsa un dibujo, la aplicación selecciona solo ese trazo.

### <a name="layout-analysis"></a>Análisis de diseño

En realidad, el análisis de diseño útil va mucho más allá del desglose relativamente sencillo de la entrada de lápiz en los componentes de escritura y dibujo.

El análisis de lápiz también incluye un desglose más completo de los trazos de escritura y dibujo. Como ejemplo muy sencillo, tome un blob de lápiz como se muestra en la ilustración siguiente.

![dos líneas sencillas de escritura a mano](images/12e7a221-59c1-4d69-b7aa-67f2caebe375.jpg)

Una vez que la plataforma ha analizado estos trazos, devuelve una representación de árbol de estos trazos, como se muestra en la ilustración siguiente. En este caso sencillo, el árbol solo contiene información de párrafo, línea y palabra, pero la complejidad de este árbol aumenta a medida que aumenta la complejidad del documento de entrada manuscrita.

![representación de árbol de raíz, párrafo, líneas y palabras](images/be5a7635-0abc-45ad-bcb5-98fddee5e148.jpg)

Dado que esta información ahora está separada en unidades administrables, ahora puede crear características más eficaces. Por ejemplo, la aplicación puede ampliar la característica en la que el usuario pulsa para seleccionar una palabra en una característica en la que el usuario pulsa una vez para seleccionar la palabra, pulsa dos veces para seleccionar toda la línea y pulsa tres veces para seleccionar todo el párrafo. Al aprovechar la estructura de árbol devuelta por la operación de análisis, la aplicación puede relacionar el área pulsada con un trazo del árbol. Una vez que la aplicación encuentra un trazo, puede recorrer el árbol para determinar cómo y qué trazos vecinos se seleccionan.

Seleccionar una línea completa es un ejemplo simplista de las ventajas del análisis de entrada de lápiz, pero las posibilidades se vuelven excelentes cuando se tienen en cuenta los diferentes tipos de estructuras jerárquicas que el analizador de lápiz es capaz de detectar:

-   Listas ordenadas y desordenadas
-   Formas
-   Comentarios anotativos escritos en línea con el texto

Los tipos de características varían de una aplicación a otra y se basan en los requisitos y los motores de reconocimiento y análisis de entrada de lápiz disponibles.

### <a name="key-ink-analysis-features"></a>Características clave del análisis de entrada de lápiz

Las principales funcionalidades de inkAnalysis API incluyen las siguientes características:

-   Análisis incremental
-   Persistencia
-   Proxy de datos
-   Reconciliación
-   Extensibilidad

### <a name="incremental-analysis"></a>Análisis incremental

Cuando los usuarios finales trabajan con lápiz, normalmente lo tratan como escritura a mano. La entrada de lápiz está sujeta continuamente a operaciones de edición, como la adición de nueva entrada de lápiz, la eliminación de la entrada de lápiz existente y la modificación de las propiedades de la entrada de lápiz, todo ello de la misma manera que la escritura a mano se edita continuamente. Estas operaciones de edición afectan a los resultados del análisis. Cuando se producen modificaciones, normalmente se pueden aislar en secciones del documento en momentos específicos en el tiempo. Por ejemplo, suponga que un usuario escribe cinco líneas de lápiz. La manera estándar que las aplicaciones analizan la entrada de lápiz es esperar hasta que el usuario haya terminado de escribir las cinco líneas de lápiz (un párrafo, por ejemplo) y, a continuación, analizar los resultados, ya sea de forma sincrónica o asincrónica.

Puede optimizar el tiempo total dedicado a analizar estas cinco líneas mediante el aislamiento de las áreas que se analizan a medida que se escriben y, a continuación, volver a analizar solo las partes de los resultados que han cambiado. Una vez analizada la primera línea, nunca se volverá a reconocer a menos que el usuario final la modifique. El reconocimiento de la segunda línea se trata como una operación de reconocimiento independiente.

Este enfoque incremental funciona bien en el nivel de línea para las operaciones de reconocimiento, pero debe funcionar en un nivel superior para la operación de análisis de entrada de lápiz. Dado que el analizador de entrada de lápiz puede detectar diferentes clasificaciones de nivel superior para estas cinco líneas de entrada de lápiz (por ejemplo, podría ser un párrafo estándar o cinco elementos de una lista), el enfoque incremental del analizador de lápiz es que tiene que analizar estas estructuras superiores. Es decir, después de que el analizador de entrada de lápiz clasifica la primera línea de lápiz como una línea, comprueba que sigue siendo una línea cuando clasifica la segunda línea. Sin embargo, el analizador de entrada de lápiz aísla esta comprobación doble en el párrafo y omite el primer párrafo al analizar un segundo párrafo, tratando el segundo párrafo como una operación independiente del analizador de lápiz. Este enfoque incremental para el análisis ahorra drásticamente tiempo de procesamiento cuando ya existen grandes cantidades de lápiz en la aplicación.

### <a name="persistence"></a>Persistencia

El análisis incremental funciona bien dentro de una sesión o instancia determinada de un [**objeto InkAnalyzer.**](inkanalyzer.md) Sin embargo, las API de la plataforma de tablet PC de primera generación no pueden realizar análisis incrementales después de que la entrada de lápiz se conserve en el disco. InkAnalysis API permite guardar la entrada de lápiz en el disco junto con una forma persistente de los resultados del análisis. Los resultados del análisis se pueden cargar cuando se carga la entrada de lápiz y se pueden insertar en una nueva instancia de **inkAnalyzer.** A continuación, una nueva instancia del objeto **InkAnalyzer** tiene el mismo estado de resultados que tenía anteriormente y ahora puede aceptar cualquier modificación como cambios incrementales en el estado existente, en lugar de analizar todo de nuevo.

### <a name="data-proxy"></a>Proxy de datos

Muchas aplicaciones ya tienen algún tipo de estructura de documentos existente en sus aplicaciones. por ejemplo, un gráfico o una base de datos. [**InkAnalyzer**](inkanalyzer.md) también presenta los resultados en forma estructurada, en un árbol de [**objetos ContextNode.**](icontextnode.md) La **estructura InkAnalyzer** y la estructura existente de la aplicación deben interoperar en dos direcciones: los resultados se extraen de **InkAnalyzer** en la aplicación y el estado se inserta desde la aplicación en **InkAnalyzer.**

Si lo único que se necesita fuera extraer los resultados de [**InkAnalyzer**](inkanalyzer.md) en la estructura de la aplicación, sería relativamente sencillo. Las aplicaciones iteran por el árbol de resultados y copian (integran) todos los elementos de los resultados que necesitan en su estructura de datos existente. Sin embargo, dado que muchas aplicaciones horizontales requieren análisis incremental y persistencia en el disco, el problema se vuelve bidireccional. El estado (resultados pasados) debe sacarse de la estructura de la aplicación e insertarse en **InkAnalyzer**.

Para cumplir este requisito, [**InkAnalyzer**](inkanalyzer.md) contiene una serie de eventos que genera en el momento adecuado durante una operación de análisis para permitir que las aplicaciones puedan devolver la solicitud de datos a sus estructuras existentes. Estos eventos solo se genera para los [**objetos ContextNode**](icontextnode.md) requeridos por la operación incremental.

### <a name="reconciliation"></a>Reconciliación

La mayoría de las aplicaciones querrán analizar la entrada de lápiz en segundo plano para mantener al mínimo las interrupciones de la interfaz de usuario. Sin embargo, el análisis de la entrada de lápiz en segundo plano provoca problemas si el usuario cambia la entrada de lápiz (o la entrada de lápiz vecino) que se está analizando. Por ejemplo, si el usuario elimina la entrada de lápiz durante la operación en segundo plano, la estructura resultante reflejaría el estado del documento cuando se inició la operación en segundo plano, en lugar de cuando se completó.

Para ayudar a las aplicaciones, [**InkAnalyzer concilia**](inkanalyzer.md) las diferencias en el estado del documento entre el principio y el final de la operación de análisis. Los cambios realizados por el usuario o la aplicación mientras el análisis se ejecuta en segundo plano siempre invalidan los resultados calculados en segundo plano. Después de la conciliación, solo se notifican las partes de la estructura de resultados que no están en conflicto con los cambios del documento y los trazos en conflicto se etiquetan para su análisis futuro. La próxima vez que se ejecute la operación de análisis en segundo plano, los resultados se volverán a calcular en función del nuevo estado.

En el diagrama siguiente se muestra este proceso. El tiempo se expresa linealmente de arriba abajo en el diagrama.

![proceso para conciliar los cambios de estado del documento durante la operación de análisis](images/6323e0b5-b6b3-4adc-8c73-da3fad5b4bc2.jpg)

1.  En el momento 1 (t1), la aplicación recopila la entrada de lápiz del usuario final, incluido cualquier tipo de modificación de la entrada de lápiz, como agregar, quitar o modificar.
2.  En t2, la aplicación invoca la operación de análisis en segundo plano. [**InkAnalyzer determina**](inkanalyzer.md) qué entrada de lápiz no tiene resultados y qué lápiz debe comprobarse. Copia los datos de entrada de lápiz necesarios para permitir que el subproceso en segundo plano se ejecute de forma independiente.
3.  En t3, [**InkAnalyzer devuelve**](inkanalyzer.md) la ejecución del subproceso de interfaz de usuario a la aplicación. **InkAnalyzer** crea un segundo subproceso, el subproceso de análisis de fondo y los motores de reconocimiento y análisis de entrada de lápiz analizan los datos de entrada de lápiz copiados.
4.  Mientras la operación de análisis se produce en el segundo subproceso en segundo plano, el usuario final continúa editando el documento, agregando y quitando datos de trazo, en t4 y t5. Estas modificaciones pueden estar en conflicto con el trabajo que se está procesando en segundo plano.
5.  En t6, el subproceso en segundo plano ha finalizado la operación de análisis y los resultados están listos. Antes de que [**InkAnalyzer**](inkanalyzer.md) comunique los resultados a la aplicación, ejecuta un algoritmo de conciliación para determinar si las modificaciones realizadas por el usuario mientras se calculaba la operación de análisis (t4 y t5) entra en conflicto con los resultados. Si se detecta alguna colisión, los trazos de colisión se marcan para volver a analizar, lo que se produce la próxima vez que la aplicación invoca la operación de análisis en segundo plano.
6.  Por último, en t7, con todas las colisiones detectadas, [**InkAnalyzer**](inkanalyzer.md) presenta los resultados a la aplicación.

### <a name="extensibility"></a>Extensibilidad

Las API InkAnalysis permiten que las aplicaciones utilicen nuevos tipos de motores de análisis, de forma que la aplicación no tenga que volver a escribir todas las ventajas de inkAnalysis API, incluida la conciliación, el proxy de datos, la persistencia y el análisis incremental.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft.Ink](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 
