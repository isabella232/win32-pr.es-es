---
description: Este tema le ayuda a empezar a crear aplicaciones listas para el mundo mediante la especificación de requisitos previos, el resumen de tecnologías y la introducción a un tutorial de introducción.
ms.assetid: 80c10bc2-b7e3-4f24-8bac-826149a376c7
title: Tareas iniciales con el desarrollo de Windows internacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36cc77a86b652f1b713b29517b513cddc26ed801
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274623"
---
# <a name="getting-started-with-international-windows-development"></a>Tareas iniciales con el desarrollo de Windows internacional

Este tema le ayuda a empezar a crear aplicaciones listas para el mundo mediante la especificación de requisitos previos, el resumen de tecnologías y la introducción a un tutorial de introducción.

## <a name="getting-started"></a>Introducción

Si escribe aplicaciones para los usuarios en una sola configuración regional, esas aplicaciones pueden ser correctas aunque las diseñe con suposiciones específicas de la configuración regional, como presentar fechas en un formato determinado o ordenar cadenas en una secuencia determinada. Pero ahora tiene que asegurarse de que las aplicaciones se pueden usar en varios países, por parte de los usuarios que tienen idiomas diferentes y distintas culturas. Para realizar correctamente varias configuraciones regionales, las aplicaciones deben ajustarse a la configuración regional en la que se ejecutan. Esta flexibilidad es importante tanto si se agrega a una aplicación existente como si se diseña en una nueva aplicación.

Esta sección le ayuda a empezar a trabajar en el desarrollo internacional. Presenta vínculos a temas que proporcionan información general sobre los requisitos previos de internacionalización. Resume las tecnologías que ofrece el SDK para el soporte técnico de clientes de todo el mundo. Por último, en esta sección se proporciona una aplicación de ejemplo que resuelve un problema que a menudo se produce al escribir software global.

## <a name="prerequisites"></a>Prerrequisitos

Debe familiarizarse con los problemas que surgen al desarrollar software internacional para Windows. Comience con estas información general.

