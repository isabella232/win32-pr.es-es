---
title: Traducción de la sintaxis de objetos COM para lenguajes de programación
description: Traducción de la sintaxis de objetos COM para lenguajes de programación
ms.assetid: 021e0085-c720-401e-9637-76580e67b307
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9d1ec65e5b4ff8f3b61106a4b7a8c9ee3134b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253076"
---
# <a name="translating-com-object-syntax-for-programming-languages"></a>Traducción de la sintaxis de objetos COM para lenguajes de programación

Para llamar a un objeto COM desde una aplicación escrita en un lenguaje de programación distinto del utilizado para escribir el objeto COM, primero debe traducir la sintaxis del objeto al lenguaje de programación. Esta operación se puede completar mediante los siguientes pasos:

1.  Vea la biblioteca de tipos del objeto COM en la sintaxis del lenguaje de programación. Esto proporciona descripciones de las clases, interfaces, métodos, propiedades y eventos del objeto en la sintaxis del lenguaje que se usa.

    Los productos para desarrolladores de Microsoft proporcionan varias herramientas para ayudarle a ver y convertir bibliotecas de tipos. Para obtener más información, vea [Visores y](type-library-viewers-and-conversion-tools.md) herramientas de conversión de bibliotecas de tipos y Cómo [Herramientas de desarrollo usar bibliotecas de tipos](how-developer-tools-use-type-libraries.md).

    Una vez que pueda ver la biblioteca de tipos del objeto en el lenguaje de programación que prefiera, puede comparar su sintaxis con la de la documentación del objeto. Si el objeto está documentado en un lenguaje de programación distinto del que está usando, los tipos de datos y la sintaxis pueden diferir, pero las descripciones de los parámetros, los valores devueltos y la funcionalidad del objeto deben ser las mismas.

2.  Tener en cuenta cualquier consideración especial para traducir a su lenguaje de programación.

    Dado que cada lenguaje de programación define conceptos que pueden no tener un equivalente en otros lenguajes, parte de la funcionalidad de un objeto puede funcionar de forma diferente en otro lenguaje o no estar disponible en absoluto. Por ejemplo, el Visual Basic programación no reconoce los tipos de datos sin signo de C++, como **unsignedÂ long**. Una aplicación escrita en Visual Basic no puede usar métodos COM que acepten o devuelvan variables de tipo de datos sin signo.

3.  Agregue el código compilado del objeto COM al proyecto. El código compilado normalmente se encuentra en un archivo .dll o .ocx. Este paso es necesario para que el compilador reconozca las clases del objeto COM. Después de agregar el objeto COM, la aplicación puede usar sus clases e interfaces.

En los temas siguientes se describe cómo traducir y usar objetos COM en diversos lenguajes de programación:

-   [Traducción a C++](translating-to-c--.md)
-   [Traducción a Visual Basic](translating-to-visual-basic.md)
-   [Traducción a Java](translating-to-java.md)

En estos temas se describen las herramientas de conversión y los procesos proporcionados por los productos para desarrolladores de Microsoft. Para obtener instrucciones sobre cómo programar objetos COM mediante herramientas de desarrollo creadas por otras empresas, consulte la documentación de esas herramientas de desarrollo.

 

 




