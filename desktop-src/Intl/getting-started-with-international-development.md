---
description: Este tema le ayudará a comenzar a crear aplicaciones de uso internacional, especificando requisitos previos, resumiendo tecnologías e introduciendo un tutorial de introducción.
ms.assetid: 80c10bc2-b7e3-4f24-8bac-826149a376c7
title: Introducción con el desarrollo internacional de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cc77a86b652f1b713b29517b513cddc26ed801
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687942"
---
# <a name="getting-started-with-international-windows-development"></a>Introducción con el desarrollo internacional de Windows

Este tema le ayudará a comenzar a crear aplicaciones de uso internacional, especificando requisitos previos, resumiendo tecnologías e introduciendo un tutorial de introducción.

## <a name="getting-started"></a>Introducción

Si escribe aplicaciones para los usuarios en una sola configuración regional, esas aplicaciones pueden tener éxito incluso si las diseña con suposiciones específicas de la configuración regional, como presentar fechas en un formato determinado u ordenar cadenas en una secuencia determinada. Pero ahora tiene que asegurarse de que las aplicaciones pueden usarse en varios países, por parte de usuarios que tienen distintos idiomas y referencias culturales diferentes. Para tener éxito en varias configuraciones regionales, las aplicaciones deben ajustarse a la configuración regional en la que se ejecutan. Esta flexibilidad es importante si se agrega a una aplicación existente o se diseña en una nueva aplicación.

Esta sección le ayuda a empezar a trabajar en el desarrollo internacional. Presenta vínculos a temas que proporcionan información general sobre los requisitos previos de internacionalización. Resume las tecnologías que ofrece el SDK para la compatibilidad de los clientes de todo el mundo. Por último, en esta sección se proporciona una aplicación de ejemplo que resuelve un problema que se suele encontrar al escribir software global.

## <a name="prerequisites"></a>Requisitos previos

Debe familiarizarse con los problemas que surgen al desarrollar software internacional para Windows. Comience con estas información general.

