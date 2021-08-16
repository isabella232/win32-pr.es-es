---
description: El término &\# 0034;language&0034; indica una colección de propiedades usadas en la comunicación hablada \# y escrita.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Configuraciones regionales e idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 462fc66a3296312de73a472309457e12954b6f30c80857594808350306bf4994
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147160"
---
# <a name="locales-and-languages"></a>Configuraciones regionales e idiomas

El término "idioma" indica una colección de propiedades usadas en la comunicación hablada y escrita. Cada idioma tiene un nombre de idioma y un identificador de idioma que indican [](table-of-geographical-locations.md) la página de códigos concreta [(ANSI,](code-pages.md) DOS, Macintosh) que se usa para representar la ubicación geográfica del idioma en el sistema operativo. Un idioma neutro se indica mediante un nombre como "en" para inglés. Un idioma más específico geográficamente se puede indicar mediante un nombre que incluya la configuración regional y la información de país o región. Por ejemplo, la configuración regional inglés (Estados Unidos) tiene el nombre de idioma "en-US".

Una "configuración regional" es una colección de información de preferencias de usuario relacionada con el idioma representada como una lista de valores. Windows XP admite más de 150 configuraciones regionales y Windows Vista admite aproximadamente 200. Cada configuración regional se define mediante un idioma y un criterio de ordenación, y tiene un nombre de configuración regional y un identificador de configuración regional. Un ejemplo de un nombre de configuración regional para alemán (Alemania) es "de-DE \_ phonebook".

Cada sistema operativo tiene al menos una configuración regional instalada y, a menudo, tiene muchas configuraciones regionales entre las que el usuario puede seleccionar. Cada configuración regional tiene una variedad de información asociada, aparte de su nombre y su identificador. Los tipos de información de configuración regional se describen en [Constantes de información de configuración regional](locale-information-constants.md).

El sistema operativo asigna una configuración regional a cada subproceso, asignando inicialmente la "configuración regional predeterminada del sistema", definida por [LOCALE \_ SYSTEM \_ DEFAULT](locale-system-default.md). Esta configuración regional se establece cuando se instala el sistema operativo o cuando el usuario la selecciona mediante la parte de opciones regionales y de idioma de la Panel de control. Al ejecutar un subproceso en un proceso que pertenece al usuario, el sistema operativo asigna la "configuración regional predeterminada del usuario" al subproceso. Esta configuración regional se define mediante [LOCALE \_ USER \_ DEFAULT.](locale-user-default.md) Una aplicación puede invalidar cualquiera de los valores predeterminados mediante la [**función SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) para establecer explícitamente la configuración regional de un subproceso.

La implementación de un idioma requiere una configuración regional correspondiente. El sistema operativo implementa un idioma neutro seleccionando los datos de la configuración regional asociada a una versión específica del idioma, normalmente la configuración regional más extendida.

A partir Windows Vista, es posible que un idioma determinado se corresponda con una configuración regional complementaria, que es un tipo de configuración regional personalizada. Dado que todas las configuraciones regionales complementarias comparten un único identificador de configuración regional, las aplicaciones deben controlar estas configuraciones regionales y los idiomas correspondientes por nombre en lugar de por identificador.

Los conceptos de lenguaje están estrechamente relacionados con los conceptos de configuración regional, pero los dos términos no son intercambiables. Como regla general, las funciones relacionadas con el [Interfaz de usuario multilingüe](multilingual-user-interface.md) tratan con lenguajes, mientras que las funciones NLS actúan sobre las configuraciones regionales.

En esta sección se tratan los siguientes temas:

-   [Configuraciones regionales personalizadas](custom-locales.md)
-   [Identificadores de idioma](language-identifiers.md)
-   [Nombres de idioma](language-names.md)
-   [Identificadores de configuración regional](locale-identifiers.md)
-   [Nombres de configuración regional](locale-names.md)
-   [Pseudo-Configuraciones regionales](pseudo-locales.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la compatibilidad con idiomas nacionales](about-national-language-support.md)
</dt> <dt>

[Páginas de códigos](code-pages.md)
</dt> <dt>

[Constantes de información de configuración regional](locale-information-constants.md)
</dt> <dt>

[Interfaz de usuario multilingüe](multilingual-user-interface.md)
</dt> <dt>

[Tabla de ubicaciones geográficas](table-of-geographical-locations.md)
</dt> <dt>

[Interfaz de usuario Language Management](user-interface-language-management.md)
</dt> <dt>

[**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



