---
description: Juego de caracteres de doble byte (DBCS), también conocido como &\# 0034; juego de caracteres de 8 bits expandido&\# 0034;, es un juego de caracteres de byte único extendido (SBCS), implementado como una página de códigos.
ms.assetid: df049d22-02e2-48b2-8b74-52f71c00c549
title: Juegos de caracteres de doble byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 431b762b19f5531644e4bbaace548f34245c9d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688347"
---
# <a name="double-byte-character-sets"></a>Juegos de caracteres de doble byte

Un juego de caracteres de doble byte (DBCS), también conocido como "juego de caracteres de 8 bits expandido", es un [juego de caracteres de un solo byte](single-byte-character-sets.md) extendido (SBCS), implementado como una página de códigos. DBCS se desarrolló originalmente para ampliar el diseño de SBCS para administrar idiomas como el japonés y el chino. Algunos caracteres de un DBCS, incluidos los dígitos y las letras que se usan para escribir en inglés, tienen valores de código de un solo byte. Otros caracteres, como los ideogramas chinos o el kanji japonés, tienen valores de código de doble byte. Un DBCS puede corresponder a una página de códigos de Windows o a una página de códigos OEM. Una página de códigos DBCS también puede incluir una página de códigos no nativa, por ejemplo, una página de códigos EBCDIC. Para ver las definiciones de estas páginas de códigos, vea [páginas de códigos](code-pages.md).

> [!Note]  
> Las nuevas aplicaciones de Windows deben usar [Unicode](unicode.md) para evitar las incoherencias de las distintas páginas de códigos y para facilitar la localización. Sin embargo, algunos protocolos heredados podrían requerir el uso de páginas de códigos DBCS. Cada página de códigos DBCS admite distintos caracteres, pero ninguna página admite toda la amplitud de caracteres proporcionados por Unicode. Cada página de códigos DBCS admite un subconjunto diferente, codificado de forma diferente. Los datos convertidos de una página de códigos DBCS a otra están sujetos a daños porque el mismo valor de datos en páginas de códigos diferentes puede codificar un carácter diferente. Los datos convertidos de Unicode a DBCS están sujetos a pérdida de datos, ya que es posible que una página de códigos determinada no pueda representar todos los caracteres utilizados en esos datos Unicode concretos.

 

Para interpretar una cadena DBCS, una aplicación debe empezar al principio de la cadena y examinar hacia delante. Realiza un seguimiento cuando encuentra un byte inicial en la cadena y trata el siguiente byte como la parte final del mismo carácter. Si la aplicación simplemente examina la cadena de un byte a la vez y encuentra un byte que parece ser el valor de código que representa una barra diagonal inversa (" \\ "), ese byte podría ser simplemente el byte final de un carácter de dos bytes. La aplicación no puede simplemente hacer una copia de seguridad de un byte para ver si el byte anterior es un byte inicial, ya que ese valor de byte puede ser válido para su uso como byte inicial y como byte final. Por lo tanto, la aplicación tiene esencialmente el mismo problema que con la barra diagonal inversa posible. En otras palabras, las búsquedas de subcadenas son mucho más complicadas con un DBCS que con SBCSs o Unicode. En consecuencia, las aplicaciones que admiten DBCS deben usar funciones especiales, como [ \_ mbsstr](/cpp/c-runtime-library/reference/strstr-wcsstr-mbsstr-mbsstr-l), en lugar de la función [**StrStr**](https://msdn.microsoft.com/library/z9da80kz(v=VS.71).aspx) .

Las aplicaciones usan páginas de códigos DBCS de Windows con las versiones "A" de las funciones de Windows. Vea [convenciones para prototipos de función](conventions-for-function-prototypes.md) y [páginas de códigos](code-pages.md). Para ayudar a identificar una página de códigos DBCS, una aplicación puede usar la función [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) o [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) . Una aplicación puede usar la función [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte) para determinar si un valor determinado se puede usar como byte inicial de un carácter de 2 bytes. Además, una aplicación puede usar las funciones [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para asignar entre cadenas Unicode y DBCS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Juegos de caracteres](character-sets.md)
</dt> <dt>

[Juegos de caracteres de un solo byte](single-byte-character-sets.md)
</dt> </dl>

 

 
