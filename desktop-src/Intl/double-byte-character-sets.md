---
description: Un juego de caracteres de doble byte (DBCS), también conocido como &0034;juego de caracteres de 8 bits expandido \#&0034;, es un juego extendido de caracteres de un solo byte (SBCS), implementado como una página de \# códigos.
ms.assetid: df049d22-02e2-48b2-8b74-52f71c00c549
title: Juegos de caracteres de doble byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbef827b91c5ed2468b06f759883c0ba0b874e74038871227aabe0f65f1a046
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147668"
---
# <a name="double-byte-character-sets"></a>Juegos de caracteres de doble byte

Un juego de caracteres de doble byte (DBCS), también conocido como "juego [](single-byte-character-sets.md) de caracteres expandido de 8 bits", es un juego extendido de caracteres de un solo byte (SBCS), implementado como una página de códigos. Los DBCS se desarrollaron originalmente para ampliar el diseño de SBCS para controlar idiomas como japonés y chino. Algunos caracteres de un DBCS, incluidos los dígitos y las letras usados para escribir inglés, tienen valores de código de un solo byte. Otros caracteres, como ideogramas de chino o kanji japonés, tienen valores de código de doble byte. Un DBCS puede corresponder a una página de códigos Windows o a una página de códigos OEM. Una página de códigos DBCS también puede incluir una página de códigos no nativa, por ejemplo, una página de códigos EBCDIC. Para obtener definiciones de estas páginas de códigos, vea [Páginas de códigos](code-pages.md).

> [!Note]  
> Las Windows nuevas deben usar [Unicode](unicode.md) para evitar las incoherencias de páginas de códigos variadas y facilitar la localización. Sin embargo, algunos protocolos heredados pueden requerir el uso de páginas de códigos DBCS. Cada página de códigos DBCS admite caracteres diferentes, pero ninguna página admite toda la amplitud de caracteres proporcionada por Unicode. Cada página de códigos DBCS admite un subconjunto diferente, codificado de forma diferente. Los datos convertidos de una página de códigos DBCS a otra están sujetos a daños porque el mismo valor de datos en páginas de códigos diferentes puede codificar un carácter diferente. Los datos convertidos de Unicode a DBCS están sujetos a pérdida de datos, porque es posible que una página de códigos determinada no pueda representar todos los caracteres usados en los datos Unicode concretos.

 

Para interpretar una cadena DBCS, una aplicación debe comenzar al principio de la cadena y examinar hacia delante. Realiza un seguimiento cuando encuentra un byte inicial en la cadena y trata el byte siguiente como la parte final del mismo carácter. Si la aplicación simplemente examina la cadena byte a byte y encuentra un byte que parece ser el valor de código que representa una barra diagonal inversa (" "), ese byte podría ser simplemente el byte final de un carácter de dos \\ bytes. La aplicación no puede hacer una copia de seguridad de un byte para ver si el byte anterior es un byte inicial, ya que ese valor de byte podría ser apto para usarse como byte inicial y como byte final. Por lo tanto, la aplicación tiene básicamente el mismo problema que con la posible barra diagonal inversa. En otras palabras, las búsquedas de subcadenas son mucho más complicadas con un DBCS que con SBCSs o Unicode. En consecuencia, las aplicaciones que admiten DBCS deben usar funciones especiales, como [ \_ mbsstr](/cpp/c-runtime-library/reference/strstr-wcsstr-mbsstr-mbsstr-l), en lugar de [**la función StrStr.**](https://msdn.microsoft.com/library/z9da80kz(v=VS.71).aspx)

Las aplicaciones usan DBCS Windows páginas de códigos con las versiones "A" de Windows funciones. Vea [Convenciones para prototipos de función y](conventions-for-function-prototypes.md) páginas de [códigos.](code-pages.md) Para ayudar a identificar una página de códigos DBCS, una aplicación puede usar la [**función GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) o [**GetCPInfoEx.**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) Una aplicación puede usar la función [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte) para determinar si se puede usar un valor determinado como byte inicial de un carácter de 2 bytes. Además, una aplicación puede usar las funciones [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para asignar entre cadenas Unicode y DBCS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Juegos de caracteres](character-sets.md)
</dt> <dt>

[Juegos de caracteres de un solo byte](single-byte-character-sets.md)
</dt> </dl>

 

 
