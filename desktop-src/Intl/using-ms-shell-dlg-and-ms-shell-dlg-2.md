---
description: Usar MS Shell Dlg y MS Shell Dlg 2
ms.assetid: ac3b57a6-5b92-4366-ad71-c501cec60997
title: Usar MS Shell Dlg y MS Shell Dlg 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad43f972e776151551fa312ce2bd8ed6d19be58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688698"
---
# <a name="using-ms-shell-dlg-and-ms-shell-dlg-2"></a>Usar MS Shell Dlg y MS Shell Dlg 2

Windows está disponible en ediciones localizadas para muchos idiomas. Sin embargo, la edición en inglés también puede usarse para ejecutar aplicaciones escritas en idiomas distintos del inglés. Esto es así incluso cuando el script usado para estos idiomas es diferente, como cuando las aplicaciones están escritas en griego o japonés. Estas aplicaciones requieren una interfaz de usuario con cuadros de diálogo, iconos y utilidades que proporcionan información en el idioma de la aplicación, que puede ser diferente del idioma que se usa en la interfaz de usuario actual de Windows.

El problema al seleccionar la fuente para una interfaz de usuario es obvio. Por ejemplo, la fuente de Shell, también conocida como fuente del sistema o predeterminada, para inglés (Estados Unidos) Windows 98 es MS Sans Serif, mientras que la fuente de Shell para el griego (Grecia) Windows 98 es MS Sans Serif griego. En el caso de Windows 98 japonés (Japón), la fuente de Shell es MS UI Gothic. Estos juegos de caracteres no se pueden asignar directamente entre sí. El reemplazo de MS Sans Serif con MS Sans Serif griego cuando la configuración regional está establecida en griego (Grecia) no permite que las aplicaciones existentes se ejecuten correctamente o que muestren caracteres griegos en menús del sistema, cuadros de diálogo y controles de edición.

Windows resuelve este problema mediante las fuentes lógicas de MS Shell Dlg y MS Shell Dlg 2 para permitir la selección de la fuente adecuada para la presentación del script. En esta sección se tratan varias consideraciones de programación para usar las fuentes lógicas con el fin de implementar cuadros de diálogo, menús y similares para las interfaces de usuario flexibles que se muestran correctamente en todos los sistemas operativos Windows compatibles y en todos los idiomas. Para obtener más información, vea [creación y selección de fuentes](../gdi/font-creation-and-selection.md). Vea también [interfaz de usuario multilingüe](multilingual-user-interface.md) para obtener una explicación del uso de la tecnología de interfaz de usuario multilingüe (MUI) en la creación de interfaces de usuario para aplicaciones multilingües.

## <a name="about-the-logical-fonts"></a>Acerca de las fuentes lógicas

Las fuentes lógicas MS Shell Dlg y MS Shell Dlg 2 son esencialmente nombres de fuente que se usan para la asignación con el fin de habilitar la compatibilidad con configuraciones regionales y referencias culturales con caracteres que no se incluyen en la página de códigos 1252, el juego de caracteres de Windows para el Estados Unidos y Europa occidental. MS Shell Dlg se asigna a la fuente de Shell predeterminada asociada con la referencia cultural o configuración regional actual y admite la apariencia clásica del escritorio de Windows. El nombre de la esfera de MS Shell Dlg 2 se presentó en Windows 2000 para admitir el aspecto que se presentó con Windows 2000.

Por ejemplo, si la aplicación usa MS Shell Dlg o MS Shell Dlg 2 para sus cuadros de diálogo, un equipo de localización que cree recursos de idioma griego para la aplicación puede centrarse en la traducción de texto. No tienen que preocuparse por problemas como la distinción entre MS Sans Serif y MS Sans Serif griego.

> [!Note]  
> Las fuentes generadas por MS Shell Dlg y MS Shell Dlg 2 son diferentes en las distintas versiones de Windows. Por lo tanto, debe asegurarse de que los elementos de la interfaz de usuario se muestren correctamente en todas las plataformas.

 

## <a name="handle-hard-coded-font-names"></a>Administrar Hard-Coded nombres de fuente

El uso de Unicode permite a las aplicaciones tratar con miles de caracteres diferentes, pero la mayoría de las fuentes no cubren todo el juego de caracteres Unicode. Las aplicaciones no deben codificar los nombres de fuente de forma rígida. Una razón es que la codificación rígida de un nombre de fuente que muestra caracteres para un idioma y no caracteres para otro idioma hace que todo el texto localizado en el segundo idioma se muestre incorrectamente. Otra razón para no codificar los nombres de fuente es que la fuente deseada podría no cargarse en el sistema operativo que muestra el texto de la aplicación.

La mejor manera de tratar los nombres de fuente es considerarlos como recursos localizables. El uso de una fuente lógica resuelve el problema de ejecutar la interfaz con cualquier idioma en Windows NT o Windows 2000, para cualquier lenguaje. La configuración de un nombre de fuente como un recurso traducible permite que el localizador cambie la fuente de la interfaz de usuario localizada.

## <a name="handle-hard-coded-font-sizes"></a>Controlar los tamaños de fuente de Hard-Coded

Algunos scripts son complejos y requieren un gran número de píxeles para que se muestren correctamente. Por ejemplo, la mayoría de los caracteres ingleses se muestran en una cuadrícula de 5x7, pero los caracteres japoneses necesitan al menos una cuadrícula de 16x16 para que se puedan ver claramente. Mientras que el chino necesita una cuadrícula 24x24, el tailandés solo necesita 8 píxeles para el ancho, pero al menos 22 píxeles para el alto. Es fácil comprender que algunos caracteres podrían no ser legibles en un tamaño de fuente pequeño.

