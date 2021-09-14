---
description: Uso de MS Shell Dlg y MS Shell Dlg 2
ms.assetid: ac3b57a6-5b92-4366-ad71-c501cec60997
title: Uso de MS Shell Dlg y MS Shell Dlg 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad43f972e776151551fa312ce2bd8ed6d19be58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254846"
---
# <a name="using-ms-shell-dlg-and-ms-shell-dlg-2"></a>Uso de MS Shell Dlg y MS Shell Dlg 2

Windows está disponible en ediciones localizadas para muchos idiomas. Sin embargo, la edición en inglés también se puede usar para ejecutar aplicaciones escritas en idiomas distintos del inglés. Esto es así incluso cuando el script usado para estos idiomas es diferente, como cuando las aplicaciones se escriben en griego o japonés. Estas aplicaciones requieren una interfaz de usuario con cuadros de diálogo, iconos y utilidades que proporcionan información en el idioma de la aplicación, que puede ser diferente del idioma que se usa en la interfaz de usuario Windows actual.

El problema al seleccionar la fuente de una interfaz de usuario es obvio. Por ejemplo, la fuente del shell, también conocida como fuente predeterminada o del sistema, para inglés (Estados Unidos) Windows 98 es MS Sans Serif, mientras que la fuente de shell para griego (Griego) Windows 98 es MS Sans Serif griego. Para japonés (Japón) Windows 98, la fuente del shell es MS UI Desenlace. Estos juegos de caracteres no se pueden asignar directamente entre sí. Reemplazar MS Sans Serif por MS Sans Serif Griego cuando la configuración regional está establecida en Griego (Griego) no permite que las aplicaciones existentes se ejecuten adecuadamente o que muestren caracteres griegos en los menús del sistema, cuadros de diálogo y controles de edición.

Windows este problema mediante el uso de las fuentes lógicas Dlg y Dlg 2 de MS Shell para permitir la selección de la fuente adecuada para la presentación del script. En esta sección se abordan varias consideraciones de programación para usar las fuentes lógicas para implementar cuadros de diálogo, menús y el tipo para interfaces de usuario flexibles que se muestran bien en todos los sistemas operativos Windows compatibles y en todos los lenguajes. Para obtener más información, vea [Creación y selección de fuentes.](../gdi/font-creation-and-selection.md) Consulte también [Interfaz de usuario multilingüe](multilingual-user-interface.md) para obtener una explicación del uso de la tecnología Interfaz de usuario multilingüe (MUI) en la creación de interfaces de usuario para las aplicaciones multilingües.

## <a name="about-the-logical-fonts"></a>Acerca de las fuentes lógicas

Las fuentes lógicas Dlg de MS Shell y Dlg 2 de MS Shell son básicamente nombres de caras que se usan para la asignación con el objetivo de habilitar la compatibilidad con configuraciones regionales o culturales que tienen caracteres que no están contenidos en la página de códigos 1252, el juego de caracteres Windows para las regiones Estados Unidos y Europa Occidental. Dlg de MS Shell se asigna a la fuente de shell predeterminada asociada a la referencia cultural o configuración regional actual y admite la configuración regional clásica Windows escritorio. El nombre de la cara dlg 2 de MS Shell se introdujo en Windows 2000 para admitir el aspecto que se introdujo con Windows 2000.

Por ejemplo, si la aplicación usa Dlg de Shell de MS o Dlg 2 de MS Shell para sus cuadros de diálogo, un equipo de localización que crea recursos en idioma griego para la aplicación puede centrarse en traducir texto. No tienen que preocuparse por problemas como la distinción entre MS Sans Serif y MS Sans Serif Griego.

> [!Note]  
> Las fuentes generadas por dlg de Shell de MS y dlg 2 de MS Shell son diferentes en diferentes Windows versiones. Por lo tanto, debe asegurarse de que los elementos de la interfaz de usuario se muestren bien en todas las plataformas.

 

## <a name="handle-hard-coded-font-names"></a>Controlar nombres Hard-Coded fuente

El uso de Unicode permite a las aplicaciones tratar con miles de caracteres diferentes, pero la mayoría de las fuentes no cubren todo el juego de caracteres Unicode. Las aplicaciones no deben codificar de forma hard-code nombres de fuente. Una razón es que la codificación rígida de un nombre de fuente que muestra caracteres para un idioma y no caracteres para otro idioma hace que todo el texto localizado en el segundo idioma se muestre incorrectamente. Otra razón para no codificar de forma fuerte los nombres de fuente es que es posible que la fuente deseada no se cargue en el sistema operativo que muestra el texto de la aplicación.

La mejor manera de tratar los nombres de fuente es considerarlos como recursos localizables. El uso de una fuente lógica resuelve el problema de ejecutar la interfaz con cualquier lenguaje en Windows NT o Windows 2000, para cualquier idioma. Establecer un nombre de fuente como un recurso localizable permite que el localizador cambie la fuente de la interfaz de usuario localizada.

## <a name="handle-hard-coded-font-sizes"></a>Controlar los Hard-Coded fuente

Algunos scripts son complejos y requieren un gran número de píxeles para mostrarse correctamente. Por ejemplo, la mayoría de los caracteres en inglés se muestran en una cuadrícula de 5 x 7, pero los caracteres japoneses necesitan al menos una cuadrícula de 16 x 16 para verse claramente. Mientras que el chino necesita una cuadrícula de 24 x 24, el tailandés solo necesita 8 píxeles para el ancho, pero al menos 22 píxeles para la altura. Es fácil entender que algunos caracteres podrían no ser legibles con un tamaño de fuente pequeño.

