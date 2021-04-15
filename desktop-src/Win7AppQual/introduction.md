---
description: .
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: Introducción (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d491802735ddf1ef75a7a183cd49afea2cc657b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648453"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Introducción (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)

En todo el mundo, muchas empresas están adoptando Windows 7 debido a sus características y capacidades empresariales. Los departamentos de ti también cambian el modo en que se aproximan a sus necesidades de plataforma a largo plazo para admitir un escritorio moderno. El sistema operativo Windows 7 ayuda a reducir el costo total de propiedad ayudando a los usuarios a ser productivos en cualquier lugar, mejora la seguridad y el control, y simplifica la administración del escritorio en toda la organización. Windows 7 también incluye un explorador moderno basado en estándares, Windows Internet Explorer 8, que proporciona mayor seguridad y capacidades de exploración mejoradas. Estas dos plataformas aumentan la eficacia de ti y mejoran la agilidad y la seguridad de una organización.

Sin embargo, la migración a un nuevo sistema operativo crea desafíos únicos, principalmente con la necesidad de admitir aplicaciones web heredadas. Las empresas pueden tener aplicaciones compiladas para versiones anteriores de Windows Internet Explorer, como Windows Internet Explorer 7 o Microsoft Internet Explorer 6. Estas aplicaciones Web pueden encontrar problemas de compatibilidad con Internet Explorer 8. Además, Internet Explorer 6 no se ejecuta de forma nativa en Windows 7 y Windows no admite la ejecución simultánea de dos versiones de Internet Explorer. Para obtener más información, vea el artículo de Microsoft Knowledge base "no[se admite la ejecución de varias versiones de Internet Explorer en un solo sistema operativo](https://support.microsoft.com/kb/2020599)".

Muchas empresas todavía usan aplicaciones web basadas en Internet Explorer 6 que se han creado y personalizado durante la última década. Las empresas que planean implementar Windows 7 deben tener una estrategia completa y un plan de ejecución para migrar las aplicaciones web heredadas a Internet Explorer 8. En este documento se proporciona información general detallada sobre los problemas de compatibilidad de Internet Explorer 8, se explica cómo migrar aplicaciones web y se presentan las herramientas y los procesos relacionados.

La versión de Internet Explorer 8 se centra en tres temas principales:

-   Proporcionar interoperabilidad real con otros exploradores y compatibilidad para los sitios Web existentes.
-   Haga que el desarrollo web sea más rápido y sencillo con las herramientas de desarrollo integradas.
-   Habilite experiencias que lleguen más allá de la página a través de nuevas características del explorador que conectan a los usuarios con los servicios web innovadores.

Además de los avances significativos en la compatibilidad con estándares, Internet Explorer 8 contiene inversiones adicionales en la plataforma para los desarrolladores. Internet Explorer 8 mejora el rendimiento en muchos subsistemas de Internet Explorer, como el analizador de HTML, el procesamiento de reglas de hojas de estilos en cascada (CSS), la manipulación de árboles de marcado, el analizador de JavaScript, el tiempo de ejecución del recolector de elementos no utilizados y la administración de memoria. Entre las inversiones adicionales para desarrolladores se incluyen:

-   CSS 2,1: puede escribir las páginas una vez y hacer que se representen con mayor facilidad en diferentes exploradores, ya que Internet Explorer 8 es totalmente compatible con la especificación 2,1 de CSS.
-   Mejoras en Document Object Model (DOM) y HTML 4,01: Internet Explorer 8 proporciona mejoras adicionales de HTML 4,01 y compatibilidad completa con CSS 2,1. Internet Explorer 8 también corrige muchas incoherencias entre exploradores. Por ejemplo, la implementación del atributo Get/Set/Remove ahora es interoperable con otros exploradores y se ha mejorado el rendimiento en los patrones de diseño asincrónicos JavaScript y XML (AJAX).
-   Estándares emergentes: Internet Explorer 8 incorpora estándares futuros, como W3C HTML5 draft DOM Storage Standard, la API de selectores del grupo de trabajo de aplicaciones web y la sintaxis aprobada de ECMAScript 3,1.
-   Nuevas características de navegación para aplicaciones AJAX: puede actualizar la pila de navegación atrás y adelante del explorador y la barra de direcciones desde aplicaciones AJAX para que las características del explorador funcionen correctamente en la aplicación.
-   Acid2: Internet Explorer 8 representa correctamente la prueba del explorador Acid2.
-   Compatibilidad: Internet Explorer 8 incluye un motor de diseño compatible con estándares que permite crear un sitio basado en estándares para varios exploradores. Para migrar los sitios más fácilmente al nuevo motor de diseño compatible con los estándares, Internet Explorer 8 le permite usar el motor de diseño de Internet Explorer 7 insertando un elemento **meta** simple en el código o agregando un único encabezado HTTP en los servidores.
-   Herramientas de desarrollo: Herramientas de desarrollo de Internet Explorer (a la que se tiene acceso presionando la tecla F12) permite depurar rápidamente código HTML, CSS y JavaScript en un entorno visual. Estas herramientas se incluyen directamente en Internet Explorer 8 con funcionalidad ampliada, incluida la opción de Ana para elegir la aplicación que se va a utilizar al ver el origen de una página web. Puede identificar y resolver rápidamente los problemas debido a la información detallada que proporciona la herramienta en el DOM.
-   Para obtener más información acerca de las características nuevas y mejoradas de Internet Explorer 8, vea [novedades de Internet Explorer 8](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) en MSDN Library.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Abordar la compatibilidad de aplicaciones al migrar a Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



