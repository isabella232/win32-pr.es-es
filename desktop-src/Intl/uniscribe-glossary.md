---
description: Un ancho ABC es un valor compuesto definido por una estructura ABC de GDI. La estructura contiene los miembros abcA, abcB y abcC, correspondientes al &\# 0034; Un&\# 0034;, &\# 0034; B&\# 0034; y &\# 0034; C&\# 0034; anchos de un glifo o ejecución.
ms.assetid: 48c766e5-a69d-47d2-a885-f24b80e910d8
title: Glosario de Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808ff2e9620810fe2ec344a037437e6ce8d62bff9460a53cf7b777cedc9d46b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146981"
---
# <a name="uniscribe-glossary"></a>Glosario de Uniscribe

Un ancho ABC es un valor compuesto definido por una estructura ABC de [**GDI.**](/windows/win32/api/wingdi/ns-wingdi-abc) La estructura contiene los miembros **abcA,** **abcB** y **abcC**, correspondientes a los anchos "A", "B" y "C" de un [glifo](#glyph) o [ejecute](#run).

El ancho "A" es inferior [(positivo;](#underhang) también conocido como "relleno") o sobresalte [(negativo)](#overhang) a la izquierda del equivalente en pantalla de la entrada de lápiz que representa el glifo o la ejecución. El ancho "B" es el ancho negro, el ancho desde la entrada de lápiz situada más a la izquierda hasta la entrada de lápiz situada más a la derecha. El ancho de "C" se sobresalga a la derecha de la entrada de lápiz.

En la ilustración siguiente se muestra una F en minúscula cursiva con sobresalto a la izquierda y a la derecha. Es decir, los anchos "A" y "C" aquí son negativos. Consulte [subsalte](#underhang) para obtener una ilustración de los anchos positivos "A" y "C".

![ilustración en la que se muestra una F en minúscula cursiva con sobresalto a la izquierda y a la derecha.](images/abcwidth.gif)

Cuando se muestran dos o más glifos como una unidad, normalmente solo el glifo situado más a la izquierda contribuye al ancho "A" de la ejecución y solo el glifo situado más a la derecha contribuye al ancho "C" de la ejecución. Sin embargo, no se trata de una regla estricta. Por ejemplo, si el primer glifo de una ejecución es una letra estrecha y el segundo glifo es una marca diacrítica ancha y se controlan como glifos independientes, la marca diacrítica podría extenderse más allá de la letra.

## <a name="abc-width"></a>Ancho de ABC

Un ancho ABC es un valor compuesto definido por una estructura ABC de [**GDI.**](/windows/win32/api/wingdi/ns-wingdi-abc) La estructura contiene los miembros **abcA,** **abcB** y **abcC**, correspondientes a los anchos "A", "B" y "C" de un [glifo](#glyph) o [ejecute](#run).

El ancho "A" es inferior [(positivo;](#underhang) también conocido como "relleno") o sobresalte [(negativo)](#overhang) a la izquierda del equivalente en pantalla de la entrada de lápiz que representa el glifo o la ejecución. El ancho "B" es el ancho negro, el ancho desde la entrada de lápiz situada más a la izquierda hasta la entrada de lápiz situada más a la derecha. El ancho de "C" se sobresalga a la derecha de la entrada de lápiz.

En la ilustración siguiente se muestra una F en minúscula cursiva con sobresalto a la izquierda y a la derecha. Es decir, los anchos "A" y "C" aquí son negativos. Consulte [subsalte](#underhang) para obtener una ilustración de los anchos positivos "A" y "C".

![ilustración en la que se muestra una F en minúscula cursiva con sobresalto a la izquierda y a la derecha.](images/abcwidth.gif)

Cuando se muestran dos o más glifos como una unidad, normalmente solo el glifo situado más a la izquierda contribuye al ancho "A" de la ejecución y solo el glifo situado más a la derecha contribuye al ancho "C" de la ejecución. Sin embargo, no se trata de una regla estricta. Por ejemplo, si el primer glifo de una ejecución es una letra estrecha y el segundo glifo es una marca diacrítica ancha y se controlan como glifos independientes, la marca diacrítica podría extenderse más allá de la letra.

## <a name="advance-width"></a>ancho de avance

El ancho de avance de un [glifo](#glyph) es el movimiento en la dirección de escritura desde el punto inicial para representar ese glifo en el punto inicial para representar el glifo siguiente.

## <a name="bidirectional-stack"></a>pila bidireccional

La pila bidireccional es un entero de 5 bits que realiza un seguimiento de los niveles de anidamiento entre texto de izquierda a derecha y de derecha a izquierda. Siempre comienza en cero para de izquierda a derecha. Por lo tanto, todos los valores numerados uniformemente representan texto de izquierda a derecha y todos los valores impares representan texto de derecha a izquierda. La pila bidireccional se representa en el **miembro uBidiLevel** de una [**estructura SCRIPT \_ STATE.**](/windows/win32/api/usp10/ns-usp10-script_state)

## <a name="bidirectional-text"></a>texto bidireccional

El texto bidireccional contiene partes de izquierda a derecha y de derecha a izquierda, pero el término también se aplica a veces de forma flexible al texto puro de derecha a izquierda. Todo el texto de derecha a izquierda requiere el uso [](#embedding-level) de la pila bidireccional [,](#bidirectional-stack)ya que el nivel de incrustación predeterminado de cero implica texto de izquierda a derecha.

## <a name="cell-width"></a>ancho de celda

Una aplicación puede justificar que el texto se ajuste a una línea ajustando el ancho de celda para determinados glifos. En el caso del texto injustificado, el ancho de celda de un glifo es el mismo que el [ancho de avance.](#advance-width)

## <a name="cluster"></a>cluster

Un clúster es la unidad lingüística más pequeña que se puede configurar. En idiomas como el árabe y muchos de los idiomas indic, los glifos usados para representar cada carácter (punto de código Unicode) dependen en gran medida de los puntos de código circundantes, que constituyen el clúster. En estos lenguajes, las aplicaciones pueden traducir puntos de código en glifos adecuados solo si se mira el clúster. En algunos scripts, como Devagli, el orden de los glifos dentro de un clúster puede diferir del orden de los puntos de código Unicode correspondientes. Para obtener más información, [vea Windows de glifos en](/typography/develop/processing-part1) el sitio de tipografía de Microsoft.

## <a name="complex-script"></a>script complejo

Un script complejo es un [script](#complex-script) con cualquiera de las siguientes propiedades:

-   Permite la representación bidireccional.
-   Tiene forma contextual.
-   Tiene caracteres combinados.
-   Tiene reglas especializadas de separación de palabras y justificación.
-   Filtra las combinaciones de caracteres no válidas.
-   No se admite en el núcleo de Windows y, por lo tanto, puede requerir la [reserva de fuentes](#font-fallback).

En algunos scripts complejos, el orden de los glifos podría ser bastante diferente del orden de los caracteres Unicode subyacentes que representan. Consulte [Acerca de los scripts complejos](about-complex-scripts.md) para obtener más detalles.

> [!Note]  
> En el contexto de la tipografía, a veces es conveniente controlar el script latino que se usa para escribir inglés como un script complejo. Algunos ejemplos son la característica Alternativas estilísticas descrita en la documentación de [**OPENTYPE \_ FEATURE \_ RECORD**](/windows/desktop/api/Usp10/ns-usp10-opentype_feature_record)o ligaduras, como "fi", donde un único glifo representa dos o más caracteres consecutivos.

 

## <a name="embedding-level"></a>nivel de inserción

En [texto bidireccional,](#bidirectional-text)el nivel de inserción es el índice de la [pila bidireccional.](#bidirectional-stack)

## <a name="font-fallback"></a>reserva de fuentes

La reserva de fuentes es una selección automatizada de una fuente que no sea la fuente seleccionada por el usuario en una aplicación. En Uniscribe, la función [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) aplica la reserva de fuentes cuando todo o parte del texto está en un script que la fuente seleccionada por el usuario no admite.

## <a name="glyph"></a>glifo

Un glifo es una sola unidad de presentación en una fuente. Para OpenType, esta unidad se define mediante un esquema. Para otros tipos de fuentes, se puede definir mediante un mapa de bits, un conjunto de comandos gráficos y elementos parecidos. Un glifo no se corresponde necesariamente con un solo carácter. Por ejemplo, la ligadura "fi" ("fi") representa los dos caracteres "f" e "i". La "o" minúscula "o" con circunflejo y tilde ("ỗ") normalmente se compone de varios glifos.

## <a name="item"></a>item

Un elemento tiene un [único script y](#complex-script) dirección. La [**función ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) [**o ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) puede analizar un párrafo en elementos. Un elemento no es necesariamente una [ejecución](#run). Puede contener caracteres de varios estilos. La información de elementos y ejecución debe combinarse para determinar [los intervalos](#range).

## <a name="lrm"></a>Lrm

LRM indica la marca de izquierda a derecha (punto de código Unicode U+200E). Esta marca especifica que los caracteres que lo sigue en orden lógico se deben representar de izquierda a derecha.

## <a name="ltr"></a>LTR

LTR indica de izquierda a derecha.

## <a name="range"></a>range

Un intervalo es un caso especial de una [ejecución](#run). Se encuentra completamente dentro de un [elemento](#item). Por lo tanto, si un elemento se divide en ejecuciones, cada una de esas ejecuciones es un intervalo.

## <a name="rlm"></a>Rlm

RLM indica la MARCA DE DERECHA A IZQUIERDA (punto de código Unicode U+200F). Esta marca indica que los caracteres que lo sigue en orden lógico se deben representar de derecha a izquierda.

## <a name="rtl"></a>RTL

RTL indica de derecha a izquierda.

## <a name="run"></a>Ejecutar

Una ejecución es un fragmento de texto para que Uniscribe se represente. Debe tener un estilo único, es decir, fuente, tamaño y color, pero se puede dibujar a partir de una variedad de [scripts](#complex-script). Una ejecución puede contener contenido de izquierda a derecha y de derecha a izquierda.

## <a name="nads"></a>Nads

NADS indica NATIONAL DIGIT SHAPES (punto de código Unicode U+206E). El término especifica que los dígitos europeos (U+0030 a U+0039) se deben representar como dígitos nacionales. Consulte [Formas de dígitos](digit-shapes.md) para obtener más información sobre los dígitos nacionales.

## <a name="nods"></a>Cabecea

NODS indica FORMAS DE DÍGITO NOMINAL (punto de código Unicode U+206F). El término especifica que los dígitos europeos (U+0030 a U+0039) se deben representar normalmente, no como dígitos nacionales.

## <a name="overhang"></a>Proyección

El sobresalte es la parte de la entrada de lápiz de un glifo que se extiende más allá del [ancho de avance](#advance-width) del glifo. La mayoría de los glifos (como "H") no tienen sobresalga, ya que hay un poco de espacio en blanco a cada lado para separarlos de los glifos adyacentes. Un ejemplo de glifo con sobresalto es la cursiva "f" usada en este tema para ilustrar el [ancho de ABC.](#abc-width) La parte superior e inferior de la cursiva "f" sobresalga sobre los glifos adyacentes. El sobresalte corresponde a un ancho "A" o "C" negativo.

## <a name="padding"></a>relleno

Vea [unders(subsalte).](#underhang)

## <a name="script"></a>script

Un script es un sistema de lenguaje escrito, por ejemplo, script latino, script árabe o chino. Un solo script se puede aplicar a uno o varios idiomas humanos. El script no tiene ninguna relación concreta con una fuente. Por ejemplo, el script latino se puede representar igualmente bien con la fuente Times New Roman o Arial.

## <a name="underhang"></a>subsalte

El subdesón es un ancho de espacio en blanco a la izquierda o derecha de la parte sólida de un glifo. El subsalado corresponde a un ancho positivo "A" o "C", como se describe para [el ancho abc.](#abc-width) El subsalte se conoce a veces como "relleno". En la ilustración siguiente se muestra el subsambre de la letra minúscula n.

![ilustración en la que se muestra el subsalte de la letra minúscula n.](images/underhang.gif)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 
