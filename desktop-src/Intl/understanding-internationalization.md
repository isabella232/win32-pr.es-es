---
description: Descripción de la internacionalización
ms.assetid: 9147cd20-eeae-4ad4-8d51-ac1d68a4b2c5
title: Descripción de la internacionalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df3fc38ab844ec991c0e87f286ffb48c3d48ec7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255027"
---
# <a name="understanding-internationalization"></a>Descripción de la internacionalización

El desarrollo de productos de software internacionalizados requiere no solo la producción de código correcto, sino también un diseño que permita que el producto admita muchas configuraciones regionales. Los desarrolladores y sus administradores deben tener en cuenta el nivel de esfuerzo y la atención a los detalles necesarios para crear aplicaciones listas para el mundo, tanto si las entregan como archivos binarios únicos listos para su uso en muchos mercados diferentes, o como varios archivos binarios que son específicos de una configuración regional. Como desarrollador, asegúrese de que la administración entiende que la internacionalización implica algo más que el desarrollo de código. El diseño para la internacionalización al principio del ciclo de producto le ahorra tiempo, dinero y esfuerzo.

**La internacionalización** es la creación de software que se adapta a las configuraciones regionales de todo el mundo. Una **configuración regional es** una colección de preferencias de usuario relacionadas con el idioma. Una configuración regional se especifica mediante el emparejamiento de un idioma y una región geográfica. Por ejemplo, inglés (Estados Unidos) e inglés (Reino Unido) son dos configuraciones regionales diferentes, como inglés (Canadá) y francés (Canadá).

El software internacionalizado tiene estos atributos:

-   **La preparación para el mundo** abarca el diseño y la implementación que separan el código independiente de la configuración regional de los recursos dependientes de la configuración regional y consta de dos áreas principales:
    -   **La globalización** es el proceso de desarrollar un núcleo de programa con características y diseño de código que son independientes del idioma o la configuración regional. En su lugar, el diseño admite la entrada, la presentación y la salida de scripts de lenguaje compatibles con Unicode, así como datos relacionados con configuraciones regionales específicas.
    -   **La localizabilidad** es el diseño de la base de código de software y los recursos, de modo que un programa se puede localizar, tal como se define a continuación, en distintas ediciones de lenguaje sin realizar ningún cambio en el código fuente. Por ejemplo, los búferes de cadena en el código y los cuadros de texto de la interfaz de usuario deben ser lo suficientemente grandes como para dar cabida a cadenas de texto más largas en idiomas como alemán o neerlandés.
-   **Localización** Esto implica traducir y personalizar un producto para un mercado específico, y se trata principalmente de crear archivos de recursos en lugar de escribir código fuente.

Por ejemplo, el uso de La compatibilidad con idiomas nacionales (NLS) proporcionado por la API de Microsoft Win32 es un proceso de desarrollo de software que admite la preparación para el mundo, mientras que la modificación de los elementos de la interfaz de usuario, la traducción de texto y la terminología estandarizada son pasos de localización que normalmente realiza alguien que es un especialista en idiomas, como un traductor. Incluso cuando el desarrollo de código hace hincapié en la preparación para el mundo, es necesario comprender la localización porque las decisiones de diseño afectan al trabajo del traductor.

 

 



