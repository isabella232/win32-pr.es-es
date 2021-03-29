---
description: Un ancho ABC es un valor compuesto definido por una estructura ABC de GDI. La estructura contiene los miembros abcA, abcB y abcC, correspondientes al &\# 0034; Un&\# 0034;, &\# 0034; B&\# 0034; y &\# 0034; C&\# 0034; anchos de un glifo o ejecutar.
ms.assetid: 48c766e5-a69d-47d2-a885-f24b80e910d8
title: Glosario de Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e154e65c103ce6e4287ac8aa2e76e0be4206f9fd
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104359503"
---
# <a name="uniscribe-glossary"></a>Glosario de Uniscribe

Un ancho ABC es un valor compuesto definido por una estructura [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) de GDI. La estructura contiene los miembros **abcA**, **abcB** y **abcC**, correspondientes a los anchos "A", "B" y "C" de un [glifo](#glyph) o de una [ejecución](#run).

El ancho "A" está [desbloqueado](#underhang) (positivo; también conocido como "relleno") o [saliente](#overhang) (negativo) a la izquierda del equivalente en pantalla de la entrada de lápiz que representa el glifo o la ejecución. El ancho "B" es el ancho negro, el ancho desde la entrada de lápiz izquierda hasta la derecha. El ancho "C" está sobresaliente a la derecha de la tinta.

En la ilustración siguiente se muestra una letra F minúscula en cursiva con el saliente hacia la izquierda y la derecha. Es decir, los anchos "A" y "C" aquí son negativos. Vea [subbloqueos](#underhang) para ver una ilustración de los anchos "A" y "C" positivos.

![Ilustración en la que se muestra una letra F minúscula en cursiva con el saliente hacia la izquierda y la derecha.](images/abcwidth.gif)

Cuando dos o más glifos se muestran como una unidad, normalmente solo el glifo izquierdo contribuye al ancho "A" de la ejecución y solo el glifo más a la derecha contribuye al ancho "C" de la ejecución. Sin embargo, no se trata de una regla estricta. Por ejemplo, si el primer glifo de una ejecución es una letra estrecha y el segundo glifo es una marca diacrítica ancha y se administran como glifos independientes, la marca diacrítica podría extenderse más allá de la letra.

## <a name="abc-width"></a>Ancho ABC

Un ancho ABC es un valor compuesto definido por una estructura [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) de GDI. La estructura contiene los miembros **abcA**, **abcB** y **abcC**, correspondientes a los anchos "A", "B" y "C" de un [glifo](#glyph) o de una [ejecución](#run).

El ancho "A" está [desbloqueado](#underhang) (positivo; también conocido como "relleno") o [saliente](#overhang) (negativo) a la izquierda del equivalente en pantalla de la entrada de lápiz que representa el glifo o la ejecución. El ancho "B" es el ancho negro, el ancho desde la entrada de lápiz izquierda hasta la derecha. El ancho "C" está sobresaliente a la derecha de la tinta.

En la ilustración siguiente se muestra una letra F minúscula en cursiva con el saliente hacia la izquierda y la derecha. Es decir, los anchos "A" y "C" aquí son negativos. Vea [subbloqueos](#underhang) para ver una ilustración de los anchos "A" y "C" positivos.

![Ilustración en la que se muestra una letra F minúscula en cursiva con el saliente hacia la izquierda y la derecha.](images/abcwidth.gif)

Cuando dos o más glifos se muestran como una unidad, normalmente solo el glifo izquierdo contribuye al ancho "A" de la ejecución y solo el glifo más a la derecha contribuye al ancho "C" de la ejecución. Sin embargo, no se trata de una regla estricta. Por ejemplo, si el primer glifo de una ejecución es una letra estrecha y el segundo glifo es una marca diacrítica ancha y se administran como glifos independientes, la marca diacrítica podría extenderse más allá de la letra.

## <a name="advance-width"></a>ancho avanzado

El ancho de avance de un [glifo](#glyph) es el movimiento en la dirección de escritura desde el punto inicial para representar ese glifo hasta el punto inicial para representar el siguiente glifo.

## <a name="bidirectional-stack"></a>pila bidireccional

La pila bidireccional es un entero de 5 bits que realiza un seguimiento de los niveles de anidamiento entre el texto de izquierda a derecha y de derecha a izquierda. Siempre comienza en cero para de izquierda a derecha. Por lo tanto, todos los valores con números pares representan el texto de izquierda a derecha y todos los valores impares representan el texto de derecha a izquierda. La pila bidireccional se representa en el miembro **uBidiLevel** de una estructura de [**\_ Estado de script**](/windows/win32/api/usp10/ns-usp10-script_state) .

## <a name="bidirectional-text"></a>texto bidireccional

El texto bidireccional contiene partes de izquierda a derecha y de derecha a izquierda, pero el término también se aplica a veces de forma flexible a texto puro de derecha a izquierda. Todo el texto de derecha a izquierda requiere el uso de la [pila bidireccional](#bidirectional-stack), ya que el [nivel de incrustación](#embedding-level) predeterminado de cero implica el texto de izquierda a derecha.

## <a name="cell-width"></a>ancho de celda

Una aplicación puede justificar que el texto se ajuste a una línea ajustando el ancho de la celda para determinados glifos. En el caso de texto no justificado, el ancho de celda de un glifo es el mismo que el [ancho de avance](#advance-width).

## <a name="cluster"></a>cluster

Un clúster es la unidad lingüística más pequeña A la que se puede dar forma. En lenguajes como el árabe y muchos de los idiomas indios, los glifos utilizados para representar cada carácter (punto de código Unicode) dependen firmemente de los puntos de código circundantes, que constituyen el clúster. En estos lenguajes, las aplicaciones pueden traducir los puntos de código en los glifos correspondientes solo examinando el clúster. En algunos scripts, como Devanagari, el orden de los glifos dentro de un clúster puede diferir del orden de los puntos de código Unicode correspondientes. Para obtener más información, vea [procesamiento de glifos de Windows](/typography/develop/processing-part1) en el sitio de tipografía de Microsoft.

## <a name="complex-script"></a>script complejo

Un script complejo es un [script](#complex-script) con cualquiera de las siguientes propiedades:

-   Permite la representación bidireccional.
-   Tiene el modelado contextual.
-   Combina caracteres.
-   Tiene reglas de separación de palabras y justificación especializadas.
-   Filtra las combinaciones de caracteres no válidas.
-   No se admite en las fuentes principales de Windows y, por tanto, podría requerir la [reserva de fuentes](#font-fallback).

En algunos scripts complejos, el orden de los glifos puede ser bastante diferente del orden de los caracteres Unicode subyacentes que representan. Consulte [acerca de los scripts complejos](about-complex-scripts.md) para obtener más detalles.

> [!Note]  
> En el contexto de tipografía, a veces es conveniente controlar el script Latino que se usa para escribir en inglés como un script complejo. Entre los ejemplos se incluye la característica de alternativas estilísticas que se describe en la documentación del [**\_ \_ registro de la característica OPENTYPE**](/windows/desktop/api/Usp10/ns-usp10-opentype_feature_record), o ligaduras, como "fi", donde un solo glifo representa dos o más caracteres consecutivos.

 

## <a name="embedding-level"></a>nivel de incrustación

En [texto bidireccional](#bidirectional-text), el nivel de incrustación es el índice de la [pila bidireccional](#bidirectional-stack).

## <a name="font-fallback"></a>Reserva de fuentes

La reserva de fuentes es una selección automática de una fuente distinta de la fuente seleccionada por el usuario en una aplicación. En Uniscribe, la función [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) aplica la reserva de fuentes cuando todo o parte del texto está en un script que no admite la fuente seleccionada por el usuario.

## <a name="glyph"></a>glifo

Un glifo es una unidad única de presentación en una fuente. En el caso de OpenType, esta unidad se define mediante un esquema. Para otros tipos de fuentes, se puede definir mediante un mapa de bits, un conjunto de comandos gráficos y similares. Un glifo no se corresponde necesariamente con un solo carácter. Por ejemplo, la ligadura "fi" ("fi") representa los dos caracteres "f" y "i". La "o" minúsculas vietnamitas con acento circunflejo y tilde ("ỗ") normalmente se compone de varios glifos.

## <a name="item"></a>item

Un elemento tiene un único [script](#complex-script) y una dirección. La función [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) o [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) puede analizar un párrafo en elementos. Un elemento no es necesariamente una [ejecución](#run). Puede contener caracteres de varios estilos. El elemento y la información de ejecución deben combinarse para determinar los [intervalos](#range).

## <a name="lrm"></a>LRM

LRM indica la marca de izquierda a derecha (punto de código Unicode U + 200E). Esta marca especifica que los caracteres que lo siguen en orden lógico deben representarse de izquierda a derecha.

## <a name="ltr"></a>LTR

LTR indica de izquierda a derecha.

## <a name="range"></a>range

Un intervalo es un caso especial de una [ejecución](#run). Está completamente dentro de un [elemento](#item). Por lo tanto, si un elemento se divide en ejecuciones, cada una de esas ejecuciones es un intervalo.

## <a name="rlm"></a>RLM

RLM indica la marca de derecha a izquierda (punto de código Unicode U + 200F). Esta marca indica que los caracteres que lo siguen en orden lógico deben representarse de derecha a izquierda.

## <a name="rtl"></a>RTL

RTL indica de derecha a izquierda.

## <a name="run"></a>Ejecutar

Una ejecución es un paso del texto que se va a representar en Uniscribe. Debe tener un estilo único, es decir, fuente, tamaño y color, pero se puede extraer de diversos [scripts](#complex-script). Una ejecución puede contener tanto el contenido de izquierda a derecha como el de derecha a izquierda.

## <a name="nads"></a>NADS

NADS indica las formas de dígitos nacionales (punto de código Unicode U + 206E. El término especifica que los dígitos europeos (U + 0030 a U + 0039) deben representarse como dígitos nacionales. Consulte [formas de dígitos](digit-shapes.md) para obtener más información sobre los dígitos nacionales.

## <a name="nods"></a>NODOS

NODOS indica las formas de dígitos nominales (punto de código Unicode U + 206F). El término especifica que los dígitos europeos (U + 0030 a U + 0039) deben representarse normalmente, no como dígitos nacionales.

## <a name="overhang"></a>sobresale

El voladizo es la parte de la entrada de lápiz de un glifo que se extiende más allá del [ancho de avance](#advance-width) del glifo. La mayoría de los glifos (como "H") no tienen ningún voladizo, ya que hay un poco de espacio en blanco en cada lado para separarlos de los glifos adyacentes. Un ejemplo de un glifo con voladizo es el "f" en cursiva que se usa en este tema para ilustrar el [ancho ABC](#abc-width). La parte superior e inferior de la "f" en cursiva sobresale de los glifos adyacentes. Voladizo corresponde a un ancho negativo "A" o "C".

## <a name="padding"></a>relleno

Vea [subbloqueos](#underhang).

## <a name="script"></a>script

Un script es un sistema de lenguaje escrito, por ejemplo, alfabeto latino, script árabe, script chino. Un solo script puede aplicarse a uno o varios idiomas. El script no tiene ninguna relación determinada con una fuente. Por ejemplo, el script Latino se puede representar igualmente bien con las horas New Roman o Arial.

## <a name="underhang"></a>subbloqueos

El subbloqueo es un ancho de espacio en blanco a la izquierda o a la derecha de la parte sólida de un glifo. Los subbloqueos se corresponden con un ancho positivo "A" o "C", como se describe en el [ancho ABC](#abc-width). El bloqueo de subbloqueos a veces se conoce como "relleno". En la ilustración siguiente se muestra el bloqueo de la letra n minúscula.

![Ilustración en la que se muestra el subbloqueo de la letra n minúscula.](images/underhang.gif)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 
