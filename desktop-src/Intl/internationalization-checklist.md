---
description: En este tema se proporcionan las acciones que se deben llevar a cabo para crear código que admita varios mercados. Tenga en cuenta estas instrucciones como guía durante el diseño del código y como métricas al evaluar las compilaciones.
ms.assetid: cf2ac58e-7fc3-4635-8b82-586a0732b2a3
title: Lista de comprobación de internacionalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b18ef8cf88efa8d496d19c0b66208cd44abaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907622"
---
# <a name="internationalization-checklist"></a>Lista de comprobación de internacionalización

En este tema se proporcionan las acciones que se deben llevar a cabo para crear código que admita varios mercados. Tenga en cuenta estas instrucciones como guía durante el diseño del código y como métricas al evaluar las compilaciones.

-   Cree especificaciones del programa que tengan en cuenta las consideraciones internacionales desde el principio.
    -   Diseñe iconos y mapas de bits para que sean significativos y no ofensivos en los mercados de destino, y para que no contengan texto.
    -   Diseñe los menús y los cuadros de diálogo para dejar espacio para la expansión del texto. Por ejemplo, las cadenas en inglés suelen expandirse en un 40% cuando se traducen a alemán o holandés.
    -   No utilice jergas ni referencias culturales específicas en elementos o mensajes de la interfaz de usuario.
    -   Cree combinaciones de teclas de método abreviado a las que se pueda acceder en teclados internacionales. Por ejemplo, evite utilizar las teclas de carácter de puntuación como teclas de método abreviado porque no se encuentran siempre en teclados internacionales o el usuario las produce fácilmente. Para obtener ejemplos de distribuciones de teclado, consulte [distribuciones de teclado de Windows](https://msdn.microsoft.com/goglobal/bb964651.aspx).
    -   Tenga en cuenta las leyes locales que afecten a los diseños de características, como los requisitos que las entidades gubernamentales compran software que admite varios idiomas oficiales.
    -   Desarrolle acuerdos de terceros que admitan los estándares de interfaz de usuario y las decisiones de diseño internacionales de su organización.
    -   Use una terminología coherente en las cadenas de la interfaz de usuario que se deben traducir.

<!-- -->

-   Cree código que sea independiente de la configuración regional.
    -   No concatene cadenas para formar oraciones.
    -   No use una variable de cadena determinada en más de un contexto, como la reutilización de un fragmento de oración en diferentes mensajes y solicitudes, ya que es posible que estas cadenas no sean fáciles de traducir.
    -   Documente las cadenas mediante comentarios para proporcionar contexto a los traductores y marcar claramente cadenas o caracteres que no deben localizarse.
    -   No utilice constantes de caracteres codificados de forma rígida, constantes numéricas, posiciones de pantalla, nombres de archivo ni rutas de nombre que supongan un idioma determinado.
    -   Haga que los búferes sean lo suficientemente grandes como para contener cadenas traducidas.
    -   Permite la entrada de datos con formatos que varían según la configuración regional, como fechas, horas y divisas.
    -   Use el tamaño del papel, el tamaño del sobre y otros valores predeterminados adecuados para una configuración regional determinada.
    -   Asegúrese de que cada edición de idioma puede leer documentos creados por las otras ediciones.
    -   Proporcionar compatibilidad con el hardware específico de la configuración regional, si es necesario.
    -   Configure las características que no se aplican a los mercados internacionales como opciones de implementación que se pueden deshabilitar fácilmente.

<!-- -->

-   Cree código que aproveche la funcionalidad internacional que ofrece Microsoft Windows.
    -   Usar la información internacional incluida en el sistema (compatibilidad con National Language).
    -   Usar funciones del sistema para la ordenación, la conversión de mayúsculas y minúsculas y la asignación de cadenas.
    -   Usar funciones de diseño de texto genérico.
    -   Responder a los cambios en la configuración internacional del panel de control.
    -   Controle el \_ mensaje de INPUTLANGCHANGEREQUEST de WM.
    -   Admite editores de métodos de entrada, texto vertical y reglas de salto de línea en las ediciones de Asia oriental.

<!-- -->

-   Compile todas las ediciones internacionales del programa a partir de un conjunto de archivos de código fuente.
    -   Minimice o elimine los mecanismos que requieren que se vuelva a compilar el código para distintas ediciones de idioma.
    -   Almacenar elementos localizables, como cadenas e iconos, en archivos de recursos de Windows.
    -   Almacene documentos en todas las ediciones de idioma con el mismo formato de archivo.

<!-- -->

-   Admitir distintos juegos de caracteres, no solo la página de códigos Latin 1, número 1252.
    -   El programa es compatible con entornos de red en los que los equipos ejecutan sistemas operativos con diferentes páginas de códigos predeterminadas.
    -   Use GetCPInfoEx para recuperar los intervalos de bytes iniciales de las páginas de códigos de Asia oriental.
    -   Analizar caracteres de doble byte en aplicaciones de idiomas asiáticos orientales, a menos que el código se base en Unicode.
    -   Admitir Unicode o la conversión entre Unicode y la página de códigos local.
    -   No asuma que todos los caracteres son de 8 o 16 bits.
    -   Usar tipos de datos genéricos y prototipos de función genéricos.
    -   Use la propiedad charset de fuente, que llama a EnumFontFamiliesEx y a la función de cuadro de diálogo común ChooseFont.
    -   Mostrar e imprimir texto con las fuentes adecuadas para la configuración regional.

<!-- -->

-   Pruebe las características internacionales del programa.
    -   El texto traducido debe cumplir los estándares de los hablantes nativos.
    -   Los cuadros de diálogo deberían cambiar de tamaño correctamente y el texto debe dividirse de forma adecuada cuando se muestren diferentes idiomas.
    -   Los cuadros de diálogo, barras de estado, barras de herramientas y menús deben caber en la pantalla y leerse de forma legible cuando la pantalla se establece en resoluciones diferentes, para todos los idiomas traducidos.
    -   Los aceleradores de menús y cuadros de diálogo deben ser únicos.
    -   Los usuarios deben poder escribir caracteres de scripts no europeos en documentos, cuadros de diálogo y nombres de archivo.
    -   Los usuarios deben poder cortar, pegar, guardar e imprimir correctamente caracteres de scripts no europeos.
    -   La ordenación y la conversión de mayúsculas y minúsculas deben ser precisas para diferentes configuraciones regionales.
    -   La aplicación debería funcionar correctamente en las ediciones localizadas de Windows.

 

 



