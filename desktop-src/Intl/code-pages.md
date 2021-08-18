---
description: La mayoría de las aplicaciones escritas hoy en día controlan los datos de caracteres principalmente como Unicode, mediante la codificación UTF-16.
ms.assetid: 866f09f4-629e-4097-a974-fbda9389d077
title: Páginas de códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad589183bbb64a2feb65079a2322dd148598c6c3542320ec2ce851b9de61cfa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754965"
---
# <a name="code-pages"></a>Páginas de códigos

La mayoría de las aplicaciones escritas hoy en día controlan los datos de caracteres [principalmente como Unicode](unicode.md)mediante la codificación UTF-16. Sin embargo, muchas aplicaciones heredadas siguen usando juegos de caracteres basados en páginas de códigos. Incluso las aplicaciones nuevas a veces tienen que trabajar con páginas de códigos, a menudo por uno de los siguientes motivos:

-   Para comunicarse con aplicaciones heredadas.
-   Para comunicarse con servidores de noticias y correo antiguos, que es posible que no siempre admitan Unicode.
-   Para comunicarse con la consola Windows.

> [!Note]  
> Las Windows nuevas deben usar [Unicode](unicode.md) para evitar las incoherencias de páginas de códigos variadas y facilitar la localización.

 

Cada página de códigos se representa mediante un identificador de página de códigos, por ejemplo, 1252, y se controla mediante las funciones de API Unicode y juego de caracteres. Para obtener una lista de identificadores de página de códigos admitidos, vea [Identificadores de página de códigos](code-page-identifiers.md). La referencia "Páginas de códigos" del Centro para desarrolladores globales de Microsoft [Go](https://msdn.microsoft.com/goglobal) proporciona descripciones completa de muchas páginas de códigos.

Windows páginas de códigos, normalmente denominadas "páginas de códigos ANSI", son páginas de códigos para las que los valores no ASCII (valores mayores que 127) representan caracteres internacionales. Estas páginas de códigos se usan de forma nativa en Windows Me y también están disponibles en Windows NT y versiones posteriores.

> [!Note]  
> Originalmente, Windows página de códigos 1252, la página de códigos que se usaba normalmente para inglés y otros idiomas de Europa Occidental, se basaba en un borrador American National Standards Institute (ANSI). Finalmente, ese borrador se convirtió en ISO 8859-1, pero Windows la página de códigos 1252 se implementó antes de que el estándar se convirtiese en final y no es exactamente lo mismo que iso 8859-1.

 

Muchas Windows API tienen versiones "A" (ANSI) y "W" (wide, Unicode). La versión "A" controla el texto en función Windows páginas de códigos, mientras que la versión "W" controla el texto Unicode. Vea [Windows tipos de datos para cadenas](windows-data-types-for-strings.md) y [convenciones para prototipos de función.](conventions-for-function-prototypes.md)

Windows las páginas de códigos también se conocen como "páginas de códigos activas" o "páginas de códigos activas del sistema". Un Windows operativo siempre tiene una página de códigos Windows activa. Todas [las versiones ANSI de las funciones de API](conventions-for-function-prototypes.md) usan la página de códigos activa actualmente.

Las páginas de códigos del fabricante de equipos originales (OEM) son páginas de códigos para las que los valores no ASCII representan caracteres de puntuación y dibujo de línea. Estas páginas de códigos se usaron originalmente para MS-DOS y se siguen utilizando para las aplicaciones de consola. También se usan para los nombres de archivo no extendidos en los sistemas de archivos FAT12, FAT16 y FAT32, como se describe en Juegos de caracteres usados en nombres de [archivo](character-sets-used-in-file-names.md). La página de códigos oem habitual para inglés es la página de códigos 437.

Para las Windows y las páginas de códigos OEM, los valores de 0x00 a 0x7F corresponden al juego de caracteres ASCII de 7 bits. Los valores de 0x00 a 0x19 y 0x7F representan siempre caracteres de control estandarizados y 0x20 a 0x7E representan caracteres que se pueden mostrar estandarizados. Los caracteres representados por los códigos restantes, 0x80 a 0xff, varían entre los juegos de caracteres. Cada juego de caracteres incluye distintos caracteres especiales, normalmente personalizados para un idioma o grupo de idiomas. Windows página de códigos 1252 y la página de códigos 437 de OEM se usan generalmente en la Estados Unidos.

Además de las Windows y las páginas de códigos OEM, las aplicaciones pueden usar páginas de códigos no nativas. Algunos ejemplos son las páginas de códigos EBCDIC y Macintosh.

Dos codificaciones de Unicode (UTF-7 y UTF-8) se implementan como páginas de códigos. Al igual que otras páginas de códigos, cada página se conoce mediante un identificador numérico y se puede controlar con muchas de las mismas funciones de API unicode y juego de caracteres.

Las páginas de códigos pueden ser [páginas de](single-byte-character-sets.md) juego de caracteres de un solo byte (SBCS) o páginas de juego de caracteres de doble [byte](double-byte-character-sets.md) (DBCS). En las páginas de SBCS, cada byte codifica directamente un solo carácter, por lo que es posible representar exactamente 256 caracteres distintos (incluidos caracteres de control, letras, dígitos, puntuación, símbolos y otros). Las páginas de códigos DBCS se usan para idiomas como japonés y chino. En esta página de códigos, algunos caracteres tienen codificaciones de dos bytes con determinados valores de byte (siempre valores mayores que 127) que sirven como "bytes iniciales". En lugar de codificar caracteres por derecho propio, los bytes iniciales solo se pueden asignar a un carácter junto con un "byte final".

Algunos protocolos heredados requieren el uso de páginas de códigos SBCS y DBCS. Cada página de códigos SBCS/DBCS admite caracteres diferentes, pero ninguna página de códigos admite toda la amplitud de caracteres proporcionada por Unicode. Cada página de códigos SBCS/DBCS admite un subconjunto diferente, codificado de forma diferente.

> [!Note]  
> Los datos convertidos de una página de códigos SBCS o DBCS a otra están sujetos a daños, ya que el mismo valor de datos en páginas de códigos diferentes puede codificar un carácter diferente. Los datos convertidos de Unicode a SBCS o DBCS están sujetos a pérdida de datos, porque es posible que una página de códigos determinada no pueda representar todos los caracteres usados en los datos Unicode concretos.

 

Además de las páginas de códigos SBCS y DBCS, las aplicaciones tienen disponibles las páginas de códigos del juego de caracteres multibyte 52936, 54936, 51949 y 5022x, que usan un enfoque similar al de un DBCS. Sin embargo, una página de códigos de juego de caracteres multibyte va más allá de las codificaciones de dos bytes de algunos caracteres. UTF-7 y UTF-8 usan un enfoque similar para codificar Unicode en función de bytes de 7 y 8 bits, respectivamente. Para obtener más información, vea [Unicode](unicode.md).

Varias funciones Unicode y juego de caracteres permiten a las aplicaciones controlar páginas de códigos. Una aplicación puede usar las [**funciones GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) y [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) para obtener información sobre una página de códigos. Esta información incluye el carácter predeterminado que se usa cuando un carácter de una cadena convertida no tiene ninguna entrada correspondiente en la página de códigos.

Una aplicación puede usar las funciones [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para convertir entre cadenas basadas Windows páginas de códigos y cadenas Unicode. Aunque sus nombres hacen referencia a "MultiByte", estas funciones funcionan igual de bien con las páginas de códigos SBCS, DBCS y juego de caracteres multibyte.

> [!Note]  
> [**WideCharToMultiByte puede**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) perder algunos datos si la página de códigos proporcionada no puede representar todos los caracteres de una cadena Unicode.

 

La aplicación puede convertir entre Windows y páginas de códigos OEM mediante las funciones estándar de la biblioteca en tiempo de ejecución de C. Sin embargo, el uso de estas funciones presenta un riesgo de pérdida de datos porque los caracteres que puede representar cada página de códigos no coinciden exactamente.

Las aplicaciones también pueden llamar a [**la función GetACP.**](/windows/desktop/api/Winnls/nf-winnls-getacp) Esta función recupera el identificador de la página de códigos Windows (ANSI) actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Juegos de caracteres](character-sets.md)
</dt> </dl>

 

 



