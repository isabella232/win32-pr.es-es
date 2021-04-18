---
description: Descripción de la internacionalización
ms.assetid: 9147cd20-eeae-4ad4-8d51-ac1d68a4b2c5
title: Descripción de la internacionalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df3fc38ab844ec991c0e87f286ffb48c3d48ec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688198"
---
# <a name="understanding-internationalization"></a>Descripción de la internacionalización

El desarrollo de productos de software internacionalizados no solo requiere la producción de código correcto, sino también un diseño que permita que el producto admita muchas configuraciones regionales. Los desarrolladores y sus administradores deben tener en cuenta el nivel de esfuerzo y la atención de los detalles necesarios para crear aplicaciones de uso internacional, tanto si las entregan como archivos binarios únicos listos para usarse en muchos mercados diferentes como si son varios binarios que son específicos de una configuración regional. Como desarrollador, asegúrese de que su administración entiende que la internacionalización implica algo más que el desarrollo de código. El diseño para la internacionalización al principio del ciclo del producto le ahorra tiempo, dinero y esfuerzo.

**Internacionalización** es la creación de software que se adapta a las configuraciones regionales en todo el mundo. Una **configuración regional** es una colección de preferencias de usuario relacionadas con el lenguaje. La configuración regional se especifica mediante el emparejamiento de un idioma y una región geográfica. Por ejemplo, Inglés (Estados Unidos) e inglés (Reino Unido) son dos configuraciones regionales diferentes, como inglés (Canadá) y francés (Canadá).

El software internacionalizado tiene estos atributos:

-   **La preparación mundial** cubre el diseño y la implementación que separa el código independiente de la configuración regional de los recursos dependientes de la configuración regional y consta de dos áreas principales:
    -   La **globalización** es el proceso de desarrollar un núcleo de programa con características y diseño de código que son independientes del idioma o la configuración regional. En su lugar, el diseño es compatible con la entrada, la presentación y la salida de los scripts de lenguaje compatibles con Unicode, así como los datos relacionados con las configuraciones regionales específicas.
    -   La **localizabilidad** es el diseño de la base de código de software y los recursos de modo que se pueda localizar un programa, como se define a continuación, en ediciones de idioma diferentes sin necesidad de realizar cambios en el código fuente. Por ejemplo, los búferes de cadena en el código y los cuadros de texto de la interfaz de usuario deben ser lo suficientemente grandes como para admitir cadenas de texto más largas en idiomas como el alemán o el holandés.
-   **Localización** de Esto implica traducir y personalizar un producto para un mercado específico, y es principalmente la creación de archivos de recursos en lugar de escribir código fuente.

Por ejemplo, el uso de la compatibilidad con el idioma nacional (NLS) que proporciona la API Win32 de Microsoft es un proceso de desarrollo de software que admite la preparación mundial, mientras que la modificación de los elementos de la interfaz de usuario, la traducción de texto y la estandarización de la terminología son pasos de localización que suele realizar alguien que es un especialista en lenguaje, como un traductor. Incluso cuando el desarrollo de código enfatiza la preparación mundial, debe comprender la localización porque las decisiones de diseño afectan al trabajo del traductor.

 

 



