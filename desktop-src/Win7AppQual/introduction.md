---
description: Introducción (Windows guía de calidad de la aplicación Windows Server 2008 R2)
ms.assetid: 6BB5AABC-6281-4575-8189-477C57DF4F4F
title: Introducción (Windows guía de calidad de la aplicación Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4125c2bd122d239c155f089f06bef2f455ee121b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253244"
---
# <a name="introduction-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Introducción (Windows guía de calidad de la aplicación Windows Server 2008 R2)

En todo el mundo, muchas empresas adoptan Windows 7 debido a sus características y capacidades empresariales. Los departamentos de TI también están cambiando la forma en que se aproximan a sus necesidades de plataforma a largo plazo para admitir un escritorio moderno. El Windows operativo 7 ayuda a reducir el costo total de propiedad al ayudar a los usuarios a mantener la productividad en cualquier lugar, mejora la seguridad y el control, y simplifica la administración de escritorio en toda la organización. Windows 7 también incluye un explorador moderno basado en estándares, Windows Internet Explorer 8, que proporciona una seguridad mejorada y funcionalidades de exploración mejoradas. Estas dos plataformas aumentan la eficacia de IT y mejoran la agilidad y la seguridad de una organización.

Sin embargo, la migración a un nuevo sistema operativo crea desafíos únicos, principalmente con la necesidad de admitir aplicaciones web heredadas. Las empresas pueden tener aplicaciones creadas para versiones anteriores de Windows Internet Explorer, como Windows Internet Explorer 7 o Microsoft Internet Explorer 6. Estas aplicaciones web pueden encontrar problemas de compatibilidad con Internet Explorer 8. Además, Internet Explorer 6 no se ejecuta de forma nativa en Windows 7 y Windows no admite la ejecución de dos versiones de Internet Explorer simultáneamente. Para obtener más información, vea el Microsoft Knowledge Base,["Ejecutar](https://support.microsoft.com/kb/2020599)varias versiones de Internet Explorer en un único sistema operativo no es compatible".

Muchas empresas siguen utilizando Internet Explorer web basadas en 6 que se crearon y personalizaron durante la última década. Las empresas que planean implementar Windows 7 deben tener una estrategia completa y un plan de ejecución para migrar aplicaciones web heredadas a Internet Explorer 8. En este documento se proporciona información general detallada sobre Internet Explorer 8 problemas de compatibilidad, se describe cómo migrar aplicaciones web y se presentan herramientas y procesos relacionados.

La Internet Explorer 8 se centra en tres temas principales:

-   Proporcionar interoperabilidad real con otros exploradores y compatibilidad con sitios web existentes.
-   Haga que el desarrollo web sea más rápido y sencillo mediante las herramientas de desarrollo integradas.
-   Habilite experiencias que lleguen más allá de la página, a través de nuevas características del explorador que conectan a los usuarios a servicios web innovadores.

Además de importantes avances en la compatibilidad con estándares, Internet Explorer 8 contiene inversiones en plataformas adicionales para desarrolladores. Internet Explorer 8 mejora el rendimiento en muchos subsistemas de Internet Explorer, como el analizador HTML, el procesamiento de reglas de hoja de estilos en cascada (CSS), la manipulación del árbol de marcado, el analizador de JavaScript, el tiempo de ejecución del recolector de elementos no utilizados y la administración de memoria. Las inversiones adicionales para desarrolladores incluyen:

-   CSS 2.1: puede escribir las páginas una vez y hacer que se representen más fácilmente correctamente en distintos exploradores, ya que Internet Explorer 8 es totalmente compatible con la especificación CSS 2.1.
-   Document Object Model (DOM) y mejoras de HTML 4.01: Internet Explorer 8 proporciona mejoras adicionales de HTML 4.01 y cumplimiento completo de CSS 2.1. Internet Explorer 8 también corrige muchas incoherencias entre exploradores. Por ejemplo, la implementación de atributos get,set/remove ahora es interoperable con otros exploradores y se mejora el rendimiento en patrones de diseño asincrónicos de JavaScript y XML (AJAX).
-   Estándares emergentes: Internet Explorer 8 incorpora estándares futuros, como el estándar HTML5 Draft DOM Storage de W3C, la API Selectors del grupo de trabajo de aplicaciones web y la sintaxis aprobada de ECMAScript 3.1.
-   Nuevas características de navegación para aplicaciones AJAX: puede actualizar la pila de navegación hacia atrás y hacia delante del explorador y la barra de direcciones desde una aplicación AJAX para que esas características del explorador funcionen correctamente en la aplicación.
-   Acid2: Internet Explorer 8 representa correctamente la prueba del explorador Acid2.
-   Compatibilidad: Internet Explorer 8 incluye un motor de diseño más compatible con estándares que permite crear un sitio basado en estándares para varios exploradores. Para migrar los sitios más fácilmente al nuevo motor de diseño compatible con estándares, Internet Explorer 8 le permite usar el motor de diseño de Internet Explorer 7 insertando un elemento **meta** simple en el código o agregando un solo encabezado HTTP en los servidores.
-   Herramientas de desarrollo: Herramientas de desarrollo en Internet Explorer (al que se accede presionando la tecla F12) le permiten depurar rápidamente código HTML, CSS y JavaScript en un entorno visual. Estas herramientas se incluyen directamente en Internet Explorer 8 con funcionalidad expandida, incluida la opción ann para elegir qué aplicación usar al ver el origen de una página web. Puede identificar y resolver rápidamente los problemas debido a la profunda información que proporciona la herramienta en dom.
-   Para obtener más información sobre las características nuevas y mejoradas de Internet Explorer 8, vea Novedades de [Internet Explorer 8](https://msdn.microsoft.com/library/Gg598940(v=VS.85).aspx) en MSDN Library.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Abordar la compatibilidad de aplicaciones al migrar a Internet Explorer 8](addressing-application-compatibility-when-migrating-to-internet-explorer-8.md)
</dt> </dl>

 

 