La interfaz de usuario de la aplicación debe tratar los tamaños de fuente como recursos localizables. El uso de una fuente lógica resuelve el problema de ejecutar la interfaz con cualquier lenguaje en Windows NT o Windows 2000, para cualquier idioma. Establecer un tamaño de fuente como un recurso localizable permite al localizador cambiar la fuente de la interfaz de usuario localizada.

## <a name="map-the-logical-fonts"></a>Asignar las fuentes lógicas

Cada una de las fuentes lógicas se asigna mediante una entrada del Registro a la fuente de shell adecuada para la configuración regional activa actualmente. Cuando se usa una de las fuentes lógicas, Windows cambia a la fuente de la configuración regional seleccionada actualmente en tiempo de ejecución. Esta operación permite mostrar correctamente el inglés (Estados Unidos) Windows interfaz de usuario, así como los caracteres que no están en la página de códigos 1252. Por lo tanto, actualmente las aplicaciones localizadas se pueden ejecutar en la versión en inglés (Estados Unidos) de Windows sin modificaciones.

Cada Windows asigna el dlg de MS Shell y el dlg 2 de MS Shell a una fuente física adecuada, en función del lenguaje definido para los programas no Unicode, que se describe en Terminología de [NLS](nls-terminology.md). Las asignaciones reales se almacenan en la clave del Registro HKEY \_ LOCAL MACHINE Software microsoft Windows NT Current Version \_ \\ \\ \\ \\ \\ FontSubstitutes.

### <a name="font-mapping-on-windows-me9895"></a>Asignación de fuentes Windows me/98/95

Por lo general, el archivo Dlg de MS Shell se asigna a una versión específica de la página de códigos de MS Sans Serif.

### <a name="font-mapping-on-windows-nt-40"></a>Asignación de fuentes Windows NT 4.0

Dlg de MS Shell se asigna a MS Sans Serif para idiomas europeos y centroeuropeos, griegos, turcos, turcos e idiomas mediante script cirílico. MS UI Desenlace para japonés; Gulim para coreano; Simsun para chino simplificado; PMinglu para chino tradicional; Etc.

### <a name="font-mapping-on-windows-2000-windows-xp-windows-server-2003-windows-vista-and-windows-7"></a>Asignación de fuentes en Windows 2000, Windows XP, Windows Server 2003, Windows Vista y Windows 7

Ambas fuentes lógicas se asignan a fuentes TrueType basadas en Unicode. MS Shell Dlg usa Microsoft Sans Serif (distinto de MS Sans Serif) si el idioma de instalación no es japonés. El archivo Dlg de MS Shell se asigna a la interfaz de usuario de MS En caso de que el idioma de instalación sea japonés.

En Windows XP DLG, el dlg del shell de MS se asigna a la interfaz de usuario de MS Desasorio solo cuando la configuración regional del sistema y el idioma de la interfaz de usuario están establecidos en japonés. De lo contrario, MS Shell Dlg se asigna a Microsoft Sans Serif.

En Windows Vista y Windows 7, el archivo Dlg de MS Shell se asigna a MS UI Deserción si el idioma predeterminado de la interfaz de usuario de la máquina está establecido en japonés (independientemente del idioma de instalación). Dlg de MS Shell se asigna a Microsoft Sans Serif si el idioma predeterminado de la interfaz de usuario de la máquina está establecido en un idioma distinto del japonés.

MS Shell Dlg 2 simplemente usa la fuente Denoma independientemente del idioma. La principal ventaja deCtooma sobre Microsoft Sans Serif es que Tiene una cara de fuente nativa en negrita. Su principal desventaja es que los sistemas operativos más antiguos podrían no tener instalado y podrían sustituir una fuente menos atractiva.

Los caracteres que no se implementan en Nooma o Microsoft Sans Serif se pueden implementar en otras fuentes Windows que se usan para la presentación de texto en las interfaces de usuario. En función de qué controles o API se usan [](https://msdn.microsoft.com/globalization/mt662331) para mostrar texto, el sistema puede usar varios mecanismos, como la vinculación de fuentes, para seleccionar automáticamente dichas fuentes para mostrar esos caracteres.

Las aplicaciones pueden usar Microsoft Sans Serif o Cascaoma explícitamente, y guardar el nivel de direccionamiento indirecto implicado en el uso de Dlg de Shell de MS o Dlg 2 de MS Shell. Debido a la vinculación de fuentes, la especificación de Microsoft Sans Serif o Unicodeoma proporciona glifos adecuados para todos los idiomas.

## <a name="use-ms-shell-dlg-for-a-non-english-application-on-windows-me9895"></a>Uso de dlg de Shell de MS para una aplicación que no está en inglés Windows me/98/95

En Windows Me/98/95, MS Shell Dlg no está diseñado para su uso con una aplicación de interfaz de usuario estática y no inglesa que se ejecuta cuando el usuario ha elegido una configuración regional con un juego de caracteres base Windows diferente. En este caso, es posible que el lenguaje de interfaz de usuario de la aplicación no sea compatible con la fuente que se sustituye por dlg de Shell de MS.

Por ejemplo, si el usuario usa una versión en alemán de Windows y desea instalar una aplicación de idioma griego no Unicode, el usuario intenta cambiar la configuración regional a Griego (Griego). Esta acción restablece el dlg de Shell de MS a una fuente griego, pero esta fuente no contiene todos los glifos necesarios para mostrarse en alemán. Por lo tanto, los caracteres no ASCII de la interfaz de usuario en alemán no se mostrarán correctamente. Para admitir este escenario, una aplicación tiene que establecer MS Shell Dlg en una fuente que contenga los glifos europeo occidental y griego.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enumeración y selección de fuentes internacionales](using-international-fonts-and-text.md)
</dt> <dt>

[Interfaz de usuario multilingüe](multilingual-user-interface.md)
</dt> </dl>

 

 
