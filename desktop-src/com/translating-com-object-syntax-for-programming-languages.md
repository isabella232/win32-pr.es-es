---
title: Traducir la sintaxis de objetos COM para lenguajes de programación
description: Traducir la sintaxis de objetos COM para lenguajes de programación
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903401"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a>Traducir la sintaxis de objetos COM para lenguajes de programación

Para llamar a un objeto COM desde una aplicación escrita en un lenguaje de programación distinto del usado para escribir el objeto COM, primero debe traducir la sintaxis del objeto al lenguaje de programación. Esta operación se puede completar mediante los siguientes pasos:

1.  Vea la biblioteca de tipos del objeto COM en la sintaxis del lenguaje de programación. Al hacerlo, se proporcionan descripciones de las clases, interfaces, métodos, propiedades y eventos del objeto en la sintaxis del lenguaje que se usa.

    Los productos para desarrolladores de Microsoft proporcionan varias herramientas que le ayudarán a ver y convertir bibliotecas de tipos. Para obtener más información, vea [visores de biblioteca de tipos y herramientas de conversión](type-library-viewers-and-conversion-tools.md) y [Cómo herramientas de desarrollo usar bibliotecas de tipos](how-developer-tools-use-type-libraries.md).

    Una vez que pueda ver la biblioteca de tipos del objeto en el lenguaje de programación que prefiera, puede comparar su sintaxis con la de la documentación del objeto. Si el objeto está documentado en un lenguaje de programación distinto del que está utilizando, los tipos de datos y la sintaxis pueden diferir, pero las descripciones de los parámetros, los valores devueltos y la funcionalidad del objeto deben ser iguales.

2.  Tenga en cuenta las consideraciones especiales para traducir a su lenguaje de programación.

    Dado que cada lenguaje de programación define conceptos que no pueden tener un equivalente en otros lenguajes, parte de la funcionalidad de un objeto puede funcionar de manera diferente en otro lenguaje o no estar disponible en absoluto. Por ejemplo, el lenguaje de programación Visual Basic no reconoce los tipos de datos sin signo de C++, como **unsignedÂ Long**. Una aplicación escrita en Visual Basic no puede usar métodos COM que acepten o devuelvan variables de tipo de datos sin firmar.

3.  Agregue el código compilado del objeto COM al proyecto. Normalmente, el código compilado se incluye en un archivo. dll o. ocx. Este paso es necesario para que el compilador reconozca las clases del objeto COM. Después de agregar el objeto COM, la aplicación puede usar sus clases e interfaces.

En los temas siguientes se describe cómo traducir y usar objetos COM en diversos lenguajes de programación:

-   [Traducir a C++](translating-to-c--.md)
-   [Trasladar a Visual Basic](translating-to-visual-basic.md)
-   [Traducir a Java](translating-to-java.md)

En estos temas se describen los procesos y las herramientas de conversión proporcionados por los productos para desarrolladores de Microsoft. Para obtener instrucciones sobre cómo programar objetos COM mediante herramientas de desarrollo creadas por otras compañías, consulte la documentación de las herramientas de desarrollo.

 

 




