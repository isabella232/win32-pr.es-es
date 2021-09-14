---
description: En este tema se proporcionan las acciones que se deben realizar para crear código que admita varios mercados. Tenga en cuenta estas instrucciones como guía durante el diseño del código y como métricas al evaluar las compilaciones.
ms.assetid: cf2ac58e-7fc3-4635-8b82-586a0732b2a3
title: Lista de comprobación de internacionalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b18ef8cf88efa8d496d19c0b66208cd44abaf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063091"
---
# <a name="internationalization-checklist"></a>Lista de comprobación de internacionalización

En este tema se proporcionan las acciones que se deben realizar para crear código que admita varios mercados. Tenga en cuenta estas instrucciones como guía durante el diseño del código y como métricas al evaluar las compilaciones.

-   Cree especificaciones de programa que tienen en cuenta las consideraciones internacionales desde el principio.
    -   Diseñe iconos y mapas de bits para que sean significativos y no ofensivos en los mercados de destino y no contengan texto.
    -   Menús de diseño y cuadros de diálogo para dejar espacio para la expansión de texto. Por ejemplo, las cadenas en inglés suelen expandirse en un 40 % cuando se traducen al alemán o neerlandés.
    -   No use referencias específicas de la jerga ni culturalmente en los elementos o mensajes de la interfaz de usuario.
    -   Cree combinaciones de teclas de método abreviado a las que se puede acceder en teclados internacionales. Por ejemplo, evite el uso de teclas de caracteres de puntuación como teclas de método abreviado, ya que no siempre se encuentran en teclados internacionales ni son fáciles de generar por el usuario. Para obtener ejemplos de diseños de teclado, [vea Windows Diseños de teclado](https://msdn.microsoft.com/goglobal/bb964651.aspx).
    -   Tenga en cuenta las leyes locales que afectan a los diseños de características, como los requisitos para que las entidades gubernamentales compren software que admita varios idiomas oficiales.
    -   Desarrolle contratos de terceros que admitan las decisiones de diseño y estándares internacionales de la interfaz de usuario de su organización.
    -   Use terminología coherente en las cadenas de interfaz de usuario que se deben traducir.

<!-- -->

-   Cree código independiente de la configuración regional.
    -   No concatena cadenas para formar oraciones.
    -   No use una variable de cadena determinada en más de un contexto, como volver a usar un fragmento de oración en mensajes y avisos diferentes, ya que es posible que estas cadenas no sean fáciles de traducir.
    -   Documente las cadenas mediante comentarios para proporcionar contexto a los traductores y marque claramente las cadenas o caracteres que no deben localizarse.
    -   No use constantes de caracteres codificadas de forma permanente, constantes numéricas, posiciones de pantalla, nombres de archivo o nombres de ruta de acceso que presuma un idioma determinado.
    -   Haga que los búferes sea lo suficientemente grande como para contener cadenas traducidas.
    -   Permita la entrada de datos con formatos que varían según la configuración regional, como fechas, horas y monedas.
    -   Use el tamaño del papel, el tamaño del sobre y otros valores predeterminados que sean adecuados para una configuración regional determinada.
    -   Asegúrese de que cada edición de lenguaje pueda leer documentos creados por las otras ediciones.
    -   Proporcione compatibilidad con hardware específico de la configuración regional, si es necesario.
    -   Configure características que no se aplican a los mercados internacionales como opciones de implementación que se pueden deshabilitar fácilmente.

<!-- -->

-   Cree código que aproveche la funcionalidad internacional que ofrece Microsoft Windows.
    -   Use la información internacional que lleva el sistema (Compatibilidad con idiomas nacionales).
    -   Use funciones del sistema para la ordenación, la conversión de casos y la asignación de cadenas.
    -   Use funciones de diseño de texto genéricas.
    -   Responda a los cambios en la configuración internacional Panel de control.
    -   Controle el \_ mensaje INPUTLANGCHANGEREQUEST de WM.
    -   Admite editores de métodos de entrada, texto vertical y reglas de separación de líneas en las ediciones de Este de Asia.

<!-- -->

-   Compile todas las ediciones internacionales del programa a partir de un conjunto de archivos de código fuente.
    -   Minimice o elimine los mecanismos que requieren que se vuelva a compilar el código para distintas ediciones de lenguaje.
    -   Almacene elementos localizables, como cadenas e iconos, en Windows archivos de recursos.
    -   Almacene documentos en todas las ediciones de lenguaje con el mismo formato de archivo.

<!-- -->

-   Admite diferentes juegos de caracteres, no solo la página de códigos Latin 1, número 1252.
    -   El programa admite entornos de red en los que los equipos ejecutan sistemas operativos con páginas de códigos predeterminadas diferentes.
    -   Use GetCPInfoEx para recuperar intervalos de bytes iniciales para páginas de códigos de Este de Asia.
    -   Analizar caracteres de doble byte en aplicaciones de idioma este de Asia, a menos que el código se base en Unicode.
    -   Admite Unicode o conversión entre Unicode y la página de códigos local.
    -   No suponga que todos los caracteres son de 8 o 16 bits.
    -   Use tipos de datos genéricos y prototipos de función genéricos.
    -   Use la propiedad charset de fuente, que llama a EnumFontFamiliesEx y a la función de diálogo común ChooseFont.
    -   Muestre e imprima texto con las fuentes adecuadas para la configuración regional.

<!-- -->

-   Pruebe las características internacionales del programa.
    -   El texto traducido debe cumplir los estándares de los hablantes nativos.
    -   Los cuadros de diálogo deben cambiar de tamaño correctamente y el texto se debe dividir correctamente, cuando se muestran idiomas diferentes.
    -   Los cuadros de diálogo, las barras de estado, las barras de herramientas y los menús deben caber en la pantalla y leerse de forma legible cuando la pantalla se establece en resoluciones diferentes, para todos los idiomas traducidos.
    -   Los aceleradores de menús y cuadros de diálogo deben ser únicos.
    -   Los usuarios deben poder escribir caracteres de scripts no europeos en documentos, cuadros de diálogo y nombres de archivo.
    -   Los usuarios deben poder cortar, pegar, guardar e imprimir caracteres de scripts no europeos correctamente.
    -   La ordenación y la conversión de mayúsculas y minúsculas deben ser precisas para distintas configuraciones regionales.
    -   La aplicación debe funcionar correctamente en las ediciones localizadas de Windows.

 

 



