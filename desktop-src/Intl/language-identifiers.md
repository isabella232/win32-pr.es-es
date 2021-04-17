---
description: Un identificador de idioma es una abreviatura numérica internacional estándar para el idioma de un país o región geográfica.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Identificadores de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e3e8f88a64d49d04402c0e72a3946bcddc41e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666595"
---
# <a name="language-identifiers"></a>Identificadores de idioma

Un identificador de idioma es una abreviatura numérica internacional estándar para el [idioma](locales-and-languages.md) de un país o región geográfica. Cada idioma tiene un identificador de idioma único (tipo de datos LANGID), un valor de 16 bits que consta de un identificador de idioma principal y un identificador de subidioma. Para obtener más información sobre los identificadores de idioma, vea [constantes y cadenas de identificador de idioma](language-identifier-constants-and-strings.md).

Un identificador de idioma se construye mediante la macro [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) . En la ilustración siguiente se muestra el formato de los bits en un identificador de idioma.

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

Estos son los identificadores de idioma predefinidos:

-   IDIOMA \_ predeterminado del sistema \_ . Idioma predeterminado del sistema operativo.
-   \_valor predeterminado de usuario de Lang \_ . El idioma del usuario actual.

La aplicación puede recuperar los identificadores de idioma actuales mediante las funciones de la [interfaz de usuario multilingüe](multilingual-user-interface.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuraciones regionales e idiomas](locales-and-languages.md)
</dt> <dt>

[Constantes y cadenas de identificador de idioma](language-identifier-constants-and-strings.md)
</dt> <dt>

[Interfaz de usuario multilingüe](multilingual-user-interface.md)
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



