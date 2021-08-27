---
description: Un identificador de idioma es una abreviatura numérica internacional estándar para el idioma de un país o región geográfica.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Identificadores de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6245101099b5df5c192af60a977ede88412f95cca8afda9270b7aba6e1c41ad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106985"
---
# <a name="language-identifiers"></a>Identificadores de idioma

Un identificador de idioma es una abreviatura numérica internacional estándar para [el idioma](locales-and-languages.md) de un país o región geográfica. Cada idioma tiene un identificador de idioma único (tipo de datos LANGID), un valor de 16 bits que consta de un identificador de idioma principal y un identificador de sublenguaje. Para obtener más información sobre los identificadores de idioma, vea [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md).

Un identificador de idioma se construye mediante la [**macro MAKELANGID.**](/windows/desktop/api/Winnt/nf-winnt-makelangid) En la ilustración siguiente se muestra el formato de los bits en un identificador de idioma.

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

Los siguientes son identificadores de lenguaje predefinidos:

-   LANG \_ SYSTEM \_ DEFAULT(PREDETERMINADO DEL SISTEMA LANG). Idioma predeterminado del sistema operativo.
-   LANG \_ USER \_ DEFAULT. El idioma del usuario actual.

La aplicación puede recuperar los identificadores de lenguaje actuales mediante las [Interfaz de usuario multilingüe](multilingual-user-interface.md) de trabajo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuraciones regionales e idiomas](locales-and-languages.md)
</dt> <dt>

[Constantes y cadenas de identificador de lenguaje](language-identifier-constants-and-strings.md)
</dt> <dt>

[Interfaz de usuario multilingüe](multilingual-user-interface.md)
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



