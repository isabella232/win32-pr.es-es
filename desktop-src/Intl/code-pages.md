---
description: La mayoría de las aplicaciones escritas actualmente controlan los datos de caracteres principalmente como Unicode, con la codificación UTF-16.
ms.assetid: 866f09f4-629e-4097-a974-fbda9389d077
title: Páginas de códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28528ba13e3db3f0c72dd7c071eb8b7886ab003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687625"
---
# <a name="code-pages"></a>Páginas de códigos

La mayoría de las aplicaciones escritas actualmente controlan los datos de caracteres principalmente como [Unicode](unicode.md), con la codificación UTF-16. Sin embargo, muchas aplicaciones heredadas continúan usando juegos de caracteres basados en páginas de códigos. Incluso las aplicaciones nuevas a veces tienen que trabajar con páginas de códigos, a menudo por una de las razones siguientes:

-   Para comunicarse con aplicaciones heredadas.
-   Para comunicarse con los servidores de correo y noticias más antiguos, que podrían no ser siempre compatibles con Unicode.
-   Para comunicarse con la consola de Windows.

> [!Note]  
> Las nuevas aplicaciones de Windows deben usar [Unicode](unicode.md) para evitar las incoherencias de las distintas páginas de códigos y para facilitar la localización.

 

Cada página de códigos se representa mediante un identificador de página de códigos, por ejemplo, 1252, y se controla mediante las funciones de la API de juegos de caracteres y Unicode. Para obtener una lista de identificadores de páginas de códigos compatibles, vea [identificadores de páginas de códigos](code-page-identifiers.md). La referencia de "páginas de códigos" del [Centro para desarrolladores de Microsoft go global](https://msdn.microsoft.com/goglobal) proporciona descripciones completas de muchas páginas de códigos.

Las páginas de códigos de Windows, que normalmente se denominan "páginas de códigos ANSI", son páginas de códigos para las que los valores no ASCII (valores mayores que 127) representan caracteres internacionales. Estas páginas de códigos se usan de forma nativa en Windows me y también están disponibles en Windows NT y versiones posteriores.

> [!Note]  
> Originalmente, la página de códigos 1252 de Windows, la página de códigos usada normalmente para inglés y otros idiomas de Europa occidental, se basaba en un borrador de American National Standards Institute (ANSI). Dicho borrador se ha convertido en ISO 8859-1, pero la página de códigos de Windows 1252 se ha implementado antes de que el estándar se convirtiera en final y no es exactamente igual que ISO 8859-1.

 

Muchas funciones de la API de Windows tienen versiones "A" (ANSI) y "W" (ancho, Unicode). La versión "A" controla el texto en función de las páginas de códigos de Windows, mientras que la versión "W" controla el texto Unicode. Vea [tipos de datos de Windows para obtener cadenas](windows-data-types-for-strings.md) y [convenciones para prototipos de función](conventions-for-function-prototypes.md).

Las páginas de códigos de Windows también se conocen a veces como "páginas de códigos activas" o "páginas de códigos activas del sistema". Un sistema operativo Windows siempre tiene una página de códigos de Windows activa actualmente. Todas [las versiones ANSI de las funciones de API](conventions-for-function-prototypes.md) usan la página de códigos activa actualmente.

Las páginas de códigos del fabricante de equipos originales (OEM) son páginas de códigos para las que los valores no ASCII representan caracteres de dibujo de línea y de puntuación. Estas páginas de códigos se usaban originalmente para MS-DOS y todavía se usan para las aplicaciones de consola. También se usan para los nombres de archivo no extendidos en los sistemas de archivos FAT12, FAT16 y FAT32, tal y como se describe en juegos de caracteres que se [usan en los nombres de archivo](character-sets-used-in-file-names.md). La página de códigos OEM habitual para inglés es la página de códigos 437.

En las páginas de códigos de Windows y las páginas de códigos OEM, los valores de código de 0x00 a 0x7F se corresponden con el juego de caracteres ASCII de 7 bits. Los valores de código 0x00 a través de 0x19 y 0x7F siempre representan caracteres de control normalizados y 0x20 a 0x7E representan caracteres que se van a mostrar normalizados. Los caracteres representados por los códigos restantes, 0x80 a 0xFF, varían entre los juegos de caracteres. Cada juego de caracteres incluye diferentes caracteres especiales, normalmente personalizados para un idioma o un grupo de idiomas. La página de códigos 1252 de Windows y la página de códigos OEM 437 se utilizan generalmente en el Estados Unidos.

Además de las páginas de códigos de Windows y OEM, las aplicaciones pueden usar páginas de códigos no nativas. Algunos ejemplos son las páginas de códigos EBCDIC y Macintosh.

Dos codificaciones de Unicode (UTF-7 y UTF-8) se implementan como páginas de códigos. Al igual que otras páginas de códigos, cada página se conoce mediante un identificador numérico y se puede controlar con muchas de las mismas funciones de la API de juegos de caracteres y Unicode.

Las páginas de códigos pueden ser páginas [de juego de caracteres de un solo byte](single-byte-character-sets.md) (SBCS) o [de juego de caracteres de doble byte](double-byte-character-sets.md) (DBCS). En las páginas de SBCS, cada byte codifica directamente un solo carácter, para que sea posible representar exactamente 256 caracteres distintos (incluidos caracteres de control, letras, dígitos, signos de puntuación, símbolos y similares). Las páginas de códigos DBCS se usan para idiomas como el japonés y el chino. En esta página de códigos, algunos caracteres tienen codificaciones de dos bytes con determinados valores de byte (valores siempre mayores que 127) que sirven como "bytes iniciales". En lugar de codificar los caracteres en su propio derecho, los bytes iniciales se pueden asignar a un carácter solo junto con un "byte final".

Algunos protocolos heredados requieren el uso de páginas de códigos SBCS y DBCS. Cada página de códigos SBCS/DBCS admite distintos caracteres, pero ninguna página de códigos admite toda la amplitud de caracteres proporcionados por Unicode. Cada página de códigos SBCS/DBCS admite un subconjunto diferente, codificado de forma diferente.

> [!Note]  
> Los datos convertidos de una página de códigos SBCS o DBCS a otra están sujetos a daños, ya que el mismo valor de datos en páginas de códigos diferentes puede codificar un carácter diferente. Los datos convertidos de Unicode a SBCS o DBCS están sujetos a pérdida de datos, ya que es posible que una página de códigos determinada no pueda representar todos los caracteres utilizados en esos datos Unicode concretos.

 

Además de las páginas de códigos SBCS y DBCS, las aplicaciones tienen disponibles las páginas de códigos 52936, 54936, 51949 y 5022x del juego de caracteres multibyte, que usan un enfoque similar al de un DBCS. Sin embargo, una página de códigos del juego de caracteres multibyte va más allá de las codificaciones de dos bytes de algunos caracteres. UTF-7 y UTF-8 usan un enfoque similar para codificar Unicode basado en bytes de 7 y 8 bits, respectivamente. Para obtener más información, consulte [Unicode](unicode.md).

Varias funciones de juego de caracteres y Unicode permiten a las aplicaciones controlar las páginas de códigos. Una aplicación puede usar las funciones [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) y [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) para obtener información sobre una página de códigos. Esta información incluye el carácter predeterminado que se usa cuando un carácter de una cadena convertida no tiene ninguna entrada correspondiente en la página de códigos.

Una aplicación puede usar las funciones [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para realizar la conversión entre cadenas basadas en páginas de códigos de Windows y cadenas Unicode. Aunque sus nombres hacen referencia a "multibyte", estas funciones funcionan igual de bien con las páginas de códigos de juego de caracteres de varios bytes y SBCS.

> [!Note]  
> [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) puede perder algunos datos si la página de códigos proporcionada no puede representar todos los caracteres de una cadena Unicode.

 

La aplicación puede convertir entre páginas de códigos de Windows y páginas de códigos OEM mediante las funciones de la biblioteca en tiempo de ejecución estándar de C. Sin embargo, el uso de estas funciones presenta un riesgo de pérdida de datos porque los caracteres que se pueden representar en cada página de códigos no coinciden exactamente.

Las aplicaciones también pueden llamar a la función [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) . Esta función recupera el identificador de la página de códigos de Windows (ANSI) actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Juegos de caracteres](character-sets.md)
</dt> </dl>

 

 