La interfaz de usuario de la aplicación debe tratar los tamaños de fuente como recursos localizables. El uso de una fuente lógica resuelve el problema de ejecutar la interfaz con cualquier idioma en Windows NT o Windows 2000, para cualquier lenguaje. La configuración de un tamaño de fuente como recurso traducible permite que el localizador cambie la fuente de la interfaz de usuario localizada.

## <a name="map-the-logical-fonts"></a>Asignar las fuentes lógicas

Cada una de las fuentes lógicas se asigna mediante una entrada del registro a la fuente de Shell adecuada para la configuración regional activa actualmente. Cuando se usa una de las fuentes lógicas, Windows cambia a la fuente para la configuración regional seleccionada actualmente en tiempo de ejecución. Esta operación permite la visualización correcta de la interfaz de usuario de Windows en inglés (Estados Unidos), así como los caracteres que no aparecen en la página de códigos 1252. Por lo tanto, las aplicaciones localizadas que se envían actualmente se pueden ejecutar en la versión de Windows en inglés (Estados Unidos) sin modificaciones.

Cada equipo de Windows asigna MS Shell Dlg y MS Shell Dlg 2 a una fuente física adecuada, según el idioma definido para programas no Unicode, que se describe en [terminología de NLS](nls-terminology.md). Las asignaciones reales se almacenan en la clave del registro HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ versión actual \\ FontSubstitutes.

### <a name="font-mapping-on-windows-me9895"></a>Asignación de fuentes en Windows Me/98/95

En general, MS Shell Dlg se asigna a una versión específica de la página de códigos de MS Sans Serif.

### <a name="font-mapping-on-windows-nt-40"></a>Asignación de fuentes en Windows NT 4,0

MS Shell Dlg se asigna a MS Sans Serif para Europa occidental y central, griego, Turco, Báltico y idiomas mediante el script cirílico; MS UI Gothic para japonés; Gulim para Coreano; Simsun para chino simplificado; PMinglu para chino tradicional; otros.

### <a name="font-mapping-on-windows-2000-windows-xp-windows-server-2003-windows-vista-and-windows-7"></a>Asignación de fuentes en Windows 2000, Windows XP, Windows Server 2003, Windows Vista y Windows 7

Ambas fuentes lógicas se asignan a fuentes TrueType basadas en Unicode. MS Shell Dlg usa Microsoft sans serif (distinto de MS Sans serif) si el idioma de instalación no es japonés. MS Shell Dlg se asigna a MS UI Gothic si el idioma de instalación es el japonés.

En los sistemas MUI de Windows XP, MS Shell Dlg se asigna a MS UI Gothic solo cuando la configuración regional del sistema y el idioma de la interfaz de usuario están establecidos en japonés. De lo contrario, MS Shell Dlg se asigna a Microsoft sans serif.

En Windows Vista y Windows 7, MS Shell Dlg se asigna a MS UI Gothic si el idioma predeterminado de la interfaz de usuario de la máquina está establecido en japonés (independientemente del idioma de instalación). MS Shell Dlg se asigna a Microsoft sans serif si el idioma de la interfaz de usuario predeterminada de la máquina está establecido en un idioma distinto del japonés.

MS Shell Dlg 2 simplemente utiliza la fuente Tahoma independientemente del lenguaje. La principal ventaja de Tahoma sobre Microsoft sans serif es que Tahoma tiene un aspecto de fuente Negrita nativo. Su principal desventaja es que es posible que los sistemas operativos anteriores no los tengan instalado y puede sustituir una fuente menos atractiva.

Los caracteres que no se implementan en Tahoma o en Microsoft sans serif se pueden implementar en otras fuentes de Windows que se usan para la presentación de texto en interfaces de usuario. En función de los controles o las API que se usan para mostrar texto, el sistema puede usar varios mecanismos como la [vinculación de fuentes](https://msdn.microsoft.com/globalization/mt662331) para seleccionar automáticamente estas fuentes para mostrar esos caracteres.

Las aplicaciones pueden usar Microsoft sans serif o Tahoma explícitamente y guardar el nivel de direccionamiento indirecto implicado en el uso de MS Shell Dlg o MS Shell Dlg 2. Debido a la vinculación de fuentes, la especificación de Microsoft sans serif o Tahoma proporciona glifos adecuados para todos los idiomas.

## <a name="use-ms-shell-dlg-for-a-non-english-application-on-windows-me9895"></a>Usar MS Shell Dlg para una aplicación que no esté en inglés en Windows Me/98/95

En Windows Me/98/95, MS Shell Dlg no está diseñado para usarse con una aplicación de interfaz de usuario estática que no sea en inglés y que se ejecute cuando el usuario haya elegido una configuración regional con un juego de caracteres base de Windows diferente. En este caso, es posible que el idioma de la interfaz de usuario de la aplicación no sea compatible con la fuente sustituida por MS Shell Dlg.

Por ejemplo, si el usuario utiliza una versión de Windows en el idioma alemán y desea instalar una aplicación de idioma griego que no sea Unicode, el usuario intenta cambiar la configuración regional a griego (Grecia). Esta acción restablece MS Shell Dlg en una fuente griega, pero esta fuente no contiene todos los glifos necesarios para mostrar en alemán. Por lo tanto, los caracteres que no sean ASCII en la interfaz de usuario de idioma alemán no se mostrarán correctamente. Para admitir este escenario, una aplicación tiene que establecer MS Shell Dlg en una fuente que contenga los glifos europeo occidental y griego.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeración y selección de fuentes internacionales](using-international-fonts-and-text.md)
</dt> <dt>

[Interfaz de usuario multilingüe](multilingual-user-interface.md)
</dt> </dl>

 

 
