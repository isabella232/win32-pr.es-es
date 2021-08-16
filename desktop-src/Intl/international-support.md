---
description: En esta sección se describen las tecnologías de Windows que permiten admitir las muchas culturas y los lenguajes escritos del marketplace internacional en la aplicación Win32 de Microsoft basada en C o C++.
ms.assetid: 90dbbd70-3609-4c12-bdc1-7fa222c96f67
title: Internacionalización para aplicaciones para Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78f4831390ffc31a5f3290f0784d32c3aa1044863c708e6e0329225519c2cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147548"
---
# <a name="internationalization-for-windows-applications"></a>Internacionalización para aplicaciones para Windows

(anteriormente titulado "Soporte internacional")

En esta sección se describen las tecnologías de Windows que permiten admitir las muchas culturas y los lenguajes escritos del marketplace internacional en la aplicación Win32 de Microsoft basada en C o C++.

Windows se ha convertido en una plataforma esencial para clientes de todo el mundo. Los usuarios internacionales esperan soluciones adaptadas a sus idiomas y regiones de todo el mundo. En esta sección, encontrará la información que necesita para desarrollar soluciones multilenguaje, transversales y de varios sitios. La compatibilidad internacional integrada en Windows permite implementar muchos escenarios con menos sobrecarga de ingeniería que nunca.

El desarrollo de aplicaciones listas para el mundo requiere el uso de muchos servicios y herramientas. Windows contiene características que le permiten desarrollar soluciones que:

- Admite las distintas necesidades específicas del idioma y específicas de la configuración regional de los usuarios de todo el mundo (incluida la compatibilidad con texto especializada, el comportamiento de ordenación, el formato de fecha y hora y los diseños de teclado). (Para obtener más información, vea [National Language Support Knowledge Center).](./national-language-support-reference.md)
- Se globalizan (se pueden implementar en todo el mundo a partir de una sola imagen binaria) y se pueden localizar (se pueden adaptar para mercados locales específicos). (Para obtener más información, [vea Interfaz de usuario multilingüe](./multilingual-user-interface.md)).
- Mostrar fuentes internacionales y texto, y permitir a los usuarios especificar la fuente que desean. (Para obtener más información, vea [Compatibilidad con scripts y](/globalization/input/font-support)fuentes Windows ).
- Permite al usuario escribir caracteres complejos y símbolos con un teclado estándar.
- Proporcionar compatibilidad con muchos lenguajes escritos diferentes a través de Unicode y juegos de caracteres tradicionales.
- Descubra la entrada de idioma de un usuario y adapte la experiencia de usuario proporcionada por la aplicación. (Para obtener más información, vea [Writing World-Ready Applications in Windows: Extended Linguistic Services in Windows](./using-extended-linguistic-services.md)).

## <a name="in-this-section"></a>En esta sección

En esta sección se documentan las siguientes tecnologías de soporte internacional. Se enumeran con algunos escenarios clave para los que se pueden usar.

- [Tareas iniciales con el desarrollo de Windows internacional](getting-started-with-international-development.md)

    Describe cómo empezar a crear aplicaciones listas para el mundo y proporciona un tutorial que ilustra una tarea común para escribir software global.

    Escenarios comunes:

    - Determine una ruta de acceso a seguir para aprender a desarrollar software internacional.
    - Descubra las tecnologías de internacionalización disponibles en Microsoft Windows Software Development Kit (SDK).
    - Siga un tutorial que toma una aplicación monolingüe existente y agrega compatibilidad con idiomas adicionales.

- [Servicios de globalización](globalization-services.md)

    Describe Los Servicios lingüísticos extendidos [(ELS),](extended-linguistic-services.md)que permiten detectar el idioma en el que se escribe el texto y la entrada del usuario, y [National Language Support (NLS),](national-language-support.md)que permite a una aplicación usar la información de configuración regional para mostrar información confidencial de la referencia cultural (como la hora, las fechas y la moneda) y ordenar las cadenas correctamente.

    Escenarios comunes:

    - Descubra el idioma de la entrada del usuario para que el contenido de ayuda se pueda mostrar en un idioma comprensible.
    - Detecte el script usado en el texto que se va a mostrar. Si es chino simplificado o tradicional, ofrezca al usuario la opción de transliterar el texto de uno a otro.
    - Permitir al usuario seleccionar una configuración regional (una colección de información de preferencias de usuario relacionadas con el idioma).
    - Mostrar horas, fechas, información de calendario, moneda y muchos otros objetos dependientes de la referencia cultural en los idiomas y formatos adecuados.
    - Ordene las cadenas en el orden esperado por el usuario de una configuración regional determinada.

- [Administrador de métodos de entrada](input-method-manager.md)

    Describe la tecnología utilizada por una aplicación para comunicarse con un editor de métodos de entrada (IME). El IME permite a los usuarios del equipo escribir caracteres complejos y símbolos mediante un teclado estándar.

    Escenario común:

    - Permitir que el usuario use un teclado estándar para escribir caracteres kanji en japonés.

- [Fuentes internacionales y presentación de texto](international-fonts-and-text-display.md)

    Describe la compatibilidad proporcionada por la plataforma Windows para fuentes internacionales, texto internacional y tipografía fina.

    Escenarios comunes:

    - Permitir al usuario seleccionar fuentes internacionales basadas en juego de caracteres.
    - Mostrar texto internacional.
    - Procese scripts complejos, incluida la representación bidireccional, el modelado contextual y las ligaduras (Uniscribe).
    - Permita un alto grado de control para la tipografía fina (Uniscribe).

- [Interfaz de usuario multilingüe](multilingual-user-interface.md)

    Describe cómo las aplicaciones pueden separar los recursos dependientes del lenguaje del código independiente del idioma para los idiomas de interfaz de usuario admitidos.

    Escenarios comunes:

    - Cree imágenes de implementación única regionales o en todo el mundo de una aplicación.
    - Localice una solución actualizando los recursos de la aplicación sin ningún cambio en el código fuente de la aplicación.
    - Permitir que los usuarios cambien de un idioma de interfaz de usuario a otro en tiempo de ejecución.

- [Unicode y juegos de caracteres](unicode-and-character-sets.md)

    Describe cómo las aplicaciones pueden aprovechar Unicode, el estándar mundial de codificación de caracteres que usa valores de código de 16 bits para representar todos los caracteres usados en la informática moderna, incluidos los símbolos técnicos y los caracteres especiales que se usan en la publicación.

    Escenarios comunes:

    - Admitir los muchos idiomas diferentes del marketplace internacional a través de Unicode.
    - Convertir caracteres Unicode en y desde otros juegos de caracteres, cuando sea necesario.

- [Consideraciones de seguridad: Características internacionales](security-considerations--international-features.md)

    Proporciona información sobre las consideraciones de seguridad relacionadas con las características de soporte técnico de desarrollo internacional.

    La información de seguridad pertenece a todos los escenarios.

## <a name="related-international-technologies"></a>Tecnologías internacionales relacionadas

La compatibilidad con el desarrollo internacional también está disponible para las aplicaciones escritas en código administrado. Si va a desarrollar para la .NET Framework, necesitará algunos o todos estos:

- El [espacio de nombres System.Globalization](/dotnet/api/system.globalization) contiene clases que definen información relacionada con la referencia cultural y proporcionan funciones avanzadas de globalización.
- El [espacio de nombres System.Text](/dotnet/api/system.text) contiene clases que representan codificaciones de caracteres, convierten bloques de caracteres y manipulan y formatear objetos String.