-   [Comprender la internacionalización](understanding-internationalization.md) explica la dificultad adicional de desarrollar aplicaciones de uso internacional y define los términos clave.
-   El tema [obtención mundial](https://msdn.microsoft.com/goglobal/bb895995.aspx) le conduce a las instrucciones y prácticas recomendadas que puede hojear o profundizar según sea necesario.
-   La [lista de comprobación de internacionalización](internationalization-checklist.md) resume las acciones que debe realizar para crear una aplicación de uso internacional.
-   La seguridad siempre es un problema en el desarrollo de software, pero debe tener en cuenta otros problemas al desarrollar software internacional. Eche un vistazo a [las consideraciones de seguridad: características internacionales](security-considerations--international-features.md).

También debe tener en cuenta los artículos más extensos que encontrará en el [Centro para desarrolladores de go global](https://msdn.microsoft.com/globalization/mt613165) en la sección [paso a paso de globalización](https://msdn.microsoft.com/globalization/mt642951) . Al desarrollar software internacional, querrá consultar las información general adicional y los artículos detallados que se pueden encontrar allí.

## <a name="learning-paths"></a>Rutas de aprendizaje

La ruta de acceso que sigue en el aprendizaje para crear software internacional depende de los escenarios a los que se enfrente. Los escenarios siguientes se basan en los que se presentan en el tema de la sección principal, [internacionalización para aplicaciones Windows](international-support.md).

-   **Cree aplicaciones que se puedan implementar en varias regiones en varios idiomas.**

    El reto es desarrollar una aplicación que no tenga que volver a escribirse para cada idioma o referencia cultural.

    -   Lea el artículo [Descripción de la interfaz de usuario multilingüe (MUI)](./about-multilingual-user-interface.md).
    -   Explore la documentación de la [interfaz de usuario multilingüe](multilingual-user-interface.md).
    -   Introducción a la aplicación [Hello mui](#the-hello-mui-application) .

-   **Admite la entrada y la presentación de diferentes idiomas, juegos de caracteres y fuentes.**

    Es posible que la aplicación necesite admitir varios conjuntos de caracteres, admitir scripts complejos (como los que se usan para representar los idiomas hebreo, Árabe, tailandés e hindú), permitir que el usuario seleccione entre fuentes internacionales, o permitir que el usuario escriba caracteres y símbolos, como el kanji japonés, para otros idiomas mediante un teclado estándar.

    -   Lea los artículos:

        -   [Compatibilidad con scripts y fuentes en Windows](https://msdn.microsoft.com/globalization/mt791278)
        -   [Idioma de entrada: Teclados y IME](https://msdn.microsoft.com/globalization/mt662332)

    -   Explore la documentación de:

        -   [Unicode y juegos de caracteres](unicode-and-character-sets.md)
        -   [Fuentes internacionales y presentación de texto](international-fonts-and-text-display.md)
        -   [Administrador de métodos de entrada](input-method-manager.md)

-   **Muestra los objetos dependientes de la referencia cultural en los formatos adecuados.**

    Las aplicaciones internacionales deben usar la configuración regional para ordenar cadenas correctamente y para mostrar información que tiene en cuenta la referencia cultural, como la hora, las fechas y la moneda.

    -   Explore el [centro de soporte técnico de National Language support](./national-language-support-reference.md).
    -   Examine la documentación de [National Language support (NLS)](national-language-support.md).

-   **Descubra el lenguaje o el script que usa el usuario y aplíquelo a los otros servicios de la aplicación.**

    Si la aplicación puede determinar el idioma en el que se escribe el texto y los datos proporcionados por el usuario, puede mostrar contenido como mensajes o ayuda en un lenguaje comprensible.

    -   Lea el artículo [escribir aplicaciones de uso internacional en Windows: servicios lingüísticos extendidos en Windows](./using-extended-linguistic-services.md).
    -   Explore la documentación de los [servicios lingüísticos extendidos (Els)](extended-linguistic-services.md).

## <a name="internationalization-technologies-in-the-sdk"></a>Tecnologías de internacionalización en el SDK

La sección de soporte técnico de desarrollo internacional del SDK de proporciona tecnologías que permiten a la aplicación enumerar idiomas, configuraciones regionales y formatos específicos de la configuración regional. Puede usarlos en aplicaciones de Microsoft Win32 que escriba en C o C++.

Los [servicios lingüísticos extendidos](extended-linguistic-services.md) ofrecen tecnología Microsoft-patentada para la identificación de idiomas y scripts en texto. La aplicación puede determinar los servicios disponibles en función de la categoría, así como el idioma de entrada y salida, el script y el tipo de contenido.

Las [fuentes internacionales y la presentación de texto](international-fonts-and-text-display.md) proporcionan información sobre fuentes internacionales, scripts y glifos complejos, y la representación precisa de tipografía en la plataforma Windows.

El [Administrador de métodos de entrada (IMM)](input-method-manager.md) es una tecnología que ayuda a la aplicación a recibir entradas del software del editor de métodos de entrada (IME), que a su vez permite la entrada de caracteres y símbolos, como el kanji japonés, para otros idiomas mediante el uso de un teclado estándar.

## <a name="the-hello-mui-application"></a>La aplicación Hello MUI

Una tarea común en el desarrollo internacional comienza con una aplicación de Monolingual que debe estar preparada para el mundo. Debe agregar compatibilidad con idiomas adicionales, pero de forma que no sea necesario que vuelva a escribir el código para cada nuevo idioma o referencia cultural.

Esta tarea ofrece la oportunidad de presentar un tutorial que le lleve paso a paso la creación de una aplicación Hola a todos, haciendo uso del modelo de recursos de la [interfaz de usuario multilingüe (MUI)](multilingual-user-interface.md) y del soporte técnico asociado proporcionado en Windows.

En el tutorial se adopta el concepto de la conocida Hola mundo aplicación, en la que se muestra el uso de MUI para compilar una aplicación básica multilingüe.

Puede comenzar el tutorial de Hola a todos en la [incorporación de compatibilidad con la interfaz de usuario multilingüe en una aplicación](creating-a-multilingual-user-interface-application.md).

 

 
