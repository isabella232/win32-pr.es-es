---
description: En esta sección se describen las tecnologías de Windows que permiten admitir las diversas referencias culturales y lenguajes escritos del marketplace internacional en la aplicación Microsoft Win32 basada en C o C++.
ms.assetid: 90dbbd70-3609-4c12-bdc1-7fa222c96f67
title: Internacionalización para aplicaciones para Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f6e4952c94af3b14dc0e8f4f135c1cc0cebafc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810400"
---
# <a name="internationalization-for-windows-applications"></a>Internacionalización para aplicaciones para Windows

(Anteriormente titulado "soporte internacional")

En esta sección se describen las tecnologías de Windows que permiten admitir las diversas referencias culturales y lenguajes escritos del marketplace internacional en la aplicación Microsoft Win32 basada en C o C++.

Windows se ha convertido en una plataforma esencial para los clientes de todo el mundo. Los usuarios internacionales esperan soluciones que se adapten a sus idiomas y regiones de todo el mundo. En esta sección, encontrará la información que necesita para desarrollar soluciones multilingües, multiculturales y de varios sitios. La compatibilidad internacional integrada en Windows le permite implementar muchos escenarios con menos sobrecarga de ingeniería que nunca.

El desarrollo de aplicaciones de uso internacional requiere el uso de muchos servicios y herramientas. Windows contiene características que permiten desarrollar soluciones que:

- Admita las distintas necesidades específicas del idioma y específicas de la configuración regional de los usuarios de todo el mundo (incluida la compatibilidad con texto especializado, el comportamiento de ordenación, el formato de fecha y hora y las distribuciones de teclado). (Para obtener más información, vea [centro de soporte técnico de National Language](./national-language-support-reference.md)).
- Se globalizan (se pueden implementar en todo el mundo a partir de una sola imagen binaria) y se pueden localizar (pueden adaptarse a mercados locales específicos). (Para obtener más información, consulte [interfaz de usuario multilingüe](./multilingual-user-interface.md)).
- Mostrar fuentes y texto internacionales y permitir que los usuarios especifiquen la fuente que deseen. (Para obtener más información, consulte [compatibilidad con scripts y fuentes en Windows](/globalization/input/font-support)).
- Permite al usuario escribir caracteres y símbolos complejos con un teclado estándar.
- Proporcionar compatibilidad con muchos lenguajes escritos diferentes a través de Unicode y juegos de caracteres tradicionales.
- Detecte la entrada de idioma de un usuario y personalice la experiencia del usuario proporcionada por la aplicación. (Para obtener más información, consulte [escribir aplicaciones de uso internacional en Windows: servicios lingüísticos extendidos en Windows](./using-extended-linguistic-services.md)).

## <a name="in-this-section"></a>En esta sección

En esta sección se documentan las siguientes tecnologías de soporte internacional. Aparecen con algunos escenarios clave para los que se pueden usar.

- [Introducción con el desarrollo internacional de Windows](getting-started-with-international-development.md)

    Describe cómo empezar a crear aplicaciones de uso internacional y proporciona un tutorial que ilustra una tarea común en la escritura de software global.

    Escenarios comunes:

    - Determine la ruta de acceso que se debe llevar a cabo para obtener información sobre cómo desarrollar software internacional.
    - Descubra las tecnologías de internacionalización disponibles en el kit de desarrollo de software (SDK) de Microsoft Windows.
    - Siga un tutorial que toma una aplicación de Monolingual existente y agrega compatibilidad con otros idiomas.

- [Servicios de globalización](globalization-services.md)

    Describe los [servicios lingüísticos extendidos (Els)](extended-linguistic-services.md), que permiten detectar el idioma en el que se escribe el texto y la entrada del usuario, y la [compatibilidad con el idioma nacional (NLS)](national-language-support.md), que permite a una aplicación usar información de configuración regional para mostrar información que tiene en cuenta la referencia cultural (como hora, fechas y moneda) y ordenar correctamente las cadenas.

    Escenarios comunes:

    - Detecta el idioma de la entrada del usuario, de modo que el contenido de la ayuda se puede mostrar en un lenguaje comprensible.
    - Detecta el script usado en el texto que se va a mostrar. Si se trata de un chino simplificado o tradicional, ofrezca al usuario la opción de convertir el texto en transliteración de uno a otro.
    - Permite al usuario seleccionar una configuración regional (una colección de información de preferencias de usuario relacionada con el idioma).
    - Mostrar horas, fechas, información de calendario, moneda y muchos otros objetos dependientes de la referencia cultural en los idiomas y formatos adecuados.
    - Ordena las cadenas en el orden esperado por el usuario de una configuración regional determinada.

- [Administrador de métodos de entrada](input-method-manager.md)

    Describe la tecnología usada por una aplicación para comunicarse con un editor de métodos de entrada (IME). El IME permite a los usuarios del equipo escribir caracteres y símbolos complejos mediante un teclado estándar.

    Escenario común:

    - Permite al usuario usar un teclado estándar para escribir caracteres Kanji japoneses.

- [Fuentes internacionales y presentación de texto](international-fonts-and-text-display.md)

    Describe la compatibilidad proporcionada por la plataforma de Windows para fuentes internacionales, texto internacional y tipografía precisa.

    Escenarios comunes:

    - Permite al usuario seleccionar fuentes internacionales basadas en el juego de caracteres.
    - Mostrar texto internacional.
    - Procese scripts complejos, incluida la representación bidireccional, el modelado contextual y las ligaduras (Uniscribe).
    - Permitir un alto grado de control para la tipografía precisa (Uniscribe).

- [Interfaz de usuario multilingüe](multilingual-user-interface.md)

    Describe el modo en que las aplicaciones pueden separar los recursos dependientes del idioma del código independiente del lenguaje para los idiomas de interfaz de usuario compatibles.

    Escenarios comunes:

    - Cree imágenes de implementación única regional o internacional de una aplicación.
    - Localizar una solución actualizando los recursos de la aplicación sin cambiar el código fuente de la aplicación.
    - Permitir a los usuarios cambiar de un idioma de interfaz de usuario a otro en tiempo de ejecución.

- [Unicode y juegos de caracteres](unicode-and-character-sets.md)

    Describe cómo las aplicaciones pueden aprovechar las ventajas de Unicode, el estándar de codificación de caracteres en todo el mundo que usa valores de código de 16 bits para representar todos los caracteres que se usan en la informática moderna, incluidos los símbolos técnicos y los caracteres especiales que se usan en la publicación.

    Escenarios comunes:

    - Admita los distintos idiomas de marketplace internacional a través de Unicode.
    - Convierta los caracteres Unicode en otros juegos de caracteres, si es necesario.

- [Consideraciones de seguridad: características internacionales](security-considerations--international-features.md)

    Proporciona información sobre las consideraciones de seguridad relacionadas con las características de compatibilidad con el desarrollo internacional.

    La información de seguridad pertenece a todos los escenarios.

## <a name="related-international-technologies"></a>Tecnologías internacionales relacionadas

La compatibilidad con el desarrollo internacional también está disponible para las aplicaciones escritas en código administrado. Si va a desarrollar para el .NET Framework, necesitará algunos o todos:

- El [espacio de nombres System. Globalization](/dotnet/api/system.globalization) contiene clases que definen información relativa a la referencia cultural y proporcionan funciones avanzadas de globalización.
- El [espacio de nombres System. Text](/dotnet/api/system.text) contiene clases que representan codificaciones de caracteres, convierten bloques de caracteres y manipulan y dan formato a objetos de cadena.
