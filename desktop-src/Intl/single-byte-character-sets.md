---
description: Un juego de caracteres de un solo byte (SBCS) es una asignación de 256 caracteres individuales a sus valores de código de identificación, implementados como una página de códigos.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Juegos de caracteres de un solo byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bb0150dfaf2e3b8e8251530fd5e90e7b1ede3b3597d344e5efb192fa96ed36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130235"
---
# <a name="single-byte-character-sets"></a>Juegos de caracteres de un solo byte

Un juego de caracteres de un solo byte (SBCS) es una asignación de 256 caracteres individuales a sus valores de código de identificación, implementados como una página de códigos. Un SBCS puede corresponder a una página de Windows o a una página de códigos oem. Una página de códigos SBCS también puede incluir una página de códigos no nativa, por ejemplo, una página de códigos EBCDIC. Para obtener definiciones de estas páginas de códigos, vea [Páginas de códigos](code-pages.md).

> [!Note]  
> Las Windows nuevas aplicaciones deben usar [Unicode](unicode.md) para evitar las incoherencias de páginas de códigos variadas y facilitar la localización. Sin embargo, algunos protocolos heredados requieren el uso de un SBCS. Cada página de códigos SBCS admite caracteres diferentes, pero ninguna página admite toda la gama de caracteres proporcionada por Unicode. Cada página de códigos de SBCS admite un subconjunto diferente, codificado de forma diferente. Los datos convertidos de una página de códigos de SBCS a otra están sujetos a daños, ya que el mismo valor de datos en páginas de códigos diferentes puede codificar un carácter diferente. Los datos convertidos de Unicode a SBCS están sujetos a pérdida de datos porque es posible que una página de códigos determinada no pueda representar todos los caracteres usados en los datos Unicode concretos.

 

Las aplicaciones usan SBCS Windows páginas de códigos con las versiones "A" de Windows funciones. Vea [Convenciones para prototipos de función](conventions-for-function-prototypes.md) y páginas de [códigos](code-pages.md). Para ayudar a identificar una página de códigos de SBCS, una aplicación puede usar la [**función GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) o [**GetCPInfoEx.**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) Además, una aplicación puede usar las funciones [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) y [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) para asignar entre cadenas Unicode y SBCS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Juegos de caracteres](character-sets.md)
</dt> <dt>

[Juegos de caracteres de doble byte](double-byte-character-sets.md)
</dt> </dl>

 

 



