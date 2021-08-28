---
description: Unicode es un estándar mundial de codificación de caracteres. El sistema usa Unicode exclusivamente para la manipulación de caracteres y cadenas. Para obtener una descripción detallada de todos los aspectos de Unicode, consulte El estándar Unicode.
ms.assetid: ca5bcdee-ea13-4745-a565-5426c462892d
title: Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c99a7af4d4fbb6b7783f97ceba37b1bf6b0bf54811beaf9c7c2348ec0125c73b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764775"
---
# <a name="unicode"></a>Unicode

Unicode es un estándar mundial de codificación de caracteres. El sistema usa Unicode exclusivamente para la manipulación de caracteres y cadenas. Para obtener una descripción detallada de todos los aspectos de Unicode, consulte [El estándar Unicode](https://www.unicode.org/standard/standard.html).

En comparación con los mecanismos anteriores para controlar los datos de caracteres y cadenas, Unicode simplifica la localización de software y mejora el procesamiento de texto multilingüe. Al usar Unicode para representar datos de caracteres y cadenas en las aplicaciones, puede habilitar las funcionalidades de intercambio de datos universales para el marketing global, mediante un único archivo binario para cada código de caracteres posible. Unicode hace lo siguiente:

-   Permite que cualquier combinación de caracteres, dibujada a partir de cualquier combinación de scripts e idiomas, coexista en un único documento.
-   Define la semántica de cada carácter.
-   Estandariza el comportamiento del script.
-   Proporciona un algoritmo estándar para el texto bidireccional.
-   Define asignaciones cruzadas a otros estándares.
-   Define varias codificaciones de su único juego de caracteres: UTF-7, UTF-8, UTF-16 y UTF-32. La conversión de datos entre estas codificaciones no tiene pérdidas.

Unicode admite numerosos scripts usados por lenguajes de todo el mundo, así como un gran número de símbolos técnicos y caracteres especiales que se usan en la publicación. Los scripts admitidos incluyen, entre otros, latín, griego, cirílico, hebreo, árabe, devalino, tailandés, han, hangul, hiragana y katakana. Los idiomas admitidos incluyen, entre otros, alemán, francés, inglés, griego, ruso, hebreo, árabe, hindi, tailandés, chino, coreano y japonés. Unicode actualmente puede representar la gran mayoría de los caracteres en el uso de equipos modernos en todo el mundo y se sigue actualizando para que sea aún más completo.

Las funciones habilitadas para Unicode se describen [en Convenciones para prototipos de función](conventions-for-function-prototypes.md). Estas funciones usan la codificación UTF-16 (caracteres anchos), que es la codificación más común de Unicode y la que se usa para la codificación Unicode nativa en Windows sistemas operativos. Cada valor de código tiene 16 bits [](code-pages.md) de ancho, a diferencia del enfoque anterior de la página de códigos para los datos de caracteres y cadenas, que usa valores de código de 8 bits. El uso de 16 bits permite la codificación directa de 65 536 caracteres. De hecho, el universo de símbolos usados para transcribir idiomas humanos es incluso mayor que eso, y los puntos de código UTF-16 del intervalo U+D800 a U+DFFF se usan para formar pares suplentes, que constituyen codificaciones de 32 bits de caracteres adicionales. Consulte [Suplentes y caracteres adicionales para](surrogates-and-supplementary-characters.md) obtener más información.

El juego de caracteres Unicode incluye numerosos caracteres combinados, como U+0308 ("ö"), una diéresis o umlaut combinados. Unicode a menudo puede representar el mismo glifo en un formato "'composed' o ''descomposed'": por ejemplo, la forma compuesta de "º" es el único punto de código Unicode "º" (U+00C4), mientras que su forma descompuesta es "A" + " conversiones" (U+0041 U+0308). Unicode no define un formulario compuesto para cada glifo. Por ejemplo, la "o" minúscula de La infiel con circunflejo y tilde ("ỗ") se representa mediante U+006f U+0302 U+0303 (o + Circunflejo + Tilde). Para obtener más información sobre la combinación de caracteres y problemas relacionados, vea [Using Unicode Normalization to Represent Strings](using-unicode-normalization-to-represent-strings.md).

Para la compatibilidad con entornos de 8 y 7 bits, Unicode también se puede codificar como UTF-8 y UTF-7, respectivamente. Aunque las funciones habilitadas para Unicode en Windows usan UTF-16, también es posible trabajar con datos codificados en UTF-8 o UTF-7, que se admiten en Windows como páginas de códigos de juego de caracteres multibyte [.](code-pages.md)

Las Windows nuevas deben usar UTF-16 como representación de datos interna. Windows también proporciona una amplia compatibilidad con las páginas de códigos y es posible el uso mixto en la misma aplicación. Incluso las nuevas aplicaciones basadas en Unicode a veces tienen que trabajar con páginas de códigos. Las razones para ello se explican en [Páginas de códigos](code-pages.md).

Una aplicación puede usar las funciones [**MultiByteToWideChar**](/windows/win32/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) para convertir entre cadenas basadas en páginas de códigos y cadenas Unicode. Aunque sus nombres hacen referencia a "MultiByte", estas funciones funcionan igual de bien con páginas de códigos de juego de caracteres de un solo byte [](single-byte-character-sets.md) (SBCS), [](double-byte-character-sets.md) juego de caracteres de doble byte (DBCS) y juego de caracteres multibyte (MBCS).

Normalmente, una Windows aplicación debe usar UTF-16 internamente y convertir solo como parte de una "capa fina" sobre la interfaz que debe usar otro formato. Esta técnica se defenderá contra la pérdida y los daños de los datos. Cada página de códigos admite caracteres diferentes, pero ninguno de ellos admite el espectro completo de caracteres proporcionado por Unicode. La mayoría de las páginas de códigos admiten subconjuntos diferentes, codificados de forma diferente. Las páginas de códigos para UTF-8 y UTF-7 son una excepción, ya que admiten el juego de caracteres Unicode completo y la conversión entre estas codificaciones y UTF-16 no tiene pérdidas.

Los datos convertidos directamente de la codificación utilizada por una página de códigos a la codificación utilizada por otra están sujetos a daños, ya que el mismo valor de datos en páginas de códigos diferentes puede codificar un carácter diferente. Incluso cuando la aplicación se convierte lo más cerca posible de la interfaz, debe pensar detenidamente en el intervalo de datos que se va a controlar.

Los datos convertidos de Unicode a una página de códigos están sujetos a pérdida de datos, porque es posible que una página de códigos determinada no pueda representar todos los caracteres usados en los datos Unicode concretos. Por lo tanto, tenga en [**cuenta que WideCharToMultiByte**](/windows/win32/api/Stringapiset/nf-stringapiset-widechartomultibyte) podría perder algunos datos si la página de códigos de destino no puede representar todos los caracteres de la cadena Unicode.

Al modernizar aplicaciones heredadas basadas en páginas de códigos para usar Unicode, puede usar funciones genéricas y la macro [**TEXT**](/windows/win32/api/Winnt/nf-winnt-text) para mantener un único conjunto de orígenes a partir del cual compilar dos versiones de la aplicación. Una versión admite Unicode y la otra funciona con Windows páginas de códigos. Con este mecanismo, puede convertir incluso aplicaciones muy grandes de páginas de códigos de Windows Windows Unicode al tiempo que mantiene orígenes de aplicación que se pueden compilar, compilar y probar en todas las fases de la conversión. Para obtener más información, vea [Convenciones para prototipos de función.](conventions-for-function-prototypes.md)

Los caracteres Unicode y las cadenas usan tipos de datos distintos de los de las cadenas y los caracteres basados en páginas de códigos. Junto con una serie de macros y convenciones de nomenclatura, esta distinción minimiza la posibilidad de mezclar accidentalmente los dos tipos de datos de caracteres. Facilita la comprobación de tipos del compilador para asegurarse de que solo se usan valores de parámetros Unicode con funciones que esperan cadenas Unicode.

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

 

 



