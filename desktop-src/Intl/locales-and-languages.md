---
description: El término &\# 0034; language&\# 0034; indica una colección de propiedades utilizadas en la comunicación oral y escrita.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Configuraciones regionales e idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687098"
---
# <a name="locales-and-languages"></a>Configuraciones regionales e idiomas

El término "idioma" indica una colección de propiedades que se utilizan en la comunicación escrita y oral. Cada idioma tiene un nombre de idioma y un identificador de idioma que indican la [Página de códigos](code-pages.md) determinada (ANSI, dos, Macintosh) que se usa para representar la [ubicación geográfica](table-of-geographical-locations.md) del idioma en el sistema operativo. Un idioma neutro se indica con un nombre como "en" para inglés. Un idioma más específico geográficamente puede indicarse mediante un nombre que incluya información de configuración regional y país o región. Por ejemplo, la configuración regional inglés (Estados Unidos) tiene el nombre de idioma "en-US".

Una "configuración regional" es una colección de información de preferencias de usuario relacionada con el lenguaje que se representa como una lista de valores. Windows XP admite más de 150 configuraciones regionales y Windows Vista admite aproximadamente 200. Cada configuración regional se define mediante un lenguaje y un criterio de ordenación, y tiene un nombre de configuración regional y un identificador de configuración regional. Un ejemplo de un nombre de configuración regional para alemán (Alemania) es "de-DE la \_ Guía de teléfonos".

Cada sistema operativo tiene al menos una configuración regional instalada y a menudo tiene muchas configuraciones regionales desde las que el usuario puede seleccionar. Cada configuración regional tiene una gran variedad de información asociada, aparte de su nombre y identificador. Los tipos de información de configuración regional se describen en [constantes de información de configuración regional](locale-information-constants.md).

El sistema operativo asigna una configuración regional a cada subproceso, asignando inicialmente la "configuración regional predeterminada del sistema", definida por el [ \_ \_ valor predeterminado del sistema de configuración regional](locale-system-default.md). Esta configuración regional se establece cuando se instala el sistema operativo o cuando el usuario lo selecciona mediante la parte de configuración regional y de idioma del panel de control. Cuando se ejecuta un subproceso en un proceso que pertenece al usuario, el sistema operativo asigna la "configuración regional predeterminada del usuario" al subproceso. Esta configuración regional se define mediante el [ \_ \_ valor predeterminado de usuario de configuración regional](locale-user-default.md). Una aplicación puede invalidar de forma predeterminada mediante la función [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) para establecer explícitamente la configuración regional de un subproceso.

La implementación de un lenguaje requiere una configuración regional correspondiente. El sistema operativo implementa un idioma neutro seleccionando los datos de la configuración regional asociada a una versión específica del idioma, normalmente la configuración regional más generalizada.

A partir de Windows Vista, es posible que un idioma determinado se corresponda con una configuración regional complementaria, que es un tipo de configuración regional personalizada. Como las configuraciones regionales complementarias comparten un único identificador de configuración regional, las aplicaciones deben controlar estas configuraciones regionales y los idiomas correspondientes por nombre en lugar de por identificador.

Los conceptos del lenguaje están estrechamente relacionados con los conceptos de configuración regional, pero los dos términos no son intercambiables. Como norma general, las funciones relacionadas con la [interfaz de usuario multilingüe](multilingual-user-interface.md) se ocupan de los lenguajes, mientras que las funciones NLS actúan en configuraciones regionales.

En esta sección se tratan los siguientes temas:

-   [Configuraciones regionales personalizadas](custom-locales.md)
-   [Identificadores de idioma](language-identifiers.md)
-   [Nombres de idioma](language-names.md)
-   [Identificadores de configuración regional](locale-identifiers.md)
-   [Nombres de configuración regional](locale-names.md)
-   [Pseudo-configuraciones regionales](pseudo-locales.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la compatibilidad con National Language](about-national-language-support.md)
</dt> <dt>

[Páginas de códigos](code-pages.md)
</dt> <dt>

[Constantes de información de configuración regional](locale-information-constants.md)
</dt> <dt>

[Interfaz de usuario multilingüe](multilingual-user-interface.md)
</dt> <dt>

[Tabla de ubicaciones geográficas](table-of-geographical-locations.md)
</dt> <dt>

[Administración del idioma de la interfaz de usuario](user-interface-language-management.md)
</dt> <dt>

[**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



