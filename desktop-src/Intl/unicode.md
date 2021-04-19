---
description: Unicode es un estándar de codificación de caracteres en todo el mundo. El sistema utiliza Unicode exclusivamente para la manipulación de caracteres y cadenas. Para obtener una descripción detallada de todos los aspectos de Unicode, consulte el estándar Unicode.
ms.assetid: ca5bcdee-ea13-4745-a565-5426c462892d
title: Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88facae63fbb365fd6f38cb09464de735e0759b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688707"
---
# <a name="unicode"></a>Unicode

Unicode es un estándar de codificación de caracteres en todo el mundo. El sistema utiliza Unicode exclusivamente para la manipulación de caracteres y cadenas. Para obtener una descripción detallada de todos los aspectos de Unicode, consulte [el estándar Unicode](https://www.unicode.org/standard/standard.html).

En comparación con los mecanismos más antiguos para administrar datos de caracteres y cadenas, Unicode simplifica la localización de software y mejora el procesamiento de texto multilingüe. Mediante el uso de Unicode para representar los datos de caracteres y cadenas en las aplicaciones, puede habilitar las capacidades de intercambio de datos universal para marketing global mediante un solo archivo binario para cada código de carácter posible. Unicode hace lo siguiente:

-   Permite que una combinación de caracteres, dibujada a partir de cualquier combinación de scripts y lenguajes, coexista en un solo documento.
-   Define la semántica de cada carácter.
-   Normaliza el comportamiento del script.
-   Proporciona un algoritmo estándar para texto bidireccional.
-   Define las asignaciones cruzadas a otros estándares.
-   Define varias codificaciones de su único juego de caracteres: UTF-7, UTF-8, UTF-16 y UTF-32. La conversión de datos entre estas codificaciones es sin pérdida.

Unicode admite numerosos scripts usados por lenguajes de todo el mundo y también un gran número de símbolos técnicos y caracteres especiales que se usan en la publicación. Entre los scripts admitidos se incluyen, entre otros, latín, griego, cirílico, hebreo, Árabe, Devanagari, tailandés, ha, hangul, hiragana y katakana. Entre los idiomas admitidos se incluyen, entre otros, alemán, Francés, Inglés, griego, Ruso, hebreo, Árabe, Hindi, tailandés, Chino, Coreano y japonés. En la actualidad, Unicode puede representar la gran mayoría de los caracteres en el uso de equipos modernos en todo el mundo y continúa actualizándose para que sea aún más completo.

Las funciones habilitadas para Unicode se describen en [convenciones para prototipos de función](conventions-for-function-prototypes.md). Estas funciones utilizan la codificación UTF-16 (caracteres anchos), que es la codificación más común de Unicode y la usada para la codificación Unicode nativa en los sistemas operativos Windows. Cada valor de código tiene un ancho de 16 bits, a diferencia del enfoque de [Página de códigos](code-pages.md) anterior a los datos de caracteres y cadenas, que usa valores de código de 8 bits. El uso de 16 bits permite la codificación directa de 65.536 caracteres. De hecho, el universo de símbolos que se usan para transcribir lenguajes humanos es incluso mayor que eso, y los puntos de código UTF-16 en el intervalo de U + D800 a U + DFFF se usan para formar pares suplentes, que constituyen codificaciones de 32 bits de caracteres adicionales. Vea [suplentes y caracteres adicionales](surrogates-and-supplementary-characters.md) para obtener más información.

El juego de caracteres Unicode incluye numerosos caracteres combinables, como U + 0308 ("̈"), una combinación de diéresis o umlaut. A menudo, Unicode puede representar el mismo glifo en un formulario ' ' compuesto ' ' o un ' descompuesto ' ': por ejemplo, la forma compuesta de "Ä" es el punto de código Unicode "Ä" (U + 00C4), mientras que su forma descompuesta es "A" + "̈" (U + 0041 U + 0308). Unicode no define un formulario compuesto para cada glifo. Por ejemplo, la "o" minúscula vietnamita con acento circunflejo y tilde ("ỗ") se representa mediante U + 006F U + 0302 U + 0303 (o + acento circunflejo + tilde). Para obtener más información sobre la combinación de caracteres y problemas relacionados, vea [usar la normalización Unicode para representar cadenas](using-unicode-normalization-to-represent-strings.md).

Por compatibilidad con entornos de 8 y 7 bits, Unicode también se puede codificar como UTF-8 y UTF-7, respectivamente. Aunque las funciones Unicode habilitadas en Windows usan UTF-16, también es posible trabajar con datos codificados en UTF-8 o UTF-7, que se admiten en Windows como [páginas de códigos](code-pages.md)de juegos de caracteres multibyte.

Las nuevas aplicaciones de Windows deben usar UTF-16 como su representación de datos interna. Windows también proporciona una amplia compatibilidad con las páginas de códigos y se puede usar de forma mixta en la misma aplicación. Incluso las nuevas aplicaciones basadas en Unicode a veces tienen que trabajar con páginas de códigos. Los motivos para ello se describen en [las páginas de códigos](code-pages.md).

Una aplicación puede usar las funciones [**MultiByteToWideChar**](/windows/win32/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) para realizar la conversión entre cadenas basadas en páginas de códigos y cadenas Unicode. Aunque sus nombres hacen referencia a "multibyte", estas funciones funcionan igualmente bien con el [juego de caracteres de un solo byte](single-byte-character-sets.md) (SBCS), [el juego de caracteres de doble byte](double-byte-character-sets.md) (DBCS) y las páginas de códigos del juego de caracteres multibyte (MBCS).

Normalmente, una aplicación de Windows debe usar UTF-16 internamente, convirtiendo solo como parte de una "capa fina" a través de la interfaz que debe usar otro formato. Esta técnica defiende contra la pérdida y el daño de los datos. Cada página de códigos admite distintos caracteres, pero ninguno de ellos admite todo el espectro de caracteres proporcionado por Unicode. La mayoría de las páginas de códigos admiten subconjuntos diferentes, con codificación diferente. Las páginas de códigos de UTF-8 y UTF-7 son una excepción, ya que admiten el juego de caracteres Unicode completo y la conversión entre estas codificaciones y UTF-16 es sin pérdida.

Los datos convertidos directamente desde la codificación utilizada por una página de códigos a la codificación utilizada por otro están sujetos a daños, ya que el mismo valor de datos en páginas de códigos diferentes puede codificar un carácter diferente. Incluso cuando la aplicación se está convirtiendo lo más cerca posible de la interfaz, debe pensar detenidamente en el intervalo de datos que se va a controlar.

Los datos convertidos de Unicode a una página de códigos están sujetos a la pérdida de datos, ya que es posible que una página de códigos determinada no pueda representar todos los caracteres utilizados en esos datos Unicode concretos. Por lo tanto, tenga en cuenta que [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) podría perder algunos datos si la página de códigos de destino no puede representar todos los caracteres de la cadena Unicode.

Al modernizar las aplicaciones heredadas basadas en páginas de códigos para usar Unicode, puede utilizar las funciones genéricas y la macro [**Text**](/windows/win32/api/Winnt/nf-winnt-text) para mantener un único conjunto de orígenes desde el que compilar dos versiones de la aplicación. Una versión admite Unicode y la otra funciona con las páginas de códigos de Windows. Con este mecanismo, puede convertir incluso aplicaciones muy grandes de páginas de códigos de Windows a Unicode a la vez que mantiene los orígenes de la aplicación que se pueden compilar, compilar y probar en todas las fases de la conversión. Para obtener más información, vea [convenciones de los prototipos de función](conventions-for-function-prototypes.md).

Los caracteres Unicode y las cadenas usan tipos de datos que son distintos de los de caracteres y cadenas basados en páginas de códigos. Junto con una serie de macros y convenciones de nomenclatura, esta distinción minimiza la posibilidad de mezclar accidentalmente los dos tipos de datos de caracteres. Facilita la comprobación del tipo de compilador para asegurarse de que solo se usan valores de parámetro Unicode con funciones que esperan cadenas Unicode.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Juegos de caracteres](character-sets.md)
</dt> <dt>

[Ordenación](sorting.md)
</dt> <dt>

[Suplentes y caracteres suplementarios](surrogates-and-supplementary-characters.md)
</dt> <dt>

[Usar la normalización Unicode para representar cadenas](using-unicode-normalization-to-represent-strings.md)
</dt> </dl>

 

 