-   [En Descripción de la internacionalización](understanding-internationalization.md) se explica la dificultad agregada de desarrollar aplicaciones listas para el mundo y se definen términos clave.
-   El [tema Get World-Ready](https://msdn.microsoft.com/goglobal/bb895995.aspx) le lleva a directrices y procedimientos recomendados que puede conocer o profundizar según sea necesario.
-   La [lista de comprobación de](internationalization-checklist.md) internacionalización resume las acciones que debe realizar para crear una aplicación lista para el mundo.
-   La seguridad siempre es un problema en el desarrollo de software, pero debe tener en cuenta otros problemas al desarrollar software internacional. Echar un vistazo a [Consideraciones de seguridad: Características internacionales](security-considerations--international-features.md).

Tenga en cuenta también los artículos más amplios que se pueden encontrar en el Centro para desarrolladores globales de [Go](https://msdn.microsoft.com/globalization/mt613165) en la sección Paso a paso de [globalización.](https://msdn.microsoft.com/globalization/mt642951) A medida que desarrolle software internacional, querrá consultar información general adicional y artículos detallados que se pueden encontrar allí.

## <a name="learning-paths"></a>Rutas de aprendizaje

La ruta de acceso que sigue a continuación para aprender a crear software internacional depende de los escenarios a los que se enfrenta. Los escenarios siguientes se basan en los presentados en el tema de la sección principal, [Internacionalización para Windows Aplicaciones](international-support.md).

-   **Cree aplicaciones que se puedan implementar en varias regiones en varios idiomas.**

    El desafío es desarrollar una aplicación que no tenga que reescribirse para cada idioma o referencia cultural.

    -   Lea el artículo [Understanding Interfaz de usuario multilingüe (MUI) (Descripción de Interfaz de usuario multilingüe (MUI)](./about-multilingual-user-interface.md)).
    -   Explore la documentación de [Interfaz de usuario multilingüe](multilingual-user-interface.md).
    -   Introducción a la [aplicación Hello MUI.](#the-hello-mui-application)

-   **Admite la entrada y presentación de diferentes idiomas, juegos de caracteres y fuentes.**

    Es posible que la aplicación tenga que admitir varios juegos de caracteres, admitir scripts complejos (como los que se usan para representar idiomas hebreo, árabe, tailandés e indic), permitir al usuario seleccionar fuentes internacionales o permitir que el usuario escriba caracteres y símbolos, como kanji japonés, para otros idiomas mediante un teclado estándar.

    -   Lea los artículos:

        -   [Compatibilidad con scripts y fuentes en Windows](https://msdn.microsoft.com/globalization/mt791278)
        -   [Idioma de entrada: teclados e IME](https://msdn.microsoft.com/globalization/mt662332)

    -   Explore la documentación para:

        -   [Unicode y juegos de caracteres](unicode-and-character-sets.md)
        -   [Fuentes internacionales y presentación de texto](international-fonts-and-text-display.md)
        -   [Administrador de métodos de entrada](input-method-manager.md)

-   **Mostrar objetos dependientes de la referencia cultural en formatos adecuados.**

    Las aplicaciones internacionales deben usar la configuración regional para ordenar correctamente las cadenas y mostrar información que distingue la referencia cultural, como la hora, las fechas y la moneda.

    -   Explore el [Centro de conocimientos de compatibilidad con idiomas nacionales](./national-language-support-reference.md).
    -   Examine la documentación de [Compatibilidad con idiomas nacionales (NLS).](national-language-support.md)

-   **Descubra el lenguaje o script que usa el usuario y aplíctelo a los demás servicios de la aplicación.**

    Si la aplicación puede determinar el idioma en el que se escribe el texto y la entrada del usuario, puede mostrar contenido como mensajes o ayuda en un idioma comprensible.

    -   Lea el artículo [Writing World-Ready Applications in Windows: Extended Linguistic Services in Windows](./using-extended-linguistic-services.md).
    -   Explore la documentación de [Extended Linguistic Services (ELS).](extended-linguistic-services.md)

## <a name="internationalization-technologies-in-the-sdk"></a>Tecnologías de internacionalización en el SDK

La sección Compatibilidad internacional de desarrollo del SDK proporciona tecnologías que permiten a la aplicación enumerar idiomas, configuraciones regionales y formatos específicos de la configuración regional. Puede usarlos en aplicaciones de Microsoft Win32 que escriba en C o C++.

Los [Servicios lingüísticos extendidos](extended-linguistic-services.md) ofrecen tecnología de microsoft para la identificación de idiomas y scripts en texto. La aplicación puede determinar los servicios disponibles en función de la categoría, así como del idioma de entrada y salida, el script y el tipo de contenido.

[Fuentes internacionales y presentación de texto](international-fonts-and-text-display.md) proporciona información sobre fuentes internacionales, scripts complejos y glifos, y la representación fina de tipografía en la plataforma Windows internacional.

El Administrador de métodos de entrada [(IMM)](input-method-manager.md) es una tecnología que ayuda a la aplicación a recibir entradas del software del Editor de métodos de entrada (IME), que a su vez permite la entrada de caracteres y símbolos, como kanji japonés, para otros idiomas mediante un teclado estándar.

## <a name="the-hello-mui-application"></a>La aplicación Hello MUI

Una tarea común en el desarrollo internacional comienza con una aplicación monolingüe que debe preparar para todo el mundo. Debe agregar compatibilidad con idiomas adicionales, pero de forma que no sea necesario volver a escribir el código para cada idioma o referencia cultural nuevos.

Esta tarea proporciona la oportunidad de presentar un tutorial que le lleva paso a paso a través de la creación de una aplicación Hello MUI, haciendo uso del modelo de recursos [de Interfaz de usuario multilingüe (MUI)](multilingual-user-interface.md) y la compatibilidad asociada proporcionada en Windows.

En el tutorial se adopta el concepto de aplicación Hola mundo conocida, que muestra el uso de MUI para crear una aplicación multilingüe básica.

Puede comenzar el tutorial Hello MUI en Adding Interfaz de usuario multilingüe Support to an Application (Agregar compatibilidad [con Interfaz de usuario multilingüe a una aplicación).](creating-a-multilingual-user-interface-application.md)

 

 
